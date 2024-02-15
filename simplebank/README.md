# Simple bank app

##  backend web development: Golang, Postgres, Redis, Gin, gRPC, Docker, Kubernetes, AWS, CI/CD

### Description
In this course, you'll gain practical experience with a variety of backend web development tools and practices:

- Designing a database schema and working with transactions to ensure consistent interactions with the database.
- Understanding and applying database isolation levels to prevent data anomalies and maintain data integrity.
- Developing RESTful backend services using the Gin framework to handle HTTP requests and responses.
- Implementing user authentication and securing API endpoints using JWT (JSON Web Tokens) and PASETO tokens.
- Writing comprehensive tests with high coverage, utilizing interfaces and mocking techniques for more robust testing.
- Creating minimal Docker images for deployment, using Docker-compose for development, and orchestrating these containers in a production environment with Kubernetes.
- Automating the build and deployment pipeline using GitHub Actions for continuous integration and deployment to an AWS Kubernetes cluster.
- Setting up domain registration and configuring Kubernetes ingress to direct traffic to your service.
- Enabling and automating TLS certificate issuance and renewal with Let's Encrypt for secure communications.
- Advancing your backend skills with gRPC for efficient API development and utilizing a gRPC gateway to serve both gRPC and HTTP requests concurrently.
- Processing tasks asynchronously using Redis and Asynq, which can help run background workers for various asynchronous operations.

## utils commands
### https://github.com/golang-migrate/migrate/tree/master/cmd/migrate
- `migrate create -ext sql -dir db/migration -seq init_schema`

### Run postgres12 container
- `docker start postgres12`
  
### Acces to shell container
- `docker exec -it postgres12 /bin/sh` 

### Create database from shell console
- `createdb --username=root --owner=root simple_bank`

### Acces to sql command line from shell console
- `psql simple_bank`

### exit psql shell
- `\q`
  
### delete db from shell 
- `dropdb simple_bank`

### Create database from docker command line
- `docker exec -it postgres12 createdb --username=root --owner=root simple_bank`

### Acces from docker command line to the db
- `docker exec -it postgres12 psql -U root simple_bank`

### Migreate db from db/migration folder
- `migrate -path db/migration -database "postgresql://root:secret@localhost:5432/simple_bank?sslmode=disable" -verbose up`