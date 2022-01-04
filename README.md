# PostfwdEnv

A sample project for postfwd environment, including plugins and rules

# Execution (On Ubuntu)
- Startup Script
	- /etc/default/postfwd || /etc/init.d/postfwd
		- --plugins: plugin files (postfwd2.1.35.plugins or postfwd3.2.02.plugins)
		- --file: rule files (postfwd2.cfg)
- Postfix Configuration
	- main.cf
		- smtpd_recipient_restrictions = check_policy_service inet:127.0.0.1:{postfwd_srvport}

# Example
- Rule file
	- access control rules
	- postfwd2.cfg
- Plugin file
	- create an object to record SourceIP and Sender at once
	- postfwd2.1.35.plugins
	- postfwd3.2.02.plugins
