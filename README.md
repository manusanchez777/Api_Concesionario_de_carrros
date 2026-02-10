# Proyecto: Api_Concesionario_de_carrros

## Estudiantes: Manuela Sanchez, David Marin

URL de la API: https://698775ff8bacd1d773ed6e16.mockapi.io/vehiculo

## 1.Modelo de datos diseñado: 

Se configuro el recuros *vehiculos* con la siguiente estructura de datos:

```
 {
    "Marca": "Toyota",
    "Modelo": "Corolla",
    "precio": 280000000,
    "Disponible": true,
    "Especificaciones": {
      "Motor": "2.0L 4 cilindros",
      "Transmisión": "CVT",
      "Potencia": "169 hp",
      "Consumo": "32 mpg"
    },
    "Tipo_vehiculo": [
      "Sedán",
      "Pasajeros"
    ],
    "id": "1"
  }

```

## 2. Bitacora de operaciones CRUD (Respuestas de Postman)

## A. Obtener todos los registros(GET)
###    - Status code: 200 OK
###    - Respuesta Postman:
```
 [
    {
        "Marca": "Toyota",
        "Modelo": "Corolla",
        "precio": 280000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "2.0L 4 cilindros",
            "Transmisión": "CVT",
            "Potencia": "169 hp",
            "Consumo": "32 mpg"
        },
        "Tipo_vehiculo": [
            "Sedán",
            "Pasajeros"
        ],
        "id": "1"
    },
    {
        "Marca": "Honda",
        "Modelo": "Civic",
        "precio": 250000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "2.0L i-VTEC",
            "Transmisión": "Manual 6 vel",
            "Potencia": "158 hp",
            "Seguridad": "Honda Sensing"
        },
        "Tipo_vehiculo": [
            "Sedán",
            "Compacto"
        ],
        "id": "2"
    },
    {
        "Marca": "Mazda",
        "Modelo": "CX-5",
        "precio": 32000000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "2.5L Skyactiv-G",
            "Tracción": "AWD",
            "Potencia": "187 hp",
            "Interior": "Cuero sintético"
        },
        "Tipo_vehiculo": [
            "SUV",
            "Crossover"
        ],
        "id": "3"
    },
    {
        "Marca": "Tesla",
        "Modelo": "Model 3",
        "precio": 3700000000,
        "Disponible": false,
        "Especificaciones": {
            "Motor": "Eléctrico Dual Motor",
            "Autonomía": "430 km",
            "Aceleración": "0-100 km/h en 6.1s",
            "Carga": "Supercharger compatible"
        },
        "Tipo_vehiculo": [
            "Eléctrico",
            "Sedán"
        ],
        "id": "4"
    },
    {
        "Marca": "Kia",
        "Modelo": "Rio",
        "precio": 160000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "1.6L 4 cilindros",
            "Transmisión": "Automática 6 vel",
            "Potencia": "120 hp",
            "Eficiencia": "Muy alta"
        },
        "Tipo_vehiculo": [
            "Hatchback",
            "Urbano"
        ],
        "id": "5"
    },
    {
        "Marca": "Ford",
        "Modelo": "F-150",
        "precio": 5000000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "3.5L V6 EcoBoost",
            "Tracción": "4x4",
            "Capacidad_remolque": "6,350 kg",
            "Tecnología": "Pro Power Onboard"
        },
        "Tipo_vehiculo": [
            "Pick-up",
            "Trabajo"
        ],
        "id": "6"
    },
    {
        "Marca": "BMW",
        "Modelo": "M4",
        "precio": 85000000000,
        "Disponible": false,
        "Especificaciones": {
            "Motor": "3.0L Twin-Turbo I6",
            "Potencia": "473 hp",
            "Transmisión": "M Steptronic",
            "Frenos": "Cerámicos"
        },
        "Tipo_vehiculo": [
            "Deportivo",
            "Coupe"
        ],
        "id": "7"
    },
    {
        "Marca": "Porsche",
        "Modelo": "911 Carrera",
        "precio": 95000000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "3.0L Boxer 6 cilindros",
            "Potencia": "379 hp",
            "Velocidad_max": "293 km/h",
            "Configuración": "Motor trasero"
        },
        "Tipo_vehiculo": [
            "Deportivo",
            "Lujo"
        ],
        "id": "8"
    },
    {
        "Marca": "Audi",
        "Modelo": "Q7",
        "precio": 610000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "3.0L V6 Turbo",
            "Asientos": "7 pasajeros",
            "Tracción": "Quattro",
            "Suspensión": "Neumática adaptativa"
        },
        "Tipo_vehiculo": [
            "SUV",
            "Premium"
        ],
        "id": "9"
    },
    {
        "Marca": "Mercedes-Benz",
        "Modelo": "EQS",
        "precio": 94000000000,
        "Disponible": false,
        "Especificaciones": {
            "Motor": "Eléctrico Síncrono",
            "Autonomía": "770 km",
            "Pantalla": "Hyperscreen MBUX",
            "Sonido": "Burmester 3D"
        },
        "Tipo_vehiculo": [
            "Eléctrico",
            "Gran Lujo"
        ],
        "id": "10"
    },
    {
        "Marca": "Land Rover",
        "Modelo": "Defender",
        "precio": 730000000000,
        "Disponible": true,
        "Especificaciones": {
            "Motor": "2.0L Turbo I4",
            "Capacidad_vadeo": "900 mm",
            "Terreno": "Terrain Response 2",
            "Estilo": "Off-road"
        },
        "Tipo_vehiculo": [
            "SUV",
            "Todoterreno"
        ],
        "id": "11"
    }
] 
```

