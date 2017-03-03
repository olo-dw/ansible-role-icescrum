# Ansible Role Icescrum

## Prerequisites

* java 7
* Mysql
* tomcat7

## Usage

    http://<server>:8080/icescrum

Initial credentials are `admin / adminadmin!` . Do not forget to change it!

## Example Playbook

    - hosts: servers
      roles:
      - role: ansible-role-icescrum
        icescrum_appID: '726bafab-bcde-f1f2-abcd-f5e4d5c4b2a19'
        icescrum_scheme: 'https'
        icescrum_server: 'icescrum.company.com'
        icescrum_db_password: 'oloc4ever'

## Main variables

**icescrum_create_default_admin**: 'true' or 'false'. False provide a setup wizard.

**icescrum_appID**: Add server ID file named _appID.txt_

**icescrum_license_key**: Add iceScrum Pro Key.

**icescrum_scheme**: 'http' or 'https'

**icescrum_server**: Complete _grails.serverURL_ with the _\<server\>_ name to set a specific site location.

**icescrum_db_user**: 'icescrum'

**icescrum_db_password**: 'ic3scrum'

## Mail variables

To enable mail settings, turn `icescrum_mail_enable` into `True` and override with your own settings:

    icescrum_mail_enable: True
    icescrum_mail_host: "smtp.company.com"
    icescrum_mail_port: 465
    icescrum_mail_username: "username@company.com"
    icescrum_mail_password: "mypassword"
    icescrum_mail_auth: ''

**icescrum_mail_auth**: '', 'TLS', or 'SSL'

## LDAP variables

To enable LDAP configuration, put your own settings:

    icescrum_ldap_enable: True
    icescrum_ldap_server: 'ldaps://ldap.company.com:636'
    icescrum_ldap_manager_dn: 'cn=admin,dc=company,dc=com'
    icescrum_ldap_manager_password: 'ThouShallNotPass'

You can override the default settings below:

    icescrum_ldap_search_base: ''
    icescrum_ldap_search_filter: '(uid={0})'
    icescrum_ldap_search_subtree: 'true'
    icescrum_ldap_attribute_first_name: 'givenName'
    icescrum_ldap_attribute_last_name: 'sn'
    icescrum_ldap_attribute_mail: 'mail'
    icescrum_ldap_ignore_result_exception: 'false'
    icescrum_anonymous_no_connection: 'false'

## License

MIT

## Author Information

This role was created in 2016 by Olivier Locard on the behalf of Deveryware.

