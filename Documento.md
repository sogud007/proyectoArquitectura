Documento API Reference
====================

Documento
====
Representa los Tipos de Documentos.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Documento/:numero | Obtiene un Documento por ID. |
| list | GET | /Documento | Obtiene una lista de Documentos. |
| create | POST | /Documento/ | Ingresar un nuevo Documento. |
| delete | DELETE | /Documento/:numero | Elimina un Documento Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "numero": "1010205201",
  "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name": "Tarjeta_Identidad"},
  "created": "timestamp",
  "update": "timestamp"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Documento`
--------------------------------------------

Crear un nuevo Documento.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "numero": "1010205201",
        "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name": "Tarjeta_Identidad"}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Documento'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Documento/:numero`
----------------------------------------------

Obtener un Documento.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Documento/1010205201'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "numero": "1010205201",
  "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name": "Tarjeta_Identidad"},
  "created": "timestamp",
  "update": "timestamp"
}
```

`GET /api/proyectoArquitectura/Documento/`
----------------------------------------------

Obtener todos los Documentos.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Documento'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Documentos": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "numero": "1010205201",
      "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name": "Tarjeta_Identidad"},
      "created": "timestamp",
      "update": "timestamp"
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "numero": "152404511",
      "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name": "Tarjeta_Identidad"},
      "created": "timestamp",
      "update": "timestamp"
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "numero": "101025421",
      "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", "name": "Cedula_Ciudadania"},
      "created": "timestamp",
      "update": "timestamp"
    }
}
```

`DELETE /api/proyectoArquitectura/Documento/:numero`
----------------------------------------------
Eliminar un Documento Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Documento/101025421'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```
