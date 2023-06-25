# <first time only> docker image push
```shell
docker login
docker compose build
docker compose push
```

# Create
```shell
fly pg create --image-ref skkzsh/fly-pgvector

fly pg ls

# fly config save --app <pg-app-name>
```

# Enable PGVector
```shell
fly pg connect [-a <pg-app-name>]

create extension vector;
select * from pg_extension;
```

# Connect from external 
```shell
fly ips ls [-a <pg-app-name>]
fly services ls [-a <pg-app-name>]
fly ips allocate-v6 [-a <pg-app-name>]
fly ips ls [-a <pg-app-name>]
fly services ls [-a <pg-app-name>]

pgcli -h <pg-app-name>.fly.dev 
```

# See also
- https://github.com/pgvector/pgvector/blob/master/Dockerfile
- https://github.com/fly-apps/postgres-flex
- https://github.com/fly-apps/postgres-ha
- https://community.fly.io/t/adding-pgvector-to-fly-postgres/12202
