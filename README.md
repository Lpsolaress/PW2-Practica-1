# 🚀 Sistema de eCommerce con Soporte en Tiempo Real

Este proyecto es una aplicación web de comercio electrónico de extremo a extremo que combina un frontend reactivo desarrollado en **Svelte 5** y un backend en **Node.js** con soporte para comunicación en tiempo real. 

---

## 🛠️ Tecnologías Utilizadas

### Frontend
- **Svelte 5** (uso de **Runes** para la reactividad: `$state`, `$derived`, `$effect`).
- **Vite** para el empaquetado y desarrollo rápido.
- **Vanilla CSS** con un diseño moderno, oscuro y premium.
- **Leaflet** para mapas interactivos en la selección de direcciones a domicilio.

### Backend
- **Node.js** con **Express**.
- **Socket.io** para chat de soporte y notificaciones en vivo.
- **Mongoose** (MongoDB) para el modelado de bases de datos.
- **JWT** (JSON Web Tokens) para autenticación segura en endpoints y sockets.

---

## 🌟 Características Principales

### 1. **Autenticación y Roles**
- ✅ Registro y login basado en JWT.
- ✅ Roles diferenciados: **Usuario** y **Administrador**.
- ✅ Contraseñas encriptadas con `bcrypt`.

### 2. **Tienda y Carrito de Compras**
- ✅ Dashboard de productos con filtros, ordenamiento y paginación.
- ✅ Modal de vista rápida de productos.
- ✅ Carrito persistente: agregar, quitar y modificar cantidades.
- ✅ **Mapa Interactivo**: Selección de direcciones en vivo o de locales Nuba para recolectar.
- ✅ **Checkout**: Simulación de compra con múltiples métodos de pago (Visa/Mastercard, Paypal, **Apple Pay**).

### 3. **Centro de Soporte (Chat en Vivo)**
- ✅ Chat bidireccional entre usuarios y administradores.
- ✅ Subida de imágenes a la conversación en vivo.
- ✅ **Vista de Admin**: Cola de conversaciones activas, notificaciones de nuevos tickets y marcadores de mensajes "Leídos".

### 4. **Panel de Usuario / Administrador**
- ✅ Gestión de perfil (nombre, foto, contraseñas).
- ✅ Historial de compras/órdenes por usuario.
- ✅ **(Admin)** Control de estado de pedidos (Completado / Cancelado).
- ✅ **(Admin)** Visualización de la lista completa de usuarios registrados.
- ✅ Administración de Direcciones y Métodos de pago vinculados a la cuenta.

---

## 📂 Organización del Proyecto

El repositorio está dividido en dos grandes directorios para mantener una arquitectura limpia:

```text
├── backend/                  # Servidor Express + Socket.io
│   ├── models/               # Modelos de Mongoose (Usuario, Orden, Mensaje, etc.)
│   ├── routes/               # Enrutamiento de la API REST
│   ├── uploads/              # Almacén de imágenes estáticas (perfiles, productos, chat)
│   └── Chat Server 2.js       # Servidor unificado principal de la aplicación
|
└── frontend/                 # Aplicación Cliente Svelte 5
    └── src/
        ├── components/       # Componentes reutilizables (NavBar, Modales, etc.)
        ├── pages/           # Vistas (CartPage, LoginPage, ProductsPage, ProfilePage, SupportHubPage)
        ├── services/         # Consumo de APIs (auth, carrito, ordenes, usuarios)
        └── state/            # app.svelte.js (Gestor de Estado Global Reactivo)
```

---

## ⚙️ Instalación y Configuración

### 1. Clonar el repositorio
```bash
git clone <URL_DEL_REPOSITORIO>
cd PW-Proyecto 2
```

### 2. Variables de Entorno (Backend)
Crea un archivo `.env` dentro de la carpeta `backend/` con las siguientes configuraciones:
```dotenv
PORT=3000
MONGO_URI=mongodb://localhost:27017/productos
JWT_SECRET=tu_secreto_seguro
```

### 3. Instalar Dependencias
Debes correr `npm install` tanto para el entorno de backend como para el frontend:
```bash
# Servidor
cd backend && npm install

# Cliente
cd ../frontend && npm install
```

---

## 🚀 Cómo Ejecutar el Proyecto

Puedes arrancar tanto el backend como el frontend de forma simultánea con un solo comando desde la **raíz del proyecto**:

```bash
# Ubícate en la raíz del proyecto
npm run dev
```

El servidor utiliza `concurrently` para correr el backend en el puerto `3000` y el entorno de Vite para el frontend. 

---

## 📌 Notas Adicionales
- Para consultar o previsualizar la base de datos de manera visual, se recomienda utilizar **MongoDB Compass**.
- El puerto `3000` debe estar libre para que el Chat y la API interactúen sin errores de CORS bloqueados.

---

## 🔗 Repositorio
- [PW2-Practica-1](https://github.com/Lpsolaress/PW2-Practica-1.git)
