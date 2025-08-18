# Proyecto Backend Seguro con Express.js

## 📌 Descripción
Este proyecto consiste en la creación de un sistema backend seguro, escalable y eficiente utilizando **Express.js**. Se implementa un sistema de autenticación y autorización basado en **JWT**, con control de acceso por roles (usuario y administrador). Además, se desarrolla una API RESTful con operaciones CRUD para un recurso llamado "posts".

##  Tecnologías Utilizadas
- Node.js
- Express.js
- MongoDB (con Mongoose)
- JSON Web Tokens (JWT)
- bcryptjs
- dotenv

## ⚙ Instalación y Ejecución

1. Clona el repositorio:
```bash
git clone https://github.com/tu-usuario/backend-login-project.git
cd backend-login-project
```

2. Instala las dependencias:
```bash
npm install
```

3. Crea un archivo `.env` con el siguiente contenido:
```
PORT=3000
JWT_SECRET=supersecretkey
```

4. Asegúrate de tener MongoDB ejecutándose en tu máquina (localhost:27017)

5. Inicia el servidor:
```bash
npm start
```

##  Endpoints de Autenticación

- `POST /api/auth/register`: Registro de usuarios
- `POST /api/auth/login`: Inicio de sesión (retorna token JWT)

##  Endpoints de Post

> Todas estas rutas requieren autenticación con JWT (en Header: `Authorization: Bearer <token>`)

- `GET /api/posts`: Obtener todos los posts
- `POST /api/posts`: Crear un post
- `PUT /api/posts/:id`: Actualizar un post
- `DELETE /api/posts/:id`: Eliminar un post (**solo para admins**)

##  Roles y Autorización
- `user`: Puede crear y ver publicaciones
- `admin`: Puede además eliminar publicaciones

##  Estructura del Proyecto

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

##  Desafíos y Decisiones
- Se optó por JWT por su sencillez y portabilidad.
- Se eligió MongoDB por su flexibilidad y rápida integración con Node.js.
- Se implementó control de acceso por roles para asegurar operaciones críticas.

##  Estado del Proyecto
Funcional y probado en entorno local. Listo para ser escalado o desplegado en producción con ajustes mínimos.

## 📎 Enlace al repositorio
[GitHub: backend-login-project](https://github.com/tu-usuario/backend-login-project)
