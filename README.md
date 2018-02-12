Ansible Role - Languagetool
=========

Installs Java and LanguageTool. <https://github.com/languagetool-org/languagetool>

Requirements
------------

None.

Role Variables
--------------

```yaml
languagetool_server_password: my-password
languagetool_server_maxTextLength: 50000
languagetool_server_maxCheckThreads: 10
```

Dependencies
------------

`geerlingguy.java` <https://github.com/geerlingguy/ansible-role-java>

Example Playbook
----------------

```yaml
---
- hosts: web
  become: yes
  user: ubuntu
  roles:
    - geerlingguy.java
    - role: postedin.languagetool
      languagetool_server_maxCheckThreads: 32
```

License
-------

MIT

Author Information
------------------

This role was created by [Postedin SpA](https://postedin.com).
