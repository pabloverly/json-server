# START SEM INTERACAO MANUAL
"start": "json-server --watch ./barbearia-db.json",
 

# START COM INTERACAO AUTOMATIZADA
  "start-auth": "node server.js"

# METOD

## SELECT
GET http://localhost:3000/users


## SELECT FILTER
GET http://localhost:3000/users

## PAGINACAO
GET http://localhost:3000/users?_page=1


## CREATE USER
POST http://localhost:3000/users
BODY JSON
{
  "email": "pverly@redegazeta.com.br",
  "password":"pverly"
}

## UPDATE
PUT http://localhost:3000/users/1
BODY JSON
{
  "email": "pverly@redegazeta.com.br",
  "password":"1234"
}

## PATCH
PUT http://localhost:3000/users/1
BODY JSON
{
  "password":"12345678"
}

# DELETE
DELETE http://localhost:3000/users/2

# LOGIN - TOKEN JWT (SOMENTO MENTODO AUTOMATIZADO NPM RUN START-AUTH)
POST http://localhost:3000/auth/login


@ref
https://www.techiediaries.com/fake-api-jwt-json-server/
https://www.youtube.com/watch?v=iNps8SBv-1A