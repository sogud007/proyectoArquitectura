Responsable API Reference
====================

Responsable
====
Representa los Responsables.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Responsable/:id | Obtiene una Responsable por ID. |
| create | POST | /Responsable/ | Ingresar un nuevo Responsable. |
| delete | DELETE | /Responsable/:id | Elimina un Responsable Existente. |
| update | PUT | /Responsable/:id | Actualiza un Responsable Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "datos": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
            "update": "timestamp"},
   "direccion": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                  "name": "Calle 2 # 37 - 124",
                  "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                      "name": "Cali", 
                    "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                        "name": "Valle"}
                    },
                  "created": "timestamp",
                  "update": "timestamp"}
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Responsable`
--------------------------------------------

Crear un nuevo Responsable.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "datos": {"name": "Gustavo",
                  "name2": "Andres",
                  "last_name": "Salazar",
                  "last_name2": "Garzon",
                  "genero": "Masculino",
                  "fecha": "10/10/1900",
                  "email": "sogud007@gmail.com",
                  "documento": {"numero": "1010205201",
                                "tipoDocumento": {"name": "Tarjeta_Identidad"}}},
         "direccion": { "name": "Calle 2 # 37 - 124",
                        "municipio": {"name": "Cali", 
                          "departamento": {"name": "Valle"}
                          }}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Responsable'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Responsable/:id`
----------------------------------------------

Obtener un Responsable.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Responsable/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "datos": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
            "update": "timestamp"},
   "direccion": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                  "name": "Calle 2 # 37 - 124",
                  "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                      "name": "Cali", 
                    "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                        "name": "Valle"}
                    },
                  "created": "timestamp",
                  "update": "timestamp"}
}
```

`DELETE /api/proyectoArquitectura/Responsable/:id`
----------------------------------------------
Eliminar un Responsable Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Responsable/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Responsable/:name`
----------------------------------------------

Actualiza un Responsable Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{
        "datos": {"name": "Gustavo",
                  "name2": "Andres",
                  "last_name": "Salazar",
                  "last_name2": "Garzon",
                  "genero": "Masculino",
                  "fecha": "10/10/1900",
                  "email": "sogud007@gmail.com",
                  "documento": {"numero": "1010205201",
                                "tipoDocumento": {"name": "Tarjeta_Identidad"}}},
         "direccion": { "name": "Calle 2 # 37 - 124",
                        "municipio": {"name": "Cali", 
                          "departamento": {"name": "Valle"}
                          }}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Responsable/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
