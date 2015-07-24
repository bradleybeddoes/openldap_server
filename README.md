An OpenLDAP server installation for CentOS 7 using Ansible. This is **only** good for local development VM.

Adds 8 user accounts, under `ou=people,dc=example,dc=edu` all passwords are `password`.

I generally make use of this when working with a Shibboleth IdP though it might be useful in other scenarios as well.

Forked from the good work originally found at [https://github.com/bennojoy/openldap_server](https://github.com/bennojoy/openldap_server).

## Config
Simply copy `ansible_hosts.dist` to `ansible_hosts` and edit with your development VM IP/Hostname. You should be able to ssh to this location as root.

## Running
`ansible-playbook -i ansible_hosts site.yml`

Idempotent? Nope. Rollback point recommended.

## License
BSD

## Author
[Bradley Beddoes](https://github.com/bradleybeddoes), based on work by [Benno Joy](https://github.com/bennojoy)
