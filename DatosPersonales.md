Datos Personales API Reference
====================

Datos Personales
====
Representa los Datos Personales.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /DatosPersonales/:id | Obtiene los Datos Personales por ID. |
| create | POST | /DatosPersonales/ | Ingresar un nuevo registro de Datos Personales. |
| delete | DELETE | /DatosPersonales/:id | Elimina un registro de Datos Personales Existente. |
| update | PUT | /DatosPersonales/:id | Actualiza un registro de Datos Personales Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Gustavo",
  "name2": "Andres",
  "last_name": "Salazar",
  "last_name2": "Garzon",
  "genero": "Masculino",
  "fecha": "10/10/1900",
  "email": "sogud007@gmail.com",
  "documento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                "numero": "1010205201",
                "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", 
                                  "name": "Tarjeta_Identidad"},
                "created": "timestamp",
                "update": "timestamp"},
  "created": "timestamp",
  "update": "timestamp"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/DatosPersonales`
--------------------------------------------

Crear un nuevo registro de Datos Personales.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Gustavo",
        "name2": "Andres",
        "last_name": "Salazar",
        "last_name2": "Garzon",
        "genero": "Masculino",
        "fecha": "10/10/1900",
        "email": "sogud007@gmail.com",
        "documento": {"numero": "1010205201",
                      "tipoDocumento": {"name": "Tarjeta_Identidad"}}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/DatosPersonales'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/DatosPersonales/:id`
----------------------------------------------

Obtener un registro de Datos Personales por ID.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/DatosPersonales/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Gustavo",
  "name2": "Andres",
  "last_name": "Salazar",
  "last_name2": "Garzon",
  "genero": "Masculino",
  "fecha": "10/10/1900",
  "email": "sogud007@gmail.com",
  "documento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                "numero": "1010205201",
                "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", 
                                  "name": "Tarjeta_Identidad"},
                "created": "timestamp",
                "update": "timestamp"},
  "created": "timestamp",
  "update": "timestamp"
}
```

`DELETE /api/proyectoArquitectura/DatosPersonales/:id`
----------------------------------------------
Eliminar un registro de Datos Personales Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/DatosPersonales/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/DatosPersonales/:id`
----------------------------------------------

Actualiza un registro de Datos Personales Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{ "name": "Gustavo",
        "name2": "Andres",
        "last_name": "Salazar",
        "last_name2": "Garzon",
        "genero": "Masculino",
        "fecha": "10/10/1900",
        "email": "sogud007@gmail.com",
        "documento": {"numero": "1010205201",
                      "tipoDocumento": {"name": "Tarjeta_Identidad"}}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/DatosPersonales/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
