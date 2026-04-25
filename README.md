# 🛒 Learning App E‑commerce (Ubuntu / LAMP)

Este proyecto es una adaptación para Linux/Ubuntu del repositorio original de KodeKloud.
El objetivo es aprender a desplegar una aplicación web sencilla utilizando Apache2, PHP y MariaDB, además de practicar Git, GitHub y documentación profesional.

## 🚀 Tecnologías utilizadas

- Linux (Ubuntu)
- Apache2
- MariaDB
- PHP
- HTML / CSS / JavaScript
- Git & GitHub

## 📁 Estructura del proyecto

.
├── assets/
│   └── db-load-script.sql     # Script SQL con los productos
├── css/
├── js/
├── img/
├── index.php                  # Archivo principal PHP
└── README.md

## 🧰 Instalación en Ubuntu (LAMP)

### 1. Instalar dependencias

sudo apt update
sudo apt install -y apache2 php libapache2-mod-php php-mysql mariadb-server git

### 2. Configurar MariaDB

sudo mysql

Dentro del cliente:

CREATE DATABASE ecomdb;
CREATE USER 'ecomuser'@'localhost' IDENTIFIED BY 'ecompassword';
GRANT ALL PRIVILEGES ON ecomdb.* TO 'ecomuser'@'localhost';
FLUSH PRIVILEGES;
EXIT;

### 3. Importar los datos de productos

sudo mysql ecomdb < assets/db-load-script.sql

### 4. Copiar el proyecto al directorio web

sudo rm -rf /var/www/html/*
sudo cp -r . /var/www/html/

### 5. Crear archivo .env

sudo bash -c 'cat > /var/www/html/.env << "EOT"
DB_HOST=localhost
DB_USER=ecomuser
DB_PASSWORD=ecompassword
DB_NAME=ecomdb
EOT'

### 6. Reiniciar Apache

sudo systemctl restart apache2

Abrir en el navegador:
http://localhost

## 🧪 Probar desde otra máquina en la misma red

1. Obtener IP del servidor:

ip a

2. Desde otra máquina:

curl http://IP_DEL_SERVIDOR

O abrir en el navegador.

## 📘 Lo que aprendí

Este proyecto me permitió reforzar y demostrar habilidades prácticas en administración de sistemas Linux y despliegue de aplicaciones web. Entre los aprendizajes más importantes:

### Linux / Ubuntu
- Instalación y configuración de un entorno LAMP (Linux, Apache, MariaDB, PHP).
- Gestión de servicios con systemctl.
- Manejo de permisos y estructura de directorios en /var/www/html.

### Apache2
- Configuración de VirtualHosts.
- Despliegue de archivos web.
- Reinicio y verificación del servicio.

### MariaDB
- Creación de bases de datos y usuarios.
- Importación de datos desde scripts SQL.
- Conexión PHP ↔ MariaDB mediante variables de entorno.

### PHP
- Lectura de variables desde .env.
- Conexión a bases de datos usando mysqli.
- Renderizado dinámico de productos desde la base de datos.

### Git y GitHub
- Inicialización de repositorios desde cero.
- Limpieza de historial (rm -rf .git) para crear un proyecto propio.
- Configuración de remotos (HTTPS y SSH).
- Resolución de errores comunes de autenticación.
- Subida de commits y documentación profesional.

### Buenas prácticas
- Documentación clara y orientada a principiantes.
- Atribución correcta al proyecto original.
- Estructura de README profesional para portfolio.

## 🏷 Créditos

Proyecto original:
https://github.com/kodekloudhub/learning-app-ecommerce

Adaptado para Ubuntu/LAMP por Maria.
