🥭 La Frutería Online: Del Campo a tu Código

<p align="center">
<!-- Insignias de Colores y Tecnologías -->
<img src="https://www.google.com/search?q=https://img.shields.io/badge/PHP-777BB4%3Fstyle%3Dfor-the-badge%26logo%3Dphp%26logoColor%3Dwhite" alt="Hecho con PHP"/>
<img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="Base de Datos MariaDB"/>
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Apache-D42029%3Fstyle%3Dfor-the-badge%26logo%3Dapache%26logoColor%3Dwhite" alt="Servidor Apache"/>
<img src="https://www.google.com/search?q=https://img.shields.io/badge/AWS%2520EC2-232F3E%3Fstyle%3Dfor-the-badge%26logo%3Damazon-aws%26logoColor%3DFF9900" alt="Desplegado en AWS"/>
</p>

🎯 Objetivo y Arquitectura

El propósito de este proyecto es implementar una aplicación web funcional para una frutería, sirviendo como demostración del proceso de despliegue de una arquitectura LAMP completa (Linux, Apache, MariaDB, PHP) en un entorno de nube como AWS.

Se demuestran las siguientes habilidades:

Conexión y Manipulación de DB (CRUD): Lógica para leer, insertar y eliminar productos del catálogo de la frutería.

Despliegue en la Nube: Configuración de un servidor web Ubuntu/Apache en AWS.

🌟 ¡Frescura Garantizada!

"¡La frutería es un negocio serio... ¡y este código lo demuestra!"

🛠️ Stack Tecnológico (La Receta Perfecta)

El proyecto utiliza un stack clásico y robusto para el desarrollo web:

Componente

Rol en el Proyecto

Color / Tema

HTML/CSS

Estructura y Estilo de la Interfaz

🎨

PHP

Lógica de negocio y manejo de peticiones

🐘

MariaDB

Almacenamiento persistente del inventario

💾

Apache2

Servidor HTTP que expone la aplicación

⚙️

Ubuntu (AWS)

Sistema Operativo y Plataforma Cloud

☁️

🍎 Módulos de la Aplicación

La aplicación se estructura en tres archivos PHP principales:

1. 🏠 Página de Inicio (index.php)

Punto de entrada y navegación principal.

Ofrece enlaces a la vista del cliente (Catálogo) y a la vista de gestión (Inventario).

2. 🍉 Catálogo de Productos (catalogo.php)

Este es el módulo de visualización y gestión rápida:

Funcionalidad

Descripción

Operación de DB

Visualización

Muestra los productos en una tabla (Nombre, Precio, Cantidad, Imagen).

SELECT

Actualización

Permite modificar el stock (cantidad) de cualquier fruta.

UPDATE

Eliminación

Ofrece una interfaz para dar de baja productos del inventario.

DELETE

Requisito Clave: Inicialización de la DB

La base de datos debe inicializarse con el producto 'Fruta de la Pasión' para validar la correcta conexión antes del primer despliegue.

3. 📝 Inventario / Insertar Producto (inventario.php)

El formulario de alta que permite a los administradores añadir nuevos productos al inventario:

Campos: nombre, precio, cantidad y URL de la imagen.

El envío del formulario inserta los datos directamente en la tabla de MariaDB.

⚙️ Guía de Despliegue y Configuración

A. Estructura de la Base de Datos (MariaDB)

Conéctate a tu base de datos y ejecuta el siguiente script:

-- 1. Crear la tabla 'productos'
CREATE TABLE productos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(255) NOT NULL,
    precio DECIMAL(10, 2) NOT NULL,
    cantidad INT NOT NULL,
    imagen_url VARCHAR(255)
);

-- 2. Insertar el producto inicial (Requisito)
INSERT INTO productos (nombre, precio, cantidad, imagen_url) 
VALUES ('Fruta de la Pasión', 3.50, 15, '[https://placehold.co/100x100/FFD700/000000?text=Pasión](https://placehold.co/100x100/FFD700/000000?text=Pasión)');


B. Despliegue en Servidor (Ubuntu / Apache)

Transferencia: Copia todos los archivos (.html, .php) a la carpeta /var/www/html/ de tu servidor Ubuntu.

Configuración PHP: Asegúrate de que el código PHP tenga las credenciales correctas para la conexión a tu MariaDB (host, usuario, contraseña, nombre de la base de datos).

Permisos: Si encuentras errores de acceso, ajusta los permisos del directorio: sudo chown -R www-data:www-data /var/www/html/

🔗 Enlace al Proyecto Desplegado

<p align="center">
<!-- Botón de Acceso Directo con Color -->
<a href="[Inserta aquí la URL pública de tu máquina AWS]">
<img src="https://www.google.com/search?q=https://img.shields.io/badge/Ver%2520Aplicaci%C3%B3n%2520Web-Acceder%2520Ahora-007ACC%3Fstyle%3Dfor-the-badge%26logo%3Dworld%26logoColor%3Dwhite" alt="Botón de Acceso al Despliegue"/>
</a>
</p>

URL de la Aplicación (Página de Inicio):
[Insertar aquí la URL IP pública de tu instancia AWS]