## B. Creación de un nuevo registro(POST)

   ###  - Status code: 201 Created
   ###  - Cuerpo enviado Postman:
```
{
  "Marca": "Audi",
  "Modelo": "RS 5 Coupe",
  "precio": 85,
  "Disponible": false,
  "Especificaciones": {
    "Motor": "2.9L V6 TFSI Biturbo",
    "Potencia": "444 hp",
    "Tracción": "Quattro permanente",
    "Aceleración": "0-100 km/h en 3.9s",
    "Transmisión": "Tiptronic 8 velocidades"
  },
  "Tipo_vehiculo": ["Deportivo", "Coupe", "Premium"],
  "id": "12"
}
```
   ###   -Repuesta de Potsman:
 ```
   {
    "Marca": "Audi",
    "Modelo": "RS 5 Coupe",
    "precio": 85,
    "Disponible": false,
    "Especificaciones": {
        "Motor": "2.9L V6 TFSI Biturbo",
        "Potencia": "444 hp",
        "Tracción": "Quattro permanente",
        "Aceleración": "0-100 km/h en 3.9s",
        "Transmisión": "Tiptronic 8 velocidades"
    },
    "Tipo_vehiculo": [
        "Deportivo",
        "Coupe",
        "Premium"
    ],
    "id": "12"
}
```

## C. Culsulta de registro individual (GET)
###     -Endpoint:/vehiculo/11
###     - Status code: 200 OK
###     - Respuesta de Postman:
  ```
  {
    "Marca": "Land Rover",
    "Modelo": "Defender",
    "precio": 730000000000,
    "Disponible": true,
    "Especificaciones": {
        "Motor": "2.0L Turbo I4",
        "Capacidad_vadeo": "900 mm",
        "Terreno": "Terrain Response 2",
        "Estilo": "Off-road"
    },
    "Tipo_vehiculo": [
        "SUV",
        "Todoterreno"
    ],
    "id": "11"
}
```

## D.Actualización de registro (PUT)
   ###  - Status code: 200 OK
   ###  -Modificación: Se actualizó el precio y tipo de vehiculo del registro ID 8
   ###  - Respuesta de Postman:
   {
```
    "Marca": "Porsche",
    "Modelo": "911 Carrera",
    "precio": 99000000000,
    "Disponible": true,
    "Especificaciones": {
        "Motor": "3.0L Boxer 6 cilindros",
        "Potencia": "379 hp",
        "Velocidad_max": "293 km/h",
        "Configuración": "Motor trasero"
    },
    "Tipo_vehiculo": [
        "Carrera",
        "Deportivo"
    ],
    "id": "8"
}
```
## E.Eliminación de un registro (DELETE)
   ###  - Status code: 200 OK
   ###  - Respuesta de Postman:
    "Tipo_vehiculo": [
        "SUV",
        "Todoterreno"
    ],
    "id": "11"
}

   ## F. Validación de Recurso Inexistente (GET 404)
   ###  - Status code: 404 Not Found
   ###  - Respuesta de Postman:
```
  "Not found"

```
   
