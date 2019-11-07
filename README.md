# password-cockpit

## Environment variables for configuring your passwordcockpit instance
- PASSWORDCOCKPIT_DATABASE_USERNAME: Username for the database
- PASSWORDCOCKPIT_DATABASE_PASSWORD: Password for the database
- PASSWORDCOCKPIT_DATABASE_HOSTNAME: Hostname of the database server
- PASSWORDCOCKPIT_DATABASE_DATABASE: Name of the database
- PASSWORDCOCKPIT_BLOCK_CIPHER_KEY: Key for passwords and files encrypting, e.g. `passwordcockpit.domain.com`
- PASSWORDCOCKPIT_AUTHENTICATION_SECRET_KEY: Key for JWT, e.g. `passwordcockpit.domain.com`
- PASSWORDCOCKPIT_BASEHOST: Base host of the passwordcockpit service, e.g. `passwordcockpit.domain.com`
- PASSWORDCOCKPIT_AUTHENTICATION_TYPE: Type of the authentication, possible value: `ldap` or `password`
	- Only for LDAP type:
		- PASSWORDCOCKPIT_LDAP_HOST: Hostname of the LDAP server
		- PASSWORDCOCKPIT_LDAP_PORT: Port of the LDAP server
		- PASSWORDCOCKPIT_LDAP_USERNAME: Username for LDAP, e.g. `uid=name,cn=users,dc=domain,dc=com`
		- PASSWORDCOCKPIT_LDAP_PASSWORD: Password for LDAP
		- PASSWORDCOCKPIT_LDAP_BASEDN: Base DN, e.g. `cn=users,dc=domain,dc=com`
		- PASSWORDCOCKPIT_LDAP_ACCOUNTFILTERFORMAT: Filter for retrieving accounts, e.g. `(&(memberOf=cn=group_name,cn=groups,dc=domain,dc=com)(uid=%s))`
		- PASSWORDCOCKPIT_LDAP_BINDREQUIRESDN: Bind requires DN, possible value: `true` or `false`