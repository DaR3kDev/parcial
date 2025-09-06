# 📦 Inventory Management System (IMS) – LAMP en Docker

Este proyecto despliega el sistema **IMS (Inventory Management System)** en un entorno **LAMP** utilizando **Docker Compose**.  
El stack incluye **PHP 8.2 + Apache**, **MySQL 8.0** y **phpMyAdmin**.
---

## ⚙️ Instalación

1. **Clonar el repositorio del proyecto**
```bash
   git clone https://github.com/fizzywhizbang/ims.git
   cd ims
````

2. **Levantar los contenedores**

```bash
docker-compose up -d --build
```

---

## 🗄️ Configuración de la base de datos

1. Acceder a **phpMyAdmin** en 👉 [http://localhost:8081](http://localhost:8081)

   * Usuario: `root`
   * Contraseña: `root`

2. Seleccionar la base `imsdb` y **importar el archivo SQL** incluido en el proyecto (`ims.sql` o dump que trae el repositorio).

3. Verificar que las tablas como `ims_users`, `ims_system`, etc. estén creadas.

---

## 🔑 Credenciales de acceso

Usuarios por defecto (en `ims_users`):

* **Usuario:** `admin`
  **Contraseña:** `admin`
* **Usuario:** `test`
  **Contraseña:** *(vacío)*

> Si no funciona, actualizar el password con:
>
> ```sql
> UPDATE ims_users 
> SET password = MD5('admin') 
> WHERE username = 'admin';
> ```

---

## 🌐 Acceso a la aplicación

* **IMS App:** [http://localhost:8080](http://localhost:8080)
* **phpMyAdmin:** [http://localhost:8081](http://localhost:8081)
---
¿Quieres que te lo prepare también con los **comandos paso a paso** que debes mostrar en clase (desde `git clone` hasta `docker-compose up`), para que lo uses como guía en el parcial?
```
