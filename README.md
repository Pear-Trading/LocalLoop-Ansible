# Local Loop Ansible Config

this is the Ansible config for setting up the Local Loop on a server. Note this
is designed for Debian based distributions at present.

# Required Variables

The following are required variables - to be supplied by either a vars file or
using Tower/AWX.

```yaml
local_loop:
  runtime_user: runtime user
  perl_version: 5.26.3
  server_branch: master
  db:
    user: username
    password: password
    name: database name
```

# Groups

The following groups are used in these playbooks:

* all
* db