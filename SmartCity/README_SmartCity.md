# SMART CITY

**Objetivo:**  Simular una ciudad inteligente. Capturaremos datos de sensores de temperatura, CO2 y calidad del agua, los procesaremos en tiempo real y crearemos un panel de control para monitorizar la "salud" de la ciudad.

## Tareas

### Tarea 1. Creacion de entidades

``` json
   // Entidad: Sensor de Temperatura y Humedad
   {
     "id": "SensorTemperatura_01",
     "type": "SensorTemperatura",
     "location": {
       "type": "GeoProperty",
       "value": { "type": "Point", "coordinates": [-0.376, 39.469] }
     },
     "temperature": {
       "type": "Property",
       "value": 25.5,
       "unitCode": "CEL"
     },
     "humidity": {
       "type": "Property",
       "value": 60,
       "unitCode": "P1" // Porcentaje
     }
   }
```

### Tarea 2. Infraestructura FIWARE

#### Petición POST de creación de las entidades

``` json
  url = "http://localhost:1026/v2/entities"
  headers = {
      "Content-Type": "application/json"
  }
  data = {
    ...
  }
```

#### Petición POST de creación de la suscripcion/es

``` json
  url = "http://localhost:1026/v2/entities"
  headers = {
      "Content-Type": "application/json"
  }
  data = {
    ...
  }
```

#### Captura de pantalla de la consulta mongodb de las entidades

- Captura

#### Codigo Python de simulación de 400 entradas

- En un fichero aparte