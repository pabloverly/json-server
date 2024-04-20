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
PUT http://localhost:3000/products/1
BODY JSON
	{
		"id": 1,
		"name": "Product00s1",
		"cost": 10,
		"quantity": 1000,
		"locationId": 1,
		"familyId": 1
	}
HEADER Authorization: Bearer codigo

## PATCH
PUT http://localhost:3000/products/1
BODY JSON
	{
		"name": "Product00ss1"
	}
HEADER Authorization: Bearer codigo

# DELETE
DELETE http://localhost:3000/products/18
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
