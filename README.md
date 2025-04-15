# 🎉 Plataforma Integral para Organización de Eventos

Una aplicación móvil que revoluciona la forma de planificar, contratar y gestionar eventos en Bolivia. Diseñada para organizadores, proveedores y asistentes, esta plataforma conecta fácilmente la oferta y demanda de servicios de eventos en un entorno seguro, eficiente y colaborativo.

---

## 📱 Tecnologías Utilizadas

| Componente     | Tecnología        |
|----------------|-------------------|
| Frontend       | Flutter (Dart)    |
| Backend        | Node.js (Express) |
| Base de Datos  | PostgreSQL        |
| ORM            | Prisma            |
| API REST       | Express + JWT     |
| Gestión de versiones | GitHub        |
| Comunicación   | Google Meet, WhatsApp |
| Planificación  | Trello, Taiga     |

---

## 🚀 Funcionalidades Clave

- Registro e inicio de sesión con autenticación segura.
- Roles definidos: Organizadores, Proveedores y Asistentes.
- Gestión de eventos con fechas, ubicaciones y servicios requeridos.
- Contratación y firma digital de contratos con proveedores.
- Sistema de mensajería interna entre usuarios.
- Calificaciones y reseñas para promover la calidad del servicio.
- Pasarela de pagos integrada.
- Búsqueda de proveedores con filtros (categoría, ubicación, precios).
- Historial de servicios contratados y asistentes registrados.
- Notificaciones automáticas vía email.

---

## 🧩 Arquitectura General

```
Flutter (Mobile App)
       ↓
   Express.js API (Node.js)
       ↓
PostgreSQL (Base de datos relacional)
```

---

## 🗃️ Estructura del Proyecto

```
📁 redibo_app_flutter/       # Frontend (Flutter)
📁 redibo_api_backend/       # Backend (Node.js + Express)
├── controllers/
├── routes/
├── middlewares/
├── prisma/                  # Esquema de base de datos
└── uploads/                 # Fotos y archivos de productos/servicios
📁 docs/                     # Documentación del proyecto
```

---

## 🧠 Modelo de Datos (Resumen)

- **Usuario**: id, nombre, email, contraseña, tipo (organizador, proveedor, asistente)
- **Evento**: id, nombre, descripción, fechas, estado, organizador_id
- **Producto/Servicio**: id, nombre, descripción, precio, proveedor_id
- **Contrato**: evento_id, proveedor_id, términos, condiciones, estado, fecha
- **Reseña**: calificador_id, calificado_id, puntuación, comentario
- **Mensaje**: remitente_id, destinatario_id, contenido
- **Pago**: contrato_id, monto, método, estado
- **Ubicación y Categoría**: con entidades intermedias para relaciones N:N

---

## 🧪 Pruebas

- 🔧 Se usan endpoints con Postman para validar rutas de la API.
- 📱 Pruebas en emuladores Android/iOS para la app Flutter.
- ✔️ Autenticación probada con JWT.
- 🧪 Funcionalidades verificadas: login, creación de eventos, filtrado de proveedores, contratación y mensajería.

---

## 🌀 Metodología Scrum

| Rol                  | Integrante                        |
|----------------------|-----------------------------------|
| 🧭 Scrum Master       | Bryan Vásquez Maldonado           |
| 💡 Product Owner      | Equipo completo                   |
| 🛠️ Developers         | Alejandra Cabezas, Bryan, Rodrigo |
| 🎨 UX/UI Designer     | Rodrigo Vargas                    |
| 🔍 Tester             | Juan Adiel Butrón                 |
| 📋 PM & Coordinación  | Gianinna Miranda                  |

### 🗓️ Sprints (3 Meses)

1. **Mes 1**: Planificación, análisis, diseño.
2. **Mes 2**: Desarrollo de backend y frontend.
3. **Mes 3**: Seguridad, pruebas y despliegue.

---

## 📦 Instalación y Despliegue

### 🔧 Backend (Node.js)

```bash
cd redibo_api_backend
npm install
npx prisma migrate dev
npm run dev
```

### 🐘 Base de Datos (PostgreSQL)

- Configurar `.env` con tu URL de conexión a PostgreSQL.
- Ejecutar migraciones con Prisma.

### 📱 Frontend (Flutter)

```bash
cd redibo_app_flutter
flutter pub get
flutter run
```

---

## 🌐 Enlaces Útiles

- [Flutter](https://flutter.dev)
- [Node.js](https://nodejs.org)
- [Prisma ORM](https://www.prisma.io/)
- [PostgreSQL](https://www.postgresql.org/)
- [Scrum Guide](https://scrumguides.org/)

---

## 📃 Licencia

Este proyecto es de carácter educativo, desarrollado en la Universidad Mayor de San Simón, Facultad de Ciencias y Tecnología, para la materia de Programación Móvil (2025).

---

## 👨‍🎓 Integrantes del Proyecto

- **Juan Adiel Butron Agreda** - Tester
- **Alejandra Mishel Cabezas Morales** - Frontend
- **Gianinna Valeska Miranda Ballesteros** - Project Manager
- **Rodrigo Vargas Calvi** - UX/UI Designer
- **Bryan Vasquez Maldonado** - Backend

---

> Desarrollado con ❤️ en Cochabamba - Bolivia 🇧🇴
