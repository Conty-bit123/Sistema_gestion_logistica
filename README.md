# Sistema de gestion logistica

Aplicación web orientada a la administración de una empresa de logística,permite administrar una flota de camiones: choferes, viajes, cargas y notificaciones. Tiene dos tipos de usuario (administrador y empleado) con paneles distintos.
Es un proyecto académico que busca resolver problemas típicos de la gestión manual: información descentralizada, datos duplicados, demoras administrativas y poca trazabilidad.

## Funcionalidades
**Administrador**
- Alta, búsqueda y gestión de camiones (patente, modelo, seguro, VTV, estado).
- Alta y gestión de empleados.
- Alta de viajes con carga, producto, empresa y camión asignado; búsqueda por estado o fecha.
- Notificaciones sobre el avance de los viajes.

**Empleado**
- Ver y actualizar el estado de sus viajes, con foto de respaldo.
- Ver su estado personal y sus notificaciones.

**General**
- Login con contraseñas hasheadas (`password_hash`).
- Registro de usuarios solo para empleados previamente cargados por el administrador, con reCAPTCHA.
- Recuperación de contraseña por mail con enlace temporal (1 hora).

## Tecnologías

PHP · MySQL (mysqli) · HTML/CSS · JavaScript/jQuery · PHPMailer · Google reCAPTCHA

## Base de datos

Base `logistica`, con estas tablas: `usuarios`, `empleados`, `camiones`, `viajes`, `cargas`, `productos`, `empresas`, `notificaciones` y `password_resets`.

## Estructura

| Archivo / carpeta | Función |
|---|---|
| `LoginCamiones.php`, `registro.php`, `registro_process.php` | Login y registro |
| `olvido_contrasena.html`, `enviar_correo.php`, `restablecer.php`, `actualizar_contrasena.php` | Recuperación de contraseña |
| `admin_index.php`, `admin.php` | Panel del administrador |
| `empleado.php`, `estado_personal.php` | Panel del empleado |
| `alta_viaje.php`, `guardar_viaje.php`, `gestionar_viaje.php`, `viajes.php` | Viajes |
| `form_camiones.php`, `form_empleados.php` | Formularios de camiones y empleados |
| `class_*.php` | Clases con las consultas a la base de datos |
| `notificacion.php`, `marcar_leidas.php`, `funciones.php` | Notificaciones |
| `conexion.php` | Conexión a MySQL |
| `PHPMailer/` | Librería de envío de correos |
| `fotos_viajes/`, `imagenes/`, `js/`, `*.css` | Recursos |

## Autores

Priscilla Guerrero y Ezequiel Larroza
