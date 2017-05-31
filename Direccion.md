Direccion API Reference
====================

Direccion
====
Representa las Direcciones.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Direccion/:name | Obtiene un Direccion por ID. |
| list | GET | /Direccion | Obtiene una lista de Direcciones. |
| create | POST | /Direccion/ | Ingresar un nuevo Direccion. |
| delete | DELETE | /Direccion/:name | Elimina un Direccion Existente. |
| update | PUT | /Direccion/:name | Actualiza un Direccion Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Calle 2 # 37 - 124",
  "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name": "Cali", "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name": "Valle"}},
  "created": "timestamp",
  "update": "timestamp"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Direccion`
--------------------------------------------

Crear un nuevo Direccion.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Valle"
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Direccion'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Direccion/:name`
----------------------------------------------

Obtener un Direccion.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Direccion/Valle'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Valle"
}
```

`GET /api/proyectoArquitectura/Direccion/`
----------------------------------------------

Obtener todos los Direccions.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Direccion'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Direccions": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Valle"
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Antioquia"
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Cundinamarca"
    }
}
```

`DELETE /api/proyectoArquitectura/Direccion/:name`
----------------------------------------------
Eliminar un Direccion Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Direccion/Antioquia'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Direccion/:name`
----------------------------------------------

Actualiza un Direccion Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{"name": "Valle_del_Cauca"}' \
   'http://localhost:8080/api/proyectoArquitectura/Direccion/Valle'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
