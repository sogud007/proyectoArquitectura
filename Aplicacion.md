Aplicacion API Reference
====================

Aplicacion
====
Representa las Aplicaciones de las Vacunas en los Ciudadanos.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Aplicacion/:id | Obtiene una Aplicacion por ID. |
| list | GET | /Aplicacion/Ciudadano/:id | Obtiene una lista de Aplicaciones por Ciudadano. |
| create | POST | /Aplicacion/ | Ingresar un nuevo registro de Aplicacion. |
| delete | DELETE | /Aplicacion/:id | Elimina un registro de Aplicacion Existente. |
| update | PUT | /Aplicacion/:id | Actualiza un registro Aplicacion Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "edad": "12",
  "tipo_edad": "Años",
  "dosis": "1",
  "fecha_vacuna": "20/05/2017",
  "lote_vacuna": "ASPNA892AA",
  "fecha_refuerzo": "N/A",
  "vacuna": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
              "name": "Viruela",
              "laboratorio": "Pfizer"},
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

`POST /api/proyectoArquitectura/Aplicacion`
--------------------------------------------

Crear un nuevo registro de Aplicacion.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "edad": "12",
        "tipo_edad": "Años",
        "dosis": "1",
        "fecha_vacuna": "20/05/2017",
        "lote_vacuna": "ASPNA892AA",
        "fecha_refuerzo": "N/A",
        "vacuna": { "name": "Viruela",
                    "laboratorio": "Pfizer"},
        "ips": {"name": "Sura",
                "direccion": {"name": "Calle 2 # 37 - 124",
                              "municipio": {"name": "Cali",
                                "departamento": {"name": "Valle"}
                                }}}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Aplicacion'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Aplicacion/:id`
----------------------------------------------

Obtener un registro de Aplicacion por ID.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Aplicacion/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "edad": "12",
  "tipo_edad": "Años",
  "dosis": "1",
  "fecha_vacuna": "20/05/2017",
  "lote_vacuna": "ASPNA892AA",
  "fecha_refuerzo": "N/A",
  "vacuna": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
              "name": "Viruela",
              "laboratorio": "Pfizer"},
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

`GET /api/proyectoArquitectura/Aplicacion/Ciudadano/:id`
----------------------------------------------

Obtiene una lista de Aplicaciones por Ciudadano.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Aplicacion/Ciudadano/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "Aplicaciones": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "edad": "12",
      "tipo_edad": "Años",
      "dosis": "1",
      "fecha_vacuna": "20/05/2017",
      "lote_vacuna": "ASPNA892AA",
      "fecha_refuerzo": "N/A",
      "vacuna": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                  "name": "Viruela",
                  "laboratorio": "Pfizer"},
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
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "edad": "12",
      "tipo_edad": "Años",
      "dosis": "2",
      "fecha_vacuna": "20/04/2017",
      "lote_vacuna": "ASPNA891AA",
      "fecha_refuerzo": "N/A",
      "vacuna": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                  "name": "Sarampión",
                  "laboratorio": "Pfizer"},
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
      "edad": "11",
      "tipo_edad": "Años",
      "dosis": "1",
      "fecha_vacuna": "20/04/2016",
      "lote_vacuna": "ASPNA892AA",
      "fecha_refuerzo": "N/A",
      "vacuna": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                  "name": "Sarampión",
                  "laboratorio": "Pfizer"},
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

`DELETE /api/proyectoArquitectura/Aplicacion/:id`
----------------------------------------------
Eliminar un registro de Aplicación Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Aplicacion/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Aplicacion/:id`
----------------------------------------------

Actualiza un registro de Aplicación Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{
        "edad": "12",
        "tipo_edad": "Años",
        "dosis": "1",
        "fecha_vacuna": "20/05/2017",
        "lote_vacuna": "ASPNA892AA",
        "fecha_refuerzo": "N/A",
        "vacuna": { "name": "Viruela",
                    "laboratorio": "Pfizer"},
        "ips": {"name": "Sura"}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Aplicacion/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
