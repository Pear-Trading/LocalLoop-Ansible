# Local Loop Ansible Config

this is the ansible config for setting up the Local Loop on a server.

# DB Config

Database configuration should be stored in a file referenced by the `LOCAL_LOOP_DB_CONFIG` environment variable. The contents of this file should be:

```
db_name: <some database name>
db_user: <some database user>
db_pass: <some database pass>
```
