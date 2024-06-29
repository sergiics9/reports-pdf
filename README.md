# Report Server | NestJS

Este proyecto se basa en NestJS y tiene como objetivo generar archivos PDF a través de diversos endpoints. A continuación se describen los módulos y rutas disponibles para la generación de diferentes tipos de informes en formato PDF.

## Uso de Insomnia

Para probar los endpoints, se recomienda utilizar [Insomnia](https://insomnia.rest/). Insomnia es una herramienta fácil de usar para enviar solicitudes HTTP y ver las respuestas. Puedes configurar los endpoints descritos anteriormente y verificar la generación de los archivos PDF.

## Estructura del Proyecto

El proyecto se organiza en dos módulos principales:

- `basic-reports`
- `extra-reports`

### Basic Reports

El módulo `basic-reports` incluye las siguientes rutas y funcionalidades:

#### Rutas

- `GET /basic-reports`
  - Genera un PDF con el título "Hola-Mundo".
- `GET /basic-reports/employment-letter`
  - Genera una carta de empleo en PDF con el título "Employment-Letter".
- `GET /basic-reports/employment-letter/:employeeId`
  - Genera una carta de empleo en PDF específica para un empleado, basado en el `employeeId` proporcionado. El título del PDF es "Employment-Letter".
- `GET /basic-reports/countries`
  - Genera un informe de países en PDF con el título "Countries-Report".

### Extra Reports

El módulo `extra-reports` incluye las siguientes rutas y funcionalidades:

#### Rutas

- `GET /extra-reports/html-report`

  - Genera un informe HTML en PDF con el título "html-report".

- `GET /extra-reports/community-report`

  - Genera un informe de la comunidad en PDF con el título "Billing-Report".

- `GET /extra-reports/custom-size`
  - Genera un PDF de tamaño personalizado con el título "Custom-Size".

## Cómo Iniciar el Proyecto

### Ejecutar en Dev

1. Clonar el repositorio.
2. Instalar dependencias `npm install`.
3. Clonar `.env.template` y renombrar a `.env` y completar las variables de entorno en `.env`.
4. Levantar la base de datos `docker compose up -d`.
5. Generar el Prisma client `npx prisma generate`.
6. Ejecutar proyecto `npm run start:dev`.

## Scripts Disponibles

- `build`: Compila el proyecto.
- `format`: Formatea el código utilizando Prettier.
- `start`: Inicia la aplicación.
- `start:dev`: Inicia la aplicación en modo desarrollo con watch.
- `start:debug`: Inicia la aplicación en modo debug con watch.
- `start:prod`: Inicia la aplicación en producción.
- `lint`: Ejecuta ESLint y corrige los problemas encontrados.

## Dependencias

- NestJS
- Express
- Prisma
- pdfmake
- html-to-pdfmake
- axios
- jsdom
- reflect-metadata
- rxjs
