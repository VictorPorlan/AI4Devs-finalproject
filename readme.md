## Índice

0. [Ficha del proyecto](#0-ficha-del-proyecto)
1. [Descripción general del producto](#1-descripción-general-del-producto)
2. [Arquitectura del sistema](#2-arquitectura-del-sistema)
3. [Modelo de datos](#3-modelo-de-datos)
4. [Especificación de la API](#4-especificación-de-la-api)
5. [Historias de usuario](#5-historias-de-usuario)
6. [Tickets de trabajo](#6-tickets-de-trabajo)
7. [Pull requests](#7-pull-requests)

---

## 0. Ficha del proyecto

### **0.1. Tu nombre completo:**
Víctor Porlan Soto
### **0.2. Nombre del proyecto:**
TradeBinder
### **0.3. Descripción breve del proyecto:**
TradeBinderes una plataforma web especializada en la compra, venta e intercambio de cartas de Magic: The Gathering, diseñada para fomentar el comercio local entre jugadores. Combina la simplicidad de apps de compraventa como Wallapop con la especialización de Card Market, ofreciendo filtros específicos para cartas, perfiles con reputación y un sistema de mensajería interna. Su objetivo es conectar a jugadores y coleccionistas dentro de la misma área geográfica, evitando costes de envío y creando un espacio seguro y confiable para la comunidad de Magic.
### **0.4. URL del proyecto:**

> Puede ser pública o privada, en cuyo caso deberás compartir los accesos de manera segura. Puedes enviarlos a [alvaro@lidr.co](mailto:alvaro@lidr.co) usando algún servicio como [onetimesecret](https://onetimesecret.com/).

### 0.5. URL o archivo comprimido del repositorio

> Puedes tenerlo alojado en público o en privado, en cuyo caso deberás compartir los accesos de manera segura. Puedes enviarlos a [alvaro@lidr.co](mailto:alvaro@lidr.co) usando algún servicio como [onetimesecret](https://onetimesecret.com/). También puedes compartir por correo un archivo zip con el contenido


---

# 1. Descripción general del producto  

---

### **1.1. Objetivo**  
El propósito del producto es **conectar a jugadores y coleccionistas de Magic: The Gathering en un entorno local**, permitiendo la compra, venta e intercambio de cartas de manera más rápida, sencilla y segura.  

El valor que aporta se centra en tres puntos clave:  
1. **Reducir costes**: elimina la necesidad de envíos y comisiones elevadas al fomentar las transacciones en persona.  
2. **Especialización**: a diferencia de plataformas genéricas de compraventa, está diseñada específicamente para cartas de Magic, con filtros por nombre, edición, estado y precio.  
3. **Confianza en la comunidad**: perfiles de usuario, valoraciones y mensajería interna garantizan seguridad y transparencia en las transacciones.  

El producto está dirigido a:  
- Jugadores casuales que buscan cartas para sus mazos.  
- Coleccionistas que intercambian cartas de valor.  
- Jugadores competitivos que necesitan cambios rápidos en su colección.  
- (Futuro) Tiendas y clubs locales que quieran interactuar con la comunidad.  

---

### **1.2. Características y funcionalidades principales**  

El **MVP** incluirá las siguientes funciones:  

1. **Gestión de usuarios**  
   - Registro e inicio de sesión (email/Google).  
   - Perfil con datos básicos (nombre, ubicación aproximada, avatar).  
   - Reputación mediante valoraciones tras transacciones.  

2. **Publicación de anuncios**  
   - Carga de cartas con nombre, fotos, edición, estado y precio.  
   - Opción de venta o intercambio.  
   - Localización aproximada para favorecer encuentros presenciales.  

3. **Búsqueda avanzada y filtrado**  
   - Por nombre de carta (autocompletado con base de datos de MTG).  
   - Por edición/colección.  
   - Por estado de la carta y rango de precios.  
   - Por cercanía geográfica.  

4. **Sistema de comunicación**  
   - Chat interno entre comprador y vendedor.  
   - Notificaciones de mensajes nuevos.  

5. **Gestión de favoritos**  
   - Posibilidad de guardar cartas o anuncios para seguimiento.  

6. **Confianza y seguridad**  
   - Sistema de reseñas y puntuación de usuarios.  
   - Reporte de anuncios sospechosos.  

7. **Administración (backoffice básico)**  
   - Gestión de usuarios y publicaciones.  
   - Moderación de reportes.  
   - Estadísticas de actividad.  

---

### **1.3. Diseño y experiencia de usuario**  

La experiencia de usuario será **sencilla, rápida y adaptada a móvil**, siguiendo un flujo claro:  

1. **Pantalla de inicio** → acceso directo a búsqueda o exploración de anuncios.  
2. **Registro/Login** → creación de perfil para publicar y chatear.  
3. **Exploración** → listado de cartas filtradas por cercanía, nombre, edición o estado.  
4. **Detalle del anuncio** → información completa de la carta, precio, fotos, ubicación y botón para contactar al vendedor.  
5. **Chat integrado** → comunicación directa entre jugadores.  
6. **Valoración tras la transacción** → refuerza la confianza en la comunidad.  

📌 En esta etapa inicial de documentación, se incluirían *wireframes* o *mockups* de cada vista clave (home, búsqueda, detalle de carta, chat, perfil).  
*(Podemos generarlos en una siguiente fase si lo deseas).*  

---

### **1.4. Instrucciones de instalación**  

Para poner en marcha el proyecto en local, se plantea la siguiente arquitectura básica:  

- **Frontend**: React con Tailwind CSS.  
- **Backend**: Node.js con Express.  
- **Base de datos**: PostgreSQL.  
- **Autenticación**: JWT (con opción de OAuth para Google en fases posteriores).  
- **Entorno de desarrollo**: Docker para uniformizar backend + base de datos.  

#### Pasos de instalación (modo local)  

1. **Clonar el repositorio**  
```bash
git clone https://github.com/usuario/proyecto-mtg-market.git
cd proyecto-mtg-market
```
# 1. Descripción general del producto  
---

### **1.1. Objetivo**  
El propósito del producto es **conectar a jugadores y coleccionistas de Magic: The Gathering en un entorno local**, permitiendo la compra, venta e intercambio de cartas de manera más rápida, sencilla y segura.  

El valor que aporta se centra en tres puntos clave:  
1. **Reducir costes**: elimina la necesidad de envíos y comisiones elevadas al fomentar las transacciones en persona.  
2. **Especialización**: a diferencia de plataformas genéricas de compraventa, está diseñada específicamente para cartas de Magic, con filtros por nombre, edición, estado y precio.  
3. **Confianza en la comunidad**: perfiles de usuario, valoraciones y mensajería interna garantizan seguridad y transparencia en las transacciones.  

El producto está dirigido a:  
- Jugadores casuales que buscan cartas para sus mazos.  
- Coleccionistas que intercambian cartas de valor.  
- Jugadores competitivos que necesitan cambios rápidos en su colección.  
- (Futuro) Tiendas y clubs locales que quieran interactuar con la comunidad.  

---

### **1.2. Características y funcionalidades principales**  

El **MVP** incluirá las siguientes funciones:  

1. **Gestión de usuarios**  
   - Registro e inicio de sesión (email/Google).  
   - Perfil con datos básicos (nombre, ubicación aproximada, avatar).  
   - Reputación mediante valoraciones tras transacciones.  

2. **Publicación de anuncios**  
   - Carga de cartas con nombre, fotos, edición, estado y precio.  
   - Opción de venta o intercambio.  
   - Localización aproximada para favorecer encuentros presenciales.  

3. **Búsqueda avanzada y filtrado**  
   - Por nombre de carta (autocompletado con base de datos de MTG).  
   - Por edición/colección.  
   - Por estado de la carta y rango de precios.  
   - Por cercanía geográfica.  

4. **Sistema de comunicación**  
   - Chat interno entre comprador y vendedor.  
   - Notificaciones de mensajes nuevos.  

5. **Gestión de favoritos**  
   - Posibilidad de guardar cartas o anuncios para seguimiento.  

6. **Confianza y seguridad**  
   - Sistema de reseñas y puntuación de usuarios.  
   - Reporte de anuncios sospechosos.  

7. **Administración (backoffice básico)**  
   - Gestión de usuarios y publicaciones.  
   - Moderación de reportes.  
   - Estadísticas de actividad.  

---

### **1.3. Diseño y experiencia de usuario**  

La experiencia de usuario será **sencilla, rápida y adaptada a móvil**, siguiendo un flujo claro:  

1. **Pantalla de inicio** → acceso directo a búsqueda o exploración de anuncios.  
2. **Registro/Login** → creación de perfil para publicar y chatear.  
3. **Exploración** → listado de cartas filtradas por cercanía, nombre, edición o estado.  
4. **Detalle del anuncio** → información completa de la carta, precio, fotos, ubicación y botón para contactar al vendedor.  
5. **Chat integrado** → comunicación directa entre jugadores.  
6. **Valoración tras la transacción** → refuerza la confianza en la comunidad.  

📌 En esta etapa inicial de documentación, se incluirían *wireframes* o *mockups* de cada vista clave (home, búsqueda, detalle de carta, chat, perfil).  
*(Podemos generarlos en una siguiente fase si lo deseas).*  

---

### **1.4. Instrucciones de instalación**  

Para poner en marcha el proyecto en local, se plantea la siguiente arquitectura básica:  

- **Frontend**: React con Tailwind CSS.  
- **Backend**: Node.js con Express.  
- **Base de datos**: PostgreSQL.  
- **Autenticación**: JWT (con opción de OAuth para Google en fases posteriores).  
- **Entorno de desarrollo**: Docker para uniformizar backend + base de datos.  

#### Pasos de instalación (modo local)  

1. **Clonar el repositorio**  
```bash
git clone https://github.com/usuario/proyecto-mtg-market.git
cd proyecto-mtg-market
```

## 2. Arquitectura del Sistema

---

### 2.1. Diagrama de arquitectura

La aplicación sigue una arquitectura **cliente-servidor en tres capas**:  

- **Frontend:** SPA en React con Material UI.  
- **Backend:** NestJS modular para la lógica de negocio y API REST.  
- **Base de datos:** PostgreSQL con ORM (TypeORM o Prisma).  

Inspirada en **arquitectura en capas**, separando: presentación, negocio y datos.  

**Beneficios:**  
- Separación de responsabilidades.  
- Escalabilidad independiente de frontend y backend.  
- Productividad con MaterialUI y estructura NestJS.  
- Gran soporte comunitario.  

**Sacrificios:**  
- Curva de aprendizaje inicial.  
- Complejidad en despliegue inicial.  

**Diagrama Mermaid (indentado para mantener bloque único):**

    flowchart TD
        User((Usuario)) -->|UI/UX| Frontend[React + MaterialUI]
        Frontend -->|HTTP/REST| Backend[NestJS API]
        Backend -->|ORM| Database[(PostgreSQL)]
        Backend --> Auth[JWT / OAuth 2.0]

---

### 2.2. Descripción de componentes principales

- **Frontend (React + MaterialUI):** SPA, navegación fluida, componentes reutilizables, estado global con Context API/Redux.  
- **Backend (NestJS):** modularidad, controladores REST, servicios de negocio, guards y middleware de seguridad, ORM para PostgreSQL.  
- **Base de datos (PostgreSQL):** modelo relacional para usuarios, cartas, anuncios, transacciones y valoraciones; migraciones y seeds; índices para búsquedas rápidas.

---

### 2.3. Descripción de alto nivel y estructura de ficheros

```
/proyecto-mtg-market
│
├── /frontend
│   ├── /public
│   ├── /src
│   │   ├── /components
│   │   ├── /pages
│   │   ├── /services
│   │   ├── /context
│   │   └── /assets
│
├── /backend
│   ├── /src
│   │   ├── /modules
│   │   ├── /controllers
│   │   ├── /services
│   │   ├── /entities
│   │   ├── /middlewares
│   │   └── main.ts
│
├── /db
│   ├── /migrations
│   └── /seeds
│
└── docker-compose.yml
```

Patrón modular en backend y component-based en frontend.

---

### 2.4. Infraestructura y despliegue

**Infraestructura:** Docker: contenedores para frontend (React/Nginx), backend (NestJS), base de datos (PostgreSQL).  

**Diagrama Mermaid (indentado):**

    flowchart LR
        Dev[Desarrollador] --> GitHub[(Repositorio)]
        GitHub --> CI/CD[Pipeline CI/CD]
        CI/CD --> DockerHub[(Imágenes Docker)]
        DockerHub --> Server[Servidor/Cloud]
        Server --> Frontend[Contenedor React/Nginx]
        Server --> Backend[Contenedor NestJS]
        Server --> Database[(PostgreSQL)]

**Despliegue:** push a rama principal → CI/CD tests + build → imágenes Docker → despliegue en servidor → frontend en https://app.dominio.com y backend en https://api.dominio.com.

---

### 2.5. Seguridad

- Autenticación JWT.  
- Hash de contraseñas con bcrypt.  
- Validación de inputs (Pipes/DTOs NestJS).  
- CORS configurado.  
- HTTPS en producción.  
- Roles y guards de autorización.  
- Prevención de inyecciones SQL mediante ORM.  
- Rate limiting en endpoints sensibles.

Ejemplo guard NestJS:

    @UseGuards(JwtAuthGuard, RolesGuard)
    @Roles('admin')
    @Get('users')
    findAll() {
      return this.userService.findAll();
    }

---

### 2.6. Tests

- **Frontend:** Unit tests con Jest + React Testing Library; snapshot tests.  
- **Backend:** Unit tests de servicios, integration tests de controladores, E2E tests simulando flujos completos.  
- **Base de datos:** tests de migraciones y seeds.  

Tests ejecutados automáticamente en CI/CD antes de desplegar.

# 3. Modelo de Datos

---

### 3.1. Diagrama del modelo de datos

Diagrama Mermaid mostrando las entidades principales y relaciones:

    erDiagram
        USERS {
            int id PK "Identificador único de usuario"
            varchar email "Email del usuario" UNIQUE NOT NULL
            varchar password "Contraseña hashed" NOT NULL
            varchar username "Nombre de usuario" UNIQUE NOT NULL
            varchar location "Ubicación aproximada" NULL
        }

        CARDS {
            int id PK "Identificador único de carta"
            varchar name "Nombre de la carta" NOT NULL
            varchar edition "Edición o colección" NOT NULL
            varchar condition "Estado (NM, LP, etc.)" NOT NULL
            decimal price "Precio de venta" NOT NULL
            int seller_id FK "ID del usuario vendedor"
        }

        ANNOUNCEMENTS {
            int id PK "Identificador único del anuncio"
            int card_id FK "Carta asociada"
            int seller_id FK "Vendedor que publica"
            text description "Descripción adicional"
            datetime created_at "Fecha de creación"
        }

        MESSAGES {
            int id PK "Identificador único del mensaje"
            int sender_id FK "Usuario que envía el mensaje"
            int receiver_id FK "Usuario que recibe"
            int announcement_id FK "Anuncio relacionado"
            text content "Contenido del mensaje"
            datetime created_at "Fecha de envío"
        }

        USERS ||--o{ ANNOUNCEMENTS : "publica"
        USERS ||--o{ MESSAGES : "envía"
        USERS ||--o{ MESSAGES : "recibe"
        CARDS ||--o{ ANNOUNCEMENTS : "aparece en"
        ANNOUNCEMENTS ||--o{ MESSAGES : "relaciona"

---

### 3.2. Descripción de entidades principales

**Usuarios (USERS)**
- `id`: int, PK, autoincremental.
- `email`: varchar, UNIQUE, NOT NULL.
- `password`: varchar, NOT NULL (hashed).
- `username`: varchar, UNIQUE, NOT NULL.
- `location`: varchar, NULL, ubicación aproximada.
- Relaciones: 
  - 1:N con ANNOUNCEMENTS (un usuario puede publicar múltiples anuncios).
  - 1:N con MESSAGES (un usuario puede enviar y recibir muchos mensajes).

**Cartas (CARDS)**
- `id`: int, PK, autoincremental.
- `name`: varchar, NOT NULL.
- `edition`: varchar, NOT NULL.
- `condition`: varchar, NOT NULL.
- `price`: decimal, NOT NULL.
- `seller_id`: int, FK a USERS(id).
- Relaciones:
  - 1:N con ANNOUNCEMENTS (una carta puede aparecer en varios anuncios si distintos usuarios la venden).

**Anuncios (ANNOUNCEMENTS)**
- `id`: int, PK, autoincremental.
- `card_id`: int, FK a CARDS(id), NOT NULL.
- `seller_id`: int, FK a USERS(id), NOT NULL.
- `description`: text, opcional.
- `created_at`: datetime, NOT NULL.
- Relaciones:
  - 1:N con MESSAGES (un anuncio puede tener muchos mensajes relacionados).

**Mensajes (MESSAGES)**
- `id`: int, PK, autoincremental.
- `sender_id`: int, FK a USERS(id), NOT NULL.
- `receiver_id`: int, FK a USERS(id), NOT NULL.
- `announcement_id`: int, FK a ANNOUNCEMENTS(id), NOT NULL.
- `content`: text, NOT NULL.
- `created_at`: datetime, NOT NULL.
- Relaciones:
  - Cada mensaje se vincula a un anuncio específico y a dos usuarios (emisor y receptor).

---

Este modelo cubre el **MVP funcional** de la plataforma: registro de usuarios, publicación de cartas, anuncios y chat entre comprador/vendedor.  


## 4. Especificación de la API

---

A continuación se detallan los **endpoints principales del backend** para el MVP:

### **1. Registro de usuario**

```yaml
POST /api/auth/register
Request:
{
  "email": "usuario@ejemplo.com",
  "username": "miUsuario",
  "password": "miContraseñaSegura"
}

Response 201 Created:
{
  "id": 1,
  "email": "usuario@ejemplo.com",
  "username": "miUsuario",
  "location": null
}
```

---

### **2. Publicar un anuncio de carta**

```yaml
POST /api/announcements
Headers:
Authorization: Bearer <token_jwt>

Request:
{
  "card": {
    "name": "Black Lotus",
    "edition": "Alpha",
    "condition": "NM",
    "price": 2500.00
  },
  "description": "Carta en perfecto estado, disponible para entrega local"
}

Response 201 Created:
{
  "id": 1,
  "card_id": 1,
  "seller_id": 1,
  "description": "Carta en perfecto estado, disponible para entrega local",
  "created_at": "2025-09-26T10:15:30Z"
}
```

---

### **3. Enviar mensaje relacionado con un anuncio**

```yaml
POST /api/messages
Headers:
Authorization: Bearer <token_jwt>

Request:
{
  "announcement_id": 1,
  "receiver_id": 2,
  "content": "Hola, ¿la carta sigue disponible?"
}

Response 201 Created:
{
  "id": 1,
  "sender_id": 1,
  "receiver_id": 2,
  "announcement_id": 1,
  "content": "Hola, ¿la carta sigue disponible?",
  "created_at": "2025-09-26T10:20:00Z"
}
```

---

Estos tres endpoints cubren el **flujo mínimo del MVP**: registro de usuarios, publicación de cartas y comunicación entre comprador y vendedor.
En fases posteriores se podrán añadir: login, búsqueda avanzada, filtrado, valoraciones y favoritos.


## 5. Historias de Usuario

---

### Historia de Usuario 1: Registro e inicio de sesión

**Como**: jugador de Magic que quiere comprar y vender cartas
**Quiero**: poder registrarme y acceder a la plataforma con mis credenciales
**Para**: poder gestionar mis anuncios y contactar con otros usuarios de forma segura

**Criterios de aceptación**:

* El usuario puede registrarse con email, username y contraseña.
* El sistema valida que el email y username sean únicos.
* El usuario puede iniciar sesión con sus credenciales válidas.
* Tras iniciar sesión, el usuario es redirigido a la página principal.
* Se muestra un mensaje de error claro si las credenciales son incorrectas.

---

### Historia de Usuario 2: Publicación de un anuncio de carta

**Como**: usuario registrado que desea vender una carta
**Quiero**: crear un anuncio con detalles de la carta (nombre, edición, estado, precio y descripción)
**Para**: que otros usuarios puedan encontrarla y contactarme para comprarla

**Criterios de aceptación**:

* El usuario puede crear un anuncio con todos los campos obligatorios.
* La carta queda asociada a su usuario y se almacena en la base de datos.
* El anuncio se muestra en el listado de cartas disponibles inmediatamente después de ser creado.
* Se valida que no se puedan publicar anuncios vacíos o sin datos esenciales.

---

### Historia de Usuario 3: Enviar mensaje a otro usuario

**Como**: usuario interesado en comprar una carta
**Quiero**: enviar un mensaje al vendedor a través de la plataforma
**Para**: poder preguntar detalles y coordinar la compra de manera segura sin usar medios externos

**Criterios de aceptación**:

* El usuario puede enviar un mensaje relacionado con un anuncio específico.
* El mensaje queda registrado en la base de datos y es accesible para ambos usuarios.
* El vendedor recibe notificación de un mensaje nuevo (visual en UI).
* Se valida que los mensajes no estén vacíos y estén asociados correctamente a usuarios y anuncio.


## 6. Tickets de Trabajo

---

### **Ticket 1: Backend – Endpoint de registro e inicio de sesión**

**Título:** Implementar registro y login de usuario con JWT

**Descripción:**  
Crear los endpoints en NestJS para permitir que los usuarios se registren y puedan iniciar sesión. Se debe asegurar la validación de datos, el hash de contraseñas y la generación de token JWT para la autenticación.

**Tareas:**  
- Crear módulo `AuthModule` con controladores y servicios.  
- Implementar endpoint `POST /auth/register`:
  - Validar email y username únicos.  
  - Hashear la contraseña con bcrypt.  
  - Guardar usuario en base de datos.  
- Implementar endpoint `POST /auth/login`:
  - Validar credenciales.  
  - Generar JWT con expiración de 1h.  
- Crear DTOs para request y response.  
- Añadir pruebas unitarias para servicios de autenticación.

**Criterios de aceptación:**  
- Un usuario puede registrarse y loguearse correctamente.  
- La contraseña no se almacena en texto plano.  
- Se devuelve un JWT válido al iniciar sesión.  
- Pruebas unitarias pasan exitosamente.

---

### **Ticket 2: Frontend – Página de registro e inicio de sesión**

**Título:** Crear vistas de registro y login en React con MaterialUI

**Descripción:**  
Diseñar e implementar las páginas de registro e inicio de sesión de usuario, integrando llamadas al backend mediante fetch/axios. Se debe asegurar validación de formularios y feedback al usuario.

**Tareas:**  
- Crear componentes `RegisterForm` y `LoginForm`.  
- Usar MaterialUI para inputs, botones y mensajes de error.  
- Implementar validación de formularios (email válido, campos obligatorios).  
- Integrar con API `/auth/register` y `/auth/login`.  
- Manejar almacenamiento de JWT en localStorage/sessionStorage.  
- Redirigir a Home tras login exitoso.  
- Mostrar mensajes claros de error en caso de fallo.

**Criterios de aceptación:**  
- El usuario puede registrarse y loguearse desde la UI.  
- El JWT se guarda correctamente y permite acceder a rutas protegidas.  
- Validación de formularios funciona correctamente.  
- Mensajes de error visibles y entendibles.

---

### **Ticket 3: Base de datos – Modelo de usuario y migraciones iniciales**

**Título:** Crear tabla de usuarios y migraciones en PostgreSQL

**Descripción:**  
Diseñar y crear la tabla de usuarios en PostgreSQL con todos los campos necesarios para el MVP. Implementar migraciones y seeds para pruebas iniciales.

**Tareas:**  
- Crear tabla `users` con campos: id (PK), email (unique, not null), username (unique, not null), password (not null), location (nullable).  
- Crear migración inicial con la estructura de la tabla.  
- Crear seed de usuario de prueba para desarrollo (`admin@example.com`).  
- Validar constraints de UNIQUE y NOT NULL.  
- Integrar con ORM (TypeORM o Prisma) usado en NestJS.

**Criterios de aceptación:**  
- La tabla se crea correctamente en la base de datos.  
- Migración y seed funcionan en entorno local.  
- Constraints UNIQUE y NOT NULL están aplicadas correctamente.  
- Los datos de prueba se pueden usar para testing del backend.

## 7. Pull Requests

> Documenta 3 de las Pull Requests realizadas durante la ejecución del proyecto

**Pull Request 1**
Documentación inicial técnica y de negocio.

**Pull Request 2**

**Pull Request 3**

