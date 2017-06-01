Vacuna API Reference
====================

Vacuna
====
Representa las Vacunas.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Vacuna/:id | Obtiene una Vacuna por ID. |
| list | GET | /Vacuna/:name | Obtiene una lista de Vacunas por nombre. |
| list | GET | /Vacuna/:laboratorio | Obtiene una lista de Vacunas por Laboratorio. |
| create | POST | /Vacuna/ | Ingresar un nuevo Vacuna. |
| delete | DELETE | /Vacuna/:id | Elimina un Vacuna Existente. |
| update | PUT | /Vacuna/:id | Actualiza un Vacuna Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Viruela",
  "laboratorio": "Pfizer"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Vacuna`
--------------------------------------------

Crear un nuevo Vacuna.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Viruela",
        "laboratorio": "Pfizer"
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Vacuna'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Vacuna/:id`
----------------------------------------------

Obtener un Vacuna por ID.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Vacuna/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Viruela",
  "laboratorio": "Pfizer"
}
```

`GET /api/proyectoArquitectura/Vacuna/:name`
----------------------------------------------

Obtiene una lista de Vacunas por nombre.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Vacuna/Viruela'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Vacunas": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Viruela",
      "laboratorio": "Pfizer"
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Viruela",
      "laboratorio": "Wyeth"
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Viruela",
      "laboratorio": "Sanofi"
    }
}
```

`GET /api/proyectoArquitectura/Vacuna/:laboratorio`
----------------------------------------------

Obtiene una lista de Vacunas por Laboratorio.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Pfizer'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Vacunas": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Viruela",
      "laboratorio": "Pfizer"
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Tétano",
      "laboratorio": "Pfizer"
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Sarampión",
      "laboratorio": "Pfizer"
    }
}
```

`DELETE /api/proyectoArquitectura/Vacuna/:id`
----------------------------------------------
Eliminar un Vacuna Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Vacuna/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Vacuna/:id`
----------------------------------------------

Actualiza un Vacuna Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{
        "name": "Paperas",
        "laboratorio": "Pfizer"
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Vacuna/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
