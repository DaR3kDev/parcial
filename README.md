
# 📦 Inventory Management System (IMS) – LAMP en Docker

Este proyecto despliega el sistema **IMS (Inventory Management System)** en un entorno **LAMP** usando **Docker Compose**. El stack utilizado: **PHP 8.2 + Apache**, **MySQL 8.0** y **phpMyAdmin**.

---
## ⚙️ Requisitos previos
- Docker  
- Docker Compose  
- Git
---

## 🧭 Instalación (rápida)

1. Clonar el repositorio:
```bash
git clone https://github.com/fizzywhizbang/ims.git
cd ims
````

2. Levantar contenedores (con build por si usas Dockerfile personalizado):

```bash
docker-compose up -d --build
```

---

## 🗄️ Configuración de la base de datos

1. Acceder a **phpMyAdmin**: `http://localhost:8081`

   * Usuario: `root`
   * Contraseña: `root`

2. Seleccionar la base `imsdb` y **importar** el dump SQL incluido en el proyecto (por ejemplo `ims.sql`).

3. Verificar que existan tablas como `ims_users`, `ims_system`, `ims_product`, etc.

---

## 🔑 Credenciales (por defecto)

Usuarios en `ims_users` (según el dump importado):

* **Usuario:** `admin`
  **Contraseña:** `admin`

* **Usuario:** `test`
  **Contraseña:** *(vacío)*

> Si `admin` no funciona, ejecutar en phpMyAdmin:
>
> ```sql
> UPDATE ims_users 
> SET password = MD5('admin') 
> WHERE username = 'admin';
> ```

---

## 🌐 Acceso a la aplicación
* **IMS App:** `http://localhost:8080`
* **phpMyAdmin:** `http://localhost:8081`
--
