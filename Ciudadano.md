Ciudadano API Reference
====================

Ciudadano
====
Representa los Ciudadanos.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Ciudadano/:id | Obtiene un Ciudadano por ID. |
| get | GET | /Ciudadano/Responsable/:id | Obtiene una lista de Ciudadanos a Cargo de un Responsable. |
| create | POST | /Ciudadano/ | Ingresar un nuevo Ciudadano. |
| delete | DELETE | /Ciudadano/:id | Elimina un Ciudadano Existente. |
| update | PUT | /Ciudadano/:id | Actualiza un Ciudadano Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "registro_civil": "89895553-5",
  "registro_nacimiento": "448798266",
  "peso": "4850"
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
   "responsable": {
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
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Ciudadano`
--------------------------------------------

Crear un nuevo Ciudadano.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "registro_civil": "89895553-5",
        "registro_nacimiento": "448798266",
        "peso": "4850"
        "datos": {"name": "Gustavo",
                  "name2": "Andres",
                  "last_name": "Salazar",
                  "last_name2": "Garzon",
                  "genero": "Masculino",
                  "fecha": "10/10/1900",
                  "email": "sogud007@gmail.com",
                  "documento": {"numero": "1010205201",
                                "tipoDocumento": {"name": "Tarjeta_Identidad"}}},
         "responsable": {
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
                        }
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Ciudadano'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Ciudadano/:id`
----------------------------------------------

Obtener un Ciudadano.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Ciudadano/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "registro_civil": "89895553-5",
  "registro_nacimiento": "448798266",
  "peso": "4850"
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
   "responsable": {
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
}
```

`GET /api/proyectoArquitectura/Ciudadano/Responsable/:id`
----------------------------------------------

Obtiene una lista de Ciudadanos a Cargo de un Responsable.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Ciudadano/Responsable/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Ciudadanos": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "registro_civil": "89895553-5",
      "registro_nacimiento": "448798266",
      "peso": "4850"
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
       "responsable": {
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
    },
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "registro_civil": "89895553-5",
      "registro_nacimiento": "448798266",
      "peso": "4850"
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
       "responsable": {
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
    },
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "registro_civil": "89895553-5",
      "registro_nacimiento": "448798266",
      "peso": "4850"
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
       "responsable": {
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
    }
}
```

`DELETE /api/proyectoArquitectura/Ciudadano/:id`
----------------------------------------------
Eliminar un Ciudadano Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Ciudadano/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Ciudadano/:id`
----------------------------------------------

Actualiza un Ciudadano Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{"name": "Valle_del_Cauca"}' \
   'http://localhost:8080/api/proyectoArquitectura/Ciudadano/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
