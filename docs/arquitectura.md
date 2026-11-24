# Arquitectura inicial del frontend

## Alcance

La aplicación de esta etapa es un frontend estático. El enlace de Figma compartido requiere iniciar sesión, así que las páginas y los estilos actuales se basan únicamente en los módulos descritos para CEA Vía. La distribución visual, los estados de pantalla y los recorridos deben contrastarse con el prototipo antes de completar cada módulo.

## Capas y responsabilidades

- **Páginas (`index.html`, `pages/`):** estructura y contenido semántico de cada vista.
- **Estilos (`css/style.css`):** variables visuales, componentes reutilizables, reglas generales y ajustes responsive en una sola hoja de estilos.
- **Scripts (`js/`):** espacio reservado para interacciones y validaciones sencillas que no requieran backend.
- **Recursos (`assets/`):** imágenes, iconos y fuentes propios del proyecto.
- **Documentación (`docs/`):** decisiones, arquitectura y guías del proyecto.

## Módulos identificados

Inicio, acceso, perfil, usuarios y roles, matrícula, documentos y pagos. Las páginas de módulos distintas de inicio y acceso son placeholders: no se implementan procesos de negocio, persistencia, permisos, carga de archivos ni transacciones.

## Límites de integración

No hay conexión a base de datos ni a servicios. Cuando se defina el backend Java, acordar sus contratos HTTP, autenticación, permisos y formatos de datos antes de conectar formularios o vistas. No colocar credenciales ni datos sensibles en el frontend.

## Convenciones

- Usar rutas relativas a la ubicación de cada página.
- Mantener HTML, CSS y JavaScript en sus carpetas respectivas.
- Preferir HTML semántico, etiquetas accesibles y componentes Bootstrap 5.
- Confirmar los breakpoints, componentes y navegación contra Figma antes de asumir decisiones visuales como definitivas.
