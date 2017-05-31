Dirección API Reference
====================

Dirección
====
Representa las Direcciones.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Direccion/:id | Obtiene un Direccion por ID. |
| create | POST | /Direccion/ | Ingresar un nuevo Direccion. |
| delete | DELETE | /Direccion/:id | Elimina un Direccion Existente. |
| update | PUT | /Direccion/:id | Actualiza un Direccion Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Calle 2 # 37 - 124",
  "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
  		"name": "Cali", 
		"departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
				"name": "Valle"}
		},
  "created": "timestamp",
  "update": "timestamp"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Direccion`
--------------------------------------------

Crear una nueva Dirección.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Valle",
	"municipio": {"name"; "Cali", "departamento": {"name": "Valle"}}
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

`GET /api/proyectoArquitectura/Direccion/:id`
----------------------------------------------

Obtener un Direccion.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Direccion/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Calle 2 # 37 - 124",
  "municipio": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
  		"name": "Cali", 
		"departamento": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b", 
				"name": "Valle"}
		},
  "created": "timestamp",
  "update": "timestamp"
}
```

`DELETE /api/proyectoArquitectura/Direccion/:id`
----------------------------------------------
Eliminar un Direccion Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Direccion/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
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
	-d '{"name": "Calle 2 # 38 - 39"
		"municipio": {	"name": "Cali", 
				"departamento": {"name": "Valle"}
		}
	}' \
   'http://localhost:8080/api/proyectoArquitectura/Direccion/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
