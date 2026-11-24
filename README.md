# CEA Vía

Plataforma web para apoyar la gestión de una academia de conducción: acceso, perfiles, usuarios y roles, matrículas, documentos y pagos.

> **Estado del diseño:** el enlace de Figma requiere iniciar sesión y no permitió consultar el prototipo. La estructura de esta etapa parte de los módulos descritos y queda pendiente de validación visual y de flujos contra el diseño.

## Objetivo general

Organizar el frontend inicial de CEA Vía con HTML5, CSS3, Bootstrap 5 y JavaScript básico, separando las páginas, estilos y recursos para facilitar su mantenimiento y futura integración con un backend Java.

## Tecnologías utilizadas

| Tecnología | Uso |
| --- | --- |
| HTML5 | Estructura semántica de las páginas |
| CSS3 | Estilos propios, variables y adaptación responsive |
| Bootstrap 5 | Sistema de grillas y componentes de interfaz |
| JavaScript | Interacciones sencillas del frontend |

Bootstrap se carga desde CDN. No se requiere gestor de paquetes ni servidor backend para esta etapa.

## Requisitos

- Navegador web actualizado.
- Conexión a Internet para cargar Bootstrap desde CDN.
- Python 3, solo si deseas usar el servidor local del ejemplo.
- Editor de código (opcional).

## Instalación y ejecución local

1. Clona el repositorio o descarga sus archivos.
2. Abre la carpeta del proyecto.
3. Inicia un servidor estático local desde la raíz, por ejemplo:

   ```bash
   python -m http.server 8000
   ```

4. Visita `http://localhost:8000` en el navegador.

También puedes abrir `index.html` directamente, aunque un servidor local ofrece una experiencia más consistente al navegar entre páginas.

## Estructura del proyecto

```text
CEA/
├── README.md
├── index.html
├── pages/
│   ├── login.html
│   ├── perfil.html
│   ├── usuarios.html
│   ├── matricula.html
│   ├── documentos.html
│   └── pagos.html
├── assets/
│   ├── img/
│   ├── icons/
│   └── fonts/
├── css/
│   └── style.css
├── js/
│   ├── main.js
│   └── validation.js
└── docs/
    └── arquitectura.md
```

## Módulos y páginas

| Módulo | Página | Alcance de esta etapa |
| --- | --- | --- |
| Inicio | `index.html` | Entrada a la plataforma y navegación a los módulos disponibles |
| Acceso | `pages/login.html` | Estructura de la pantalla de inicio de sesión; sin autenticación real |
| Perfil | `pages/perfil.html` | Punto de partida para la sección de perfil |
| Usuarios y roles | `pages/usuarios.html` | Punto de partida para la administración de usuarios y roles |
| Matrícula | `pages/matricula.html` | Punto de partida para el módulo de matrícula |
| Documentos | `pages/documentos.html` | Punto de partida para la consulta y gestión de documentos |
| Pagos | `pages/pagos.html` | Punto de partida para el módulo de pagos; sin procesamiento de transacciones |

Las páginas de módulos son esqueletos de navegación, no implementaciones completas de sus procesos. Su contenido y sus interacciones deben ajustarse después de validar el prototipo de Figma.

## Arquitectura frontend

- Cada página HTML mantiene su estructura separada de las hojas de estilo y los scripts.
- `style.css` reúne las variables de color y diseño, los componentes reutilizables, los estilos generales y las reglas responsive.
- `main.js` y `validation.js` quedan reservados para interacciones frontend sencillas. No realizan llamadas a servicios ni guardan datos.
- La descripción de responsabilidades y los límites de esta arquitectura están en [`docs/arquitectura.md`](docs/arquitectura.md).

## Estado actual

- **Preparación del frontend:** estructura y páginas iniciales.
- **Diseño:** pendiente de revisar el prototipo; el enlace compartido requiere acceso a Figma.
- **Backend y persistencia:** no implementados.
- **Autenticación y pagos:** no conectados a servicios reales.

## Tecnologías previstas para futuras etapas

**Java no se utiliza en esta etapa.** Su posible uso para el backend corresponde a una fase futura. La elección de framework, base de datos, contratos API, autenticación e integración de pagos queda pendiente de decisiones del proyecto. No se incluye Java, Spring Boot, Maven ni servicios backend en esta entrega.
