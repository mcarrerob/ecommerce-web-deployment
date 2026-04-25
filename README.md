# Learning App E-commerce (Ubuntu / LAMP)

Este proyecto es una adaptación para Linux/Ubuntu de la app de ejemplo de e-commerce de KodeKloud.

## Tecnologías

- Linux (Ubuntu)
- Apache2
- MariaDB
- PHP
- HTML/CSS/JS

## Créditos

Proyecto original: `kodekloudhub/learning-app-ecommerce`.

## Despliegue en Ubuntu (local)

### 1. Instalar paquetes

```bash
sudo apt update
sudo apt install -y apache2 php libapache2-mod-php php-mysql mariadb-server git

## 📘 Lo que aprendí

Este proyecto me permitió reforzar y demostrar habilidades prácticas en administración de sistemas Linux y despliegue de aplicaciones web. Entre los aprendizajes más importantes:

### 🔹 Linux / Ubuntu
- Instalación y configuración de un entorno LAMP (Linux, Apache, MariaDB, PHP).
- Gestión de servicios con `systemctl` (iniciar, detener, reiniciar Apache y MariaDB).
- Manejo de permisos, rutas y estructura de directorios en `/var/www/html`.

### 🔹 Apache2
- Configuración de VirtualHosts.
- Copia y despliegue de archivos web en el directorio raíz del servidor.
- Reinicio y verificación del estado del servicio.

### 🔹 MariaDB
- Creación de bases de datos y usuarios con privilegios específicos.
- Importación de datos desde scripts SQL.
- Conexión de PHP a MariaDB mediante variables de entorno.

### 🔹 PHP
- Lectura de variables desde `.env`.
- Conexión a bases de datos usando `mysqli`.
- Renderizado dinámico de contenido (productos) desde la base de datos.

### 🔹 Git y GitHub
- Inicialización de repositorios desde cero.
- Limpieza de historial (`rm -rf .git`) para crear un proyecto propio.
- Configuración de remotos (HTTPS y SSH).
- Resolución de errores comunes de autenticación.
- Subida de commits y documentación profesional del proyecto.

### 🔹 Buenas prácticas
- Documentación clara y orientada a principiantes.
- Atribución correcta al proyecto original.
- Estructura de README profesional para portfolio.

