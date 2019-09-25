# Local Loop Ansible Config

this is the Ansible config for setting up the Local Loop on a server. Note this
is designed for Debian based distributions at present.

# Required Variables

The following are required variables - to be supplied by either a vars file or
using Tower/AWX.

```yaml
local_loop:
  runtime_user: runtime user
  runtime_group: runtime group
  perl_version: 5.26.3
  server_branch: master
  db:
    user: username
    password: password
    name: database name
    host: db host
    port: db port
  minion_db:
    user: username
    password: password
    name: database name
    host: db host
    port: db port
  paths:
    # These should all be absolute paths
    root: /path/to/application/root
    storage: /path/to/storage/dir
    upload: /path/to/upload/dir
  api_keys:
    google_maps: api key
  mojo:
    # optional - application generates random one on boot otherwise
    secret: secret string here
```

# Groups

The following groups are used in these playbooks:

* all
* db
* web

# Maintenance notes

We are using pipelining where possible - this means that template, copy, and
 fetch 