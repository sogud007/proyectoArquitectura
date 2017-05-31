Departamento API Reference
====================

Departamento
====
Representa los Departamentos.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Departamento/:name | Obtiene un Departamento por ID. |
| list | GET | /Departamento | Obtiene una lista de Departamentos. |
| create | POST | /Departamento/ | Ingresar un nuevo Departamento. |
| delete | DELETE | /Departamento/:name | Elimina un Departamento Existente. |
| update | PUT | /Departamento/:name | Actualiza un Departamento Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Valle"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Departamento`
--------------------------------------------

Crear un nuevo Departamento.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Valle"
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Departamento'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Departamento/:name`
----------------------------------------------

Obtener un Departamento.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Departamento/Valle'
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

`GET /api/proyectoArquitectura/Departamento/`
----------------------------------------------

Obtener todos los Departamentos.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Departamento'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Departamentos": [
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

`DELETE /api/proyectoArquitectura/Departamento/:name`
----------------------------------------------
Eliminar un Departamento Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Departamento/Antioquia'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Departamento/:name`
----------------------------------------------

Actualiza un Departamento Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{"name": "Valle_del_Cauca"}' \
   'http://localhost:8080/api/proyectoArquitectura/Departamento/Valle'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
