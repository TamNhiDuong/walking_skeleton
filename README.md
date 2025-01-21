RUN THE CONTAINER
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

RUN MANUTALLY
Run the Deno Server-side 
```sh
deno run --allow-env --allow-net --unstable --watch app-run.js
```

Run the Svelte Client-side
```sh
deno install --allow-scripts
deno run dev --open
```

Create and run e2e test manually
```sh
deno run -A npm:create-playwright@latest e2e-tests
```
