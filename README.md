Run the project
```sh
docker compose up --build
```

Run e2e Playright tests
```sh
docker compose run --rm --entrypoint=npx e2e-tests playwright test
```

Access the database
```sh
docker exec -it postgresql_database psql -U username database
psql (17.0 (Debian 17.0-1.pgdg120+1))
Type "help" for help.

database=# \dt
Did not find any relations.
database=# \quit
```
