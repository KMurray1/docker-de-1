# docker-de-1

Sign up for Docker Hub

Postgres

```docker run --name first-postgres -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres```

check it is up and running

```docker ps```

Getting pgadmin4

```docker pull dpage/pgadmin4```

Running pgadmin

```docker run --name pgadmin-container -p 5050:80 -e PGADMIN_DEFAULT_EMAIL=<email@domain.com> -e PGADMIN_DEFAULT_PASSWORD=<password> -d dpage/pgadmin4 ```

Finding the ip of postgres server

```docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' first-postgres```

Now able to connect to server in pgadmin4 
Use ip obtained in prior step and password from set up command
