# Microservicio de Personas

Este proyecto consiste en un frontend en Angular y un backend en NestJS que permite capturar y saludar a personas por su nombre y apellidos.

## Estructura del proyecto

- **frontendtest**: Frontend en Angular que contiene un formulario para capturar nombres y apellidos.
- **backendtest**: Backend en NestJS que ofrece una API para saludar a las personas.

## Requisitos previos

- Docker y Docker Compose
- Node.js (para desarrollo local)
- npm (para desarrollo local)

## Instalación y ejecución

### Usando Docker

1. Construir las imágenes:

```sh
make build
```

2. Iniciar los servicios:

```sh
make run
```

3. Para desarrollo:

```sh
make run-dev
```

4. Para detener los servicios:

```sh
make stop
```

### Desarrollo local

#### Frontend

1. Navegar a la carpeta del frontend:

```sh
cd frontendtest
```

2. Instalar dependencias:

```sh
npm install
```

3. Iniciar el servidor de desarrollo:

```sh
npm start
```

#### Backend

1. Navegar a la carpeta del backend:

```sh
cd backendtest
```

2. Instalar dependencias:

```sh
npm install
```

3. Iniciar el servidor de desarrollo:

```sh
npm run start:dev
```

## Ejecución de pruebas

### Frontend

```sh
make test-frontend
```

o

```sh
cd FrontEndTest && npm test
```

### Backend

```sh
make test-backend
```

o

```sh
cd backendtest && npm test
```

## Endpoints de la API

- `POST /api/personas/saludar`: Recibe un objeto JSON con `nombre` y `apellidos` y devuelve un saludo.

Ejemplo de petición:

```json
{
  "nombre": "Juan",
  "apellidos": "Pérez"
}
```

Ejemplo de respuesta:

```json
{
  "mensaje": "Hola Juan Pérez"
}
```
