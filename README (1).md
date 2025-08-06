# Proyecto Backend Seguro con Express.js

## Descripción del Proyecto
Este proyecto consiste en crear un sistema backend que permita a los usuarios registrarse, iniciar sesión y trabajar con publicaciones (crear, ver, editar o eliminar). El sistema protege las rutas para que solo los usuarios autorizados puedan acceder a ciertas funciones, como eliminar contenido, que solo puede hacerlo un administrador.

## Tecnologías Utilizadas
- Node.js: Entorno de ejecución de JavaScript.
- Express.js: Framework para crear el servidor backend.
- MongoDB: Base de datos para guardar usuarios y publicaciones.
- JWT: Método para proteger las rutas y manejar sesiones de usuario.

## Cómo Usar el Proyecto

1. **Descarga o clona el repositorio.**
2. **Instala las dependencias:**
   ```
   npm install
   ```
3. **Crea un archivo `.env` con lo siguiente:**
   ```
   PORT=3000
   JWT_SECRET=supersecretkey
   ```
4. **Asegúrate de tener MongoDB funcionando en tu computador.**
5. **Inicia el servidor:**
   ```
   npm start
   ```

## Endpoints Disponibles

### Autenticación
- `POST /api/auth/register`: Crear cuenta nueva.
- `POST /api/auth/login`: Iniciar sesión (devuelve un token).

### Publicaciones (Posts)
Estas rutas necesitan que el usuario esté autenticado con un token:
- `GET /api/posts`: Ver publicaciones.
- `POST /api/posts`: Crear publicación.
- `PUT /api/posts/:id`: Editar publicación.
- `DELETE /api/posts/:id`: Eliminar publicación (solo administrador).

## Roles y Permisos
- **Usuario normal**: puede ver y crear publicaciones.
- **Administrador**: puede hacer todo, incluso eliminar.

## Estructura del Proyecto
```
backend-login-project/
│
├── controllers/
├── middlewares/
├── models/
├── routes/
├── .env
├── app.js
├── package.json
└── README.md
```

## Estado Actual
El sistema funciona correctamente en modo local. Está preparado para ser mejorado o desplegado en servidores reales si se requiere.
