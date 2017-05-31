Municipio API Reference
====================

Municipio
====
Representa los Municipios.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Municipio/:name | Obtiene un Municipio por ID. |
| list | GET | /Municipio | Obtiene una lista de Municipios. |
| get | GET | /Municipio/Departamento/:name | Obtiene una lista de Municipios por nombre de Departamento. |
| create | POST | /Municipio/ | Ingresar un nuevo Municipio. |
| delete | DELETE | /Municipio/:name | Elimina un Municipio Existente. |
| update | PUT | /Municipio/:name | Actualiza un Municipio Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Cali",
  "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name"; "Valle"}
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Municipio`
--------------------------------------------

Crear un nuevo Municipio.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Cali",
        "departamento": {"name"; "Valle"}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Municipio'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Municipio/:name`
----------------------------------------------

Obtener un Municipio.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Municipio/Cali'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Cali",
  "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name"; "Valle"}
}
```

`GET /api/proyectoArquitectura/Municipio/`
----------------------------------------------

Obtener todos los Municipios.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Municipio'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Municipios": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Cali",
      "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name"; "Valle"}
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Medellin",
      "departamento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name"; "Antioquia"}
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Bogota",
      "departamento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name"; "Cundinamarca"}
    }
}
```

`GET /api/proyectoArquitectura/Municipio/Departamento/:name`
----------------------------------------------

Obtener todos los Municipios de un Departamento

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Municipio/Departamento/Valle'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Municipios": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Cali",
      "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name"; "Valle"}
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Palmira",
      "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name"; "Valle"}
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Buga",
      "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", "name"; "Valle"}
    }
}
```

`DELETE /api/proyectoArquitectura/Municipio/:name`
----------------------------------------------
Eliminar un Municipio Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Municipio/Medellin'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Municipio/:name`
----------------------------------------------

Actualiza un Municipio Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{"name": "Santiago_de_Cali"}' \
   'http://localhost:8080/api/proyectoArquitectura/Municipio/Cali'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
