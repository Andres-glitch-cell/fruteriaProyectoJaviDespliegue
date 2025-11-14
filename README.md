# 🥭 **La Frutería Online: Del Campo a tu Código**

<p align="center">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP"/>
  <img src="https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white" alt="MariaDB"/>
  <img src="https://img.shields.io/badge/Apache-D42029?style=for-the-badge&logo=apache&logoColor=white" alt="Apache"/>
  <img src="https://img.shields.io/badge/AWS_EC2-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=FF9900" alt="AWS EC2"/>
</p>

> **"¡La frutería es un negocio serio... y este código lo demuestra!"** 🍎

---

## 🎯 **Objetivo y Arquitectura**

Implementar una **aplicación web funcional** para una frutería virtual, demostrando el despliegue completo de una **arquitectura LAMP** (Linux, Apache, MariaDB, PHP) en **AWS EC2**.

### Habilidades demostradas:
- ✅ **CRUD completo** con MariaDB  
- ✅ **Conexión segura** entre PHP y base de datos  
- ✅ **Despliegue en la nube** (Ubuntu + Apache + AWS)  
- ✅ **Interfaz amigable** para clientes y administradores  

---

## 🌟 **¡Frescura Garantizada!**

> *"Del campo directo a tu navegador... con amor y código."* 🍉

---

## 🛠️ **Stack Tecnológico (La Receta Perfecta)**

| Componente | Rol en el Proyecto | Tema |
|-----------|---------------------|------|
| **HTML/CSS** | Estructura y estilo de la interfaz | 🎨 |
| **PHP** | Lógica de negocio y manejo de peticiones | 🐘 |
| **MariaDB** | Almacenamiento persistente del inventario | 💾 |
| **Apache2** | Servidor HTTP que expone la aplicación | ⚙️ |
| **Ubuntu (AWS EC2)** | Sistema operativo y plataforma cloud | ☁️ |

---

## 🍎 **Módulos de la Aplicación**

### 1. 🏠 **Página de Inicio (`index.php`)**
- Punto de entrada principal  
- Navegación a **Catálogo** y **Gestión de Inventario**

---

### 2. 🍉 **Catálogo de Productos (`catalogo.php`)**

| Funcionalidad | Descripción | Operación DB |
|--------------|-------------|--------------|
| **Visualización** | Muestra productos en tabla con imagen | `SELECT` |
| **Actualización** | Modifica stock en tiempo real | `UPDATE` |
| **Eliminación** | Da de baja productos | `DELETE` |

> **Requisito clave**: La DB debe contener inicialmente **'Fruta de la Pasión'** para validar conexión.

---

### 3. 📝 **Inventario / Insertar Producto (`inventario.php`)**

Formulario de alta con:
- Nombre
- Precio
- Cantidad
- URL de imagen

> Envío → `INSERT` directo en MariaDB

---

## ⚙️ **Guía de Despliegue y Configuración**

### A. **Estructura de la Base de Datos (MariaDB)**

```sql
-- 1. Crear la tabla 'productos'
CREATE TABLE productos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nombre VARCHAR(255) NOT NULL,
    precio DECIMAL(10, 2) NOT NULL,
    cantidad INT NOT NULL,
    imagen_url VARCHAR(255)
);

-- 2. Insertar el producto inicial (REQUISITO)
INSERT INTO productos (nombre, precio, cantidad, imagen_url)
VALUES (
  'Fruta de la Pasión',
  3.50,
  15,
  'https://placehold.co/100x100/FFD700/000000?text=Pasión'
);
