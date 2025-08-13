
# fjmserver

## Usage

#### Resetting Databases

To reset the Postgres database locally, first check that the volume exists by doing `docker volume ls`. There should be an entry called `fjmserver_pgdata`. To remove it, do `docker volume rm fjmserver_pgdata`. It might say it is in use, in which case do `docker compose down`.

### Development

#### Docker Building

You must run this at least once before starting:
```
docker compose -f ./compose.dev.yaml build
```

#### Starting

To start the server in development, do:
```
docker compose -f ./compose.dev.yaml up
```

You can try the website at `http://localhost:3000`.

To exit, just press `^C`. To stop daemons, do:
```
docker compose down
```

#### Accessing Database

Running the server in development will also start a Postgres database 'fjmdb_dev'. To interact with it using psql, do:
```
docker compose -f ./compose.dev.yaml exec db psql -U postgres -d fjmdb_dev
```

### Production
