IPS API Reference
====================

IPS
====
Representa las IPSs.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /IPS/:name | Obtiene una IPS por nombre. |
| list | GET | /IPS | Obtiene una lista de IPSs. |
| create | POST | /IPS/ | Ingresar una nueva IPS. |
| delete | DELETE | /IPS/:name | Elimina una IPS Existente. |
| update | PUT | /IPS/:name | Actualiza una IPS Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Sura",
  "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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

`POST /api/proyectoArquitectura/IPS`
--------------------------------------------

Crea una nueva IPS.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Sura",
        "direccion": {  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                        "name": "Calle 2 # 37 - 124",
                        "municipio": {"name": "Cali",
                                      "departamento": {"name": "Valle"}
                          }}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/IPS'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/IPS/:name`
----------------------------------------------

Obtener una IPS.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/IPS/Sura'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Valle",
  "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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

`GET /api/proyectoArquitectura/IPS/`
----------------------------------------------

Obtener todas las IPSs.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/IPS'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "IPSs": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Sura",
      "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                    "name": "Calle 2 # 37 - 124",
                    "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                        "name": "Cali",
                      "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                          "name": "Valle"}
                      },
                    "created": "timestamp",
                    "update": "timestamp"}
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Sanitas",
      "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                    "name": "Calle 10 # 10 - 34",
                    "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                        "name": "Cali",
                      "departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
                          "name": "Valle"}
                      },
                    "created": "timestamp",
                    "update": "timestamp"}
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Nueva EPS",
      "direccion": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                    "name": "Carera 20 # 37 - 14",
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

`DELETE /api/proyectoArquitectura/IPS/:name`
----------------------------------------------
Elimina una IPS Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/IPS/Sanitas'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/IPS/:name`
----------------------------------------------

Actualiza una IPS Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{ "name": "Sanitas",
        "direccion": {"name": "Calle 10 # 10 - 34",
                      "municipio": {"name": "Cali",
                        "departamento": {"name": "Valle"}}}
    }' \
   'http://localhost:8080/api/proyectoArquitectura/IPS/Sanitas'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
