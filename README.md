# Sistema de gestion logistica

Aplicación web orientada a la administración de una empresa de logística,permite administrar una flota de camiones: choferes, viajes, cargas y notificaciones. Tiene dos tipos de usuario (administrador y empleado) con paneles distintos.

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
