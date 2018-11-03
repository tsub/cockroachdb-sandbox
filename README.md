# cockroachdb-sandbox

https://www.cockroachlabs.com/docs/stable/build-a-go-app-with-cockroachdb-gorm.html#step-2-create-the-maxroach-user-and-bank-database

## Setup

```
$ docker-compose up -d
$ docker exec cockroachdb_master ./cockroach sql --insecure

> CREATE USER IF NOT EXISTS maxroach;
> CREATE DATABASE bank;
> GRANT ALL ON DATABASE bank TO maxroach;
> \q

$ GO111MODULE=on go run main.go
```
