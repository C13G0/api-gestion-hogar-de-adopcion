# Proyecto: API de Gestión de Hogar de Adopciones

### Estudiantes
* **Andres Rios Arbelaez**
* **Victor Andres Sanchez**
* **Luisa Usuga**

---

### URL de la API
Puedes acceder a la API a través del siguiente enlace:
[https://698773068bacd1d773ed61c8.mockapi.io/Animales](https://698773068bacd1d773ed61c8.mockapi.io/Animales)

---

### 1. Modelo de Datos Diseñado
Se configuró el recurso **Animales** con la siguiente estructura de datos:



#### Ejemplo de estructura de un objeto (JSON):

```json
{
    "Nombre": "Orus",
    "Especie": "Perro",
    "Cuidados": {},
    "Etiqueta": [],
    "en_adopcion": true,
    "id": "1"
}


# 2. Bitácora de Operaciones CRUD (Respuestas Postman)

---

## A. Obtener todos los registros (GET)

**Status code:** `200 OK`

**Respuesta Postman:**
```json
[
    {
        "Nombre": "Nombre 1",
        "Especie": "Especie 1",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "1"
    },
    {
        "Nombre": "Nombre 2",
        "Especie": "Especie 2",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "2"
    },
    {
        "Nombre": "Nombre 3",
        "Especie": "Especie 3",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "3"
    },
    {
        "Nombre": "Nombre 4",
        "Especie": "Especie 4",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "4"
    },
    {
        "Nombre": "Nombre 5",
        "Especie": "Especie 5",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "5"
    },
    {
        "Nombre": "Nombre 6",
        "Especie": "Especie 6",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "6"
    },
    {
        "Nombre": "Nombre 7",
        "Especie": "Especie 7",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "7"
    },
    {
        "Nombre": "Nombre 8",
        "Especie": "Especie 8",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "8"
    },
    {
        "Nombre": "Nombre 9",
        "Especie": "Especie 9",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "9"
    },
    {
        "Nombre": "Nombre 10",
        "Especie": "Especie 10",
        "Cuidados": {},
        "Etiqueta": [],
        "en_adopcion": false,
        "id": "10"
    }
]
```

---

## B. Creación de un nuevo registro (POST)

**Status code:** `201 Created`

**Cuerpo enviado en Postman:**
```json
{
    "Nombre": "Firulais",
    "Especie": "Perro",
    "Cuidados": {},
    "Etiqueta": [],
    "en_adopcion": true
}
```

**Respuesta de Postman:**
```json
{
    "Nombre": "Firulais",
    "Especie": "Perro",
    "Cuidados": {},
    "Etiqueta": [],
    "en_adopcion": true,
    "id": "11"
}
```

---

## C. Consulta de registro individual (GET)

**Endpoint:** `Animales/11`  
**Status code:** `200 OK`

**Respuesta de Postman:**
```json
{
    "Nombre": "Firulais",
    "Especie": "Perro",
    "Cuidados": {},
    "Etiqueta": [],
    "en_adopcion": true,
    "id": "11"
}
```

---

## D. Actualización de un registro (PUT)

**Endpoint:** `Animales/1`  
**Status code:** `200 OK`  
**Modificación:** Se modifica el nombre del id `1` a `"Orus"`

**Respuesta de Postman:**
```json
{
    "Nombre": "Orus",
    "Especie": "Perro",
    "Cuidados": {},
    "Etiqueta": [],
    "en_adopcion": true,
    "id": "1"
}
```

---

## E. Eliminación de un registro (DELETE)

**Status code:** `200 OK`

**Respuesta de Postman:**
```json
{
    "Nombre": "Nombre 2",
    "Especie": "Especie 2",
    "Cuidados": {},
    "Etiqueta": [],
    "en_adopcion": false,
    "id": "2"
}
```

---

## F. Validación de recurso inexistente (GET 404)

**Status code:** `404 Not Found`

**Respuesta de Postman:**
```
"Not found"
```


# 3. Resumen de Endpoints y Código HTTP.

| Acción     | Método   | Endpoint     | Código HTTP   |
|------------|----------|--------------|---------------|
| Listar todo | GET     | Animales     | 200 OK        |
| Crear       | POST    | Animales     | 201 Created   |
| Ver por ID  | GET     | Animales/11  | 200 OK        |
| Actualizar  | PUT     | Animales/1   | 200 OK        |
| Borrar      | DELETE  | Animales/2   | 200 OK        |
| Error       | GET     | Animales/2   | 404 Not Found |
