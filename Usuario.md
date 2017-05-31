Usuario API Reference
====================

Usuario
====
Representa los Usuarios.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Usuario/:id | Obtiene un Usuario por ID. |
| get | GET | /Usuario/IPS/:id | Obtiene una lista de Usuarios por IPS. |
| create | POST | /Usuario/ | Ingresar un nuevo Usuario. |
| delete | DELETE | /Usuario/:id | Elimina un Usuario Existente. |
| update | PUT | /Usuario/:name | Actualiza un Usuario Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "user_name": "sogud007",
  "pass": "Pass123",
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
  "ips": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
          "name": "Sura",
          "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                        "name": "Calle 2 # 37 - 124",
                        "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                            "name": "Cali",
                          "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                              "name": "Valle"}
                          },
                        "created": "timestamp",
                        "update": "timestamp"}},
  "created": "timestamp",
  "update": "timestamp"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Usuario`
--------------------------------------------

Crear un nuevo Usuario.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "user_name": "sogud007",
        "pass": "Pass123",
        "datos": {"name": "Gustavo",
                  "name2": "Andres",
                  "last_name": "Salazar",
                  "last_name2": "Garzon",
                  "genero": "Masculino",
                  "fecha": "10/10/1900",
                  "email": "sogud007@gmail.com",
                  "documento": {"numero": "1010205201",
                                "tipoDocumento": {"name": "Tarjeta_Identidad"}}},
        "ips": {"name": "Sura",
                "direccion": {"name": "Calle 2 # 37 - 124",
                              "municipio": {"name": "Cali",
                                            "departamento": {"name": "Valle"}}}}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Usuario'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Usuario/:id`
----------------------------------------------

Obtener un Usuario.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Usuario/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "user_name": "sogud007",
  "pass": "Pass123",
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
  "ips": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
          "name": "Sura",
          "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                        "name": "Calle 2 # 37 - 124",
                        "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                            "name": "Cali",
                          "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                              "name": "Valle"}
                          },
                        "created": "timestamp",
                        "update": "timestamp"}},
  "created": "timestamp",
  "update": "timestamp"
}
```

`GET /api/proyectoArquitectura/Usuario/IPS/:id`
----------------------------------------------

Obtiene una lista de Usuarios por IPS.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Usuario'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Usuarios": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "user_name": "sogud007",
      "pass": "Pass123",
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
      "ips": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
              "name": "Sura",
              "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                            "name": "Calle 2 # 37 - 124",
                            "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                                "name": "Cali",
                              "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                                  "name": "Valle"}
                              },
                            "created": "timestamp",
                            "update": "timestamp"}},
      "created": "timestamp",
      "update": "timestamp"
    },
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "user_name": "leo123",
      "pass": "Pass123",
      "datos": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                "name": "Jose",
                "name2": "Leonardo",
                "last_name": "Alfonso",
                "last_name2": "Garzon",
                "genero": "Masculino",
                "fecha": "10/10/1900",
                "email": "leo123@gmail.com",
                "documento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                              "numero": "1010205201",
                              "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", 
                                                "name": "Tarjeta_Identidad"},
                              "created": "timestamp",
                              "update": "timestamp"},
                "created": "timestamp",
                "update": "timestamp"},
      "ips": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
              "name": "Sura",
              "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                            "name": "Calle 2 # 37 - 124",
                            "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                                "name": "Cali",
                              "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                                  "name": "Valle"}
                              },
                            "created": "timestamp",
                            "update": "timestamp"}},
      "created": "timestamp",
      "update": "timestamp"
    },
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "user_name": "user123",
      "pass": "Pass123",
      "datos": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                "name": "User",
                "name2": "Test",
                "last_name": "Last_Name",
                "last_name2": "Last_Name2",
                "genero": "Masculino",
                "fecha": "10/10/1900",
                "email": "user123@gmail.com",
                "documento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                              "numero": "1010205201",
                              "tipoDocumento": {"id": "a379f19c-8c8b-11e5-8994-feff819cdc9f", 
                                                "name": "Tarjeta_Identidad"},
                              "created": "timestamp",
                              "update": "timestamp"},
                "created": "timestamp",
                "update": "timestamp"},
      "ips": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
              "name": "Sura",
              "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                            "name": "Calle 2 # 37 - 124",
                            "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                                "name": "Cali",
                              "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                                  "name": "Valle"}
                              },
                            "created": "timestamp",
                            "update": "timestamp"}},
      "created": "timestamp",
      "update": "timestamp"
    }
}
```

`DELETE /api/proyectoArquitectura/Usuario/:id`
----------------------------------------------
Eliminar un Usuario Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Usuario/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Usuario/:id`
----------------------------------------------

Actualiza un Usuario Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{
        "user_name": "sogud007",
        "pass": "Pass123",
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Usuario/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
