fetchmail
=========

install fetchmail and creates a simple fetchmailrc file.

Requirements
------------

None.

Role Variables
--------------

    fetchmail_user: fetchmailrc will be installed for this user
    fetchmail_smtphost: send mail to this host
    fetchmail_polls: list of hosts to poll for new messages. See defaults/main.yml for an example

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: fetchmail
           fetchmail_user: foobar
           fetchmail_smtphost: localhost/25
           fetchmail_polls:
              - name: example.com
                server: host.example.com
                protocol: 'pop3'
                username: 'foobar'
                password: 'secret'
                mail: 'foobar@example.com'
                sslproto: 'TLS1'

License
-------

MIT

Author Information
------------------

Stefan Jakobs <project at localside.net>
