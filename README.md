# server
This repo contains the docker containers that i'm hosting on my server, with volume over NFS. Each stack has a bash script to define every necessary env variable needed.

### Common Variables
- NFS_ADDRESS = address of nfs server
- NFS_PATH = base path of the share - will be followed by stack name and volume name as subfolders

## Stacks
### HA-Sidecar
Stuff needed to support my home-assistant os instance (running on separate vm).

#### db (postgres:latest)
Postgres-latest running on port 5433, data on db_data

- POSTGRES_PASSWORD = defaults to postgres