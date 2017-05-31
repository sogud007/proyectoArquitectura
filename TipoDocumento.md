| create | POST | /TipoDocumento/ | Ingresar un nuevo Tipo de Documento. | 
| delete | DELETE | /TipoDocumento/:name | Elimina un Tipo de Documento Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "web_development_team"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/TipoDocumento`
--------------------------------------------

Crear un nuevo Tipo de Documento.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "name": "Registro_Civil" 
      }' \
   'http://localhost:8080/api/proyectoArquitectura/TipoDocumento'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/TipoDocumento/:name`
----------------------------------------------

Obtener un Tipo de Documento.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/TipoDocumento/Registro_Civil'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "name": "Registro_Civil"
}
```

`GET /api/proyectoArquitectura/TipoDocumento/`
----------------------------------------------

Obtener todos los Tipos de Documento.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/TipoDocumento'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "TiposDocumento": [
    {
      "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
      "name": "Registro_Civil",
    },
    {
      "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
      "name": "Tarjeta_Identidad",
    },
    {
      "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
      "name": "Cedula_Ciudadania",
    },        
}   
```

`DELETE /api/proyectoArquitectura/TipoDocumento/:name`
----------------------------------------------
Eliminar un Tipo de Documento Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/TipoDocumento/Cedula_Ciudadania'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```
