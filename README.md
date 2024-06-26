# Web Full Stack Test
Este proyecto es una aplicación web full-stack con un frontend en React y un backend en .NET.

## Tabla de Contenidos
- [Introducción](#introducción)
- [Requisitos Previos](#requisitos-previos)
- [Instalación](#instalación)
- [Ejecutar la Aplicación](#ejecutar-la-aplicación)
- [Uso de la Aplicación](#uso-de-la-aplicación)

## Introducción

Este proyecto fue creado con [Create React App](https://github.com/facebook/create-react-app) para el frontend y .NET Web API para el backend.

## Requisitos Previos

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)
- [.NET SDK](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/es-es/sql-server/sql-server-downloads)

## Instalación
1. **Clonar el repositorio:**

```bash
git clone https://github.com/AlejandroBeltre/testFullStackJunior.git

cd testFullStackJunior
```

2. **Instalar dependencias del frontend:**

```bash
cd frontend 

npm install
```

3. **Instalar dependencias del backend:**

```bash
cd backend

dotnet restore
```

4. **Crear la base de datos:**

- Ejecuta el script ['WebAppDB.sql'](database/WebAppDB.sql) ubicado en la carpeta [Database](database).
- Tras esto ejecuta ambos querys de inserción para los [Productos](database/ProductsQueryInsert.sql) como para los [Usuarios](database/UsersQueryInsert.sql), ambos ubicados en la carpeta [Database](database).
A la hora de la ejecución de la apliación debe de mantener la el servidor SQL donde creo la base de datos encendida, esto además de que en el [appsettings.json](backend/appsettings.json) debe de modificar el default string para su 'User' y 'Password' especifico de su instancia. Para asegurarse de que se use la base de datos adecuada debe de mantener solamente esta instancia encendida.

## Ejecutar la Aplicación

1. **Iniciar el backend:**

```bash
cd backend

dotnet run or dotnet watch
```

2. **Iniciar el frontend:**

```bash
cd ../frontend

npm start
```

## Uso de la Aplicación

Aqui puede comenzar a testear manualmente la aplicación puesto que tras ejecutar ambos comando se abrira automáticamente dos páginas web una en donde vera el frontend de la apliación y otra donde vera la documentación de la api del backend que es consumida en el frontend.

En el localhost:3000 se encontrara con la aplicación del frontend de React donde podra testear el funcionamiento de la api en el backend siendo consumida por el frontend.

Dependiendo la manera de correr el backend que eligio varia el puerto pero si eligio utilizar ```dotnet run``` se encuentra en el localhost:5000 mientras que si eligio ```dotnet watch``` se encuentra en el localhost:5147. En estas rutas va a encontrar la documentación hecha por SwaggerUI para el consumo de la API en donde en la misma se pueden testear los endpoints.