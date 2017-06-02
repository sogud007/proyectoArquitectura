Carnet API Reference
====================

Carnet
====
Representa los Carnets de Vacunas.

| Method | HTTP request | Descripción |
| --- | --- | ---- |
| get | GET | /Carnet/:id | Obtiene una Carnet por ID. |
| create | POST | /Carnet/ | Ingresar un nuevo Carnet. |
| delete | DELETE | /Carnet/:name | Elimina un Carnet Existente. |
| update | PUT | /Carnet/:name | Actualiza un Carnet Existente. |

Nota:
URIs relative to https://www.yourhostname.com/api/proyectoArquitectura/

Resource representations
========================
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "ciudadano": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
  "ips_creacion": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
  "aplicaciones": [{"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
                "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
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
              }],
  "created": "timestamp",
  "update": "timestamp"
}
```

###Ejemplos###

`POST /api/proyectoArquitectura/Carnet`
--------------------------------------------

Crear un nuevo Carnet.

```sh
curl -sv -X POST \
  -H 'accept: application/json' \
    -H 'X-VirtShell-Authorization: UserId:Signature' \
  -d '{ 
        "ciudadano": {"registro_civil": "89895553-5",
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
					}},
	  "ips_creacion": { "name": "Sura"}
      }' \
   'http://localhost:8080/api/proyectoArquitectura/Carnet'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "create": "success" }
```

`GET /api/proyectoArquitectura/Carnet/:id`
----------------------------------------------

Obtener un Carnet.

```sh
curl -sv -H 'accept: application/json' 
     -H 'X-VirtShell-Authorization: UserId:Signature' \ 
     'http://localhost:8080/api/proyectoArquitectura/Carnet/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{
  "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
  "ciudadano": {"id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
  "ips_creacion": { "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
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
  "vacunas": [{ "id": "ab8076c0-db91-11e2-82ce-0002a5d5c51b",
                "name": "Viruela",
                "laboratorio": "Pfizer"
              },
              {
                "id": "a379f19c-8c8b-11e5-8994-feff819cdc9f",
                "name": "Viruela",
                "laboratorio": "Wyeth"
              },
              {
                "id": "a379f3d6-8c8b-11e5-8994-feff819cdc9f",
                "name": "Viruela",
                "laboratorio": "Sanofi"
              }],
  "created": "timestamp",
  "update": "timestamp"
}
```

`DELETE /api/proyectoArquitectura/Carnet/:id`
----------------------------------------------
Eliminar un Carnet Existente.

```sh
curl -sv -X DELETE \
   -H 'accept: application/json' \
   -H 'X-VirtShell-Authorization: UserId:Signature' \
   'http://localhost:8080/api/proyectoArquitectura/Carnet/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "delete": "success" }
```

`PUT /api/proyectoArquitectura/Carnet/:id`
----------------------------------------------

Actualiza un Carnet Existente.

```sh
curl -sv -X PUT \
	-H 'accept: application/json' \
   	-H 'X-VirtShell-Authorization: UserId:Signature' \
	-d '{
		"ciudadano": {  "registro_civil": "89895553-5",
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
						}},
		  "ips_creacion": { "name": "Sura"}
	    }' \
   'http://localhost:8080/api/proyectoArquitectura/Carnet/ab8076c0-db91-11e2-82ce-0002a5d5c51b'
```

Response:
```
HTTP/1.1 200 OK
Content-Type: application/json
```
```json
{ "update": "success" }
```
