Ansible Role: Sophon
===

Ansible role for Sophon, you could use this Ansible role to deploy Sophon.

Role Variables
---

Available variables are listed below, along with default values (see `defaults/main.yml`):

```
local_public_key_directory_path: "/tmp"
    
remote_public_key_directory_path: "/tmp"
    
public_key_filename: "test_key.pub"
```

You could define the directory where you the placed public key in local or remote hosts by using these variables.

```
admin_username: "admin"

admin_password: "admin"
```

You could use these two variables to set the default account for Sophon, it's only work when it's the first time that you deployed on specific hosts.


```
nginx_listen: "80 default_server"
```

This variables help you define `listen` field in the configuration of Nginx. You could visit your Sophon on this port of host.


```
cookie_secret: ".wwwpsgx.ktsy.o].b[jrdexye[bumys"
```

You could change the cookie secret in Sophon by using this variable.


Requirements
---

None

Dependencies
---

None

Example Playbook
---

```
---
- hosts: 123.123.123.123 # Input your host here
  user: sophon # Input your user here
  roles:
    - { role: ansible-role-sophon, local_public_key_directory_path: "/home/localsophon/.ssh", remote_public_key_directory_path: "/home/sophon/.ssh", public_key_filename: "test_key.pub", cookie_secret: "dasdafnskvnjsk1239j*&Y$#sdq" }
```

License
---

MIT
