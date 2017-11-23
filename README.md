ansible-role-changeonly
======================

Install ansible-changeonly

```
# Remove skipped lines from ansible output
# Do only print plays and tasks with changes
#
# To see colors, use:
# export ANSIBLE_FORCE_COLOR=true
#
# To see warnings:
# ansible-playbook site.yml 2>&1 | ansible-changeonly
#
# If you don't want to see warning:
# ansible-playbook site.yml 2>/dev/null | ansible-changeonly
#
# Mail all potential problems to root:
# ansible-playbook site.yml --check 2>&1 | ansible-changeonly | mail -E -s "Ansible not idempotent" root
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: t2d.changeonly, x: 42 }

License
-------

GPLv3

