# go-rest-api

This repo contains a simple/basic HTTP server in Go, with a basic code organization.
We use:

- net/http package to start and serve HTTP server
- Gorilla mux to handle routes
- Swagger in order to serve a REST API compliant with OpenAPI specs

## Pre-requisits

Install Go in 1.16 version minimum.

## Build the app

`$ go build -o bin/go-rest-api internal/main.go`

or

`$ task build`

## Run the app

`$ ./bin/go-rest-api`

or

`$ task run`

## Test the app

```
 http://localhost:8080/healthz


 http://localhost:8080/hello/John
"Hello John!"

 localhost:8080/gopher/dr-who

```

### Request & Response Examples

Swagger doc: [go-rest-api](https://github.com/shadkhan/golang-projects/blob/main/go-rest-api/doc/index.html)

## Generate swagger files

After editing `pkg/swagger/swagger.yml` file you need to generate swagger files again:

`$ task swagger.gen`

## Test swagger file validity

`$ task swagger.validate`

## Generate swagger documentation

`$ task swagger.doc`
