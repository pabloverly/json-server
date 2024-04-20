# START SEM INTERACAO MANUAL
"start": "json-server --watch ./barbearia-db.json",
 

# START COM INTERACAO AUTOMATIZADA
  "start-auth": "node server.js"

# METOD

## SELECT
GET http://localhost:3000/products/
HEADER Authorization: Bearer codigo

## SELECT FILTER
GET http://localhost:3000/products?id=1
HEADER Authorization: Bearer codigo

## PAGINACAO
GET http://localhost:3000/products?_page=1
HEADER Authorization: Bearer codigo

## CREATE USER
POST http://localhost:3000/auth/register
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
HEADER Authorization: Bearer codigo

## PATCH
PUT http://localhost:3000/users/1
BODY JSON
{
  "password":"12345678"
}
HEADER Authorization: Bearer codigo

# DELETE
DELETE http://localhost:3000/users/2
HEADER Authorization: Bearer codigo

# LOGIN - TOKEN JWT (SOMENTO MENTODO AUTOMATIZADO NPM RUN START-AUTH)
POST http://localhost:3000/auth/login
BODY JSON
{
  "email": "pverly@redegazeta.com.br",
  "password":"123456"
}



@ref
https://www.techiediaries.com/fake-api-jwt-json-server/
https://www.youtube.com/watch?v=iNps8SBv-1A
