# 🎓 CampusHub - Sistema de Estilos SCSS

Sistema de diseño modular y escalable para plataformas educativas, construido con SCSS y siguiendo las mejores prácticas de arquitectura CSS.

## 📋 Tabla de Contenidos

- [Características](#-características)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Instalación](#-instalación)
- [Uso](#-uso)
- [Componentes](#-componentes)
- [Variables y Personalización](#-variables-y-personalización)
- [Contribuir](#-contribuir)

## ✨ Características

- 🎨 **Sistema de diseño completo** con paleta de colores académica profesional
- 📦 **Arquitectura modular** con SCSS organizado en componentes reutilizables
- 📱 **Diseño responsivo** con breakpoints definidos
- ♿ **Accesibilidad** con estados de foco WCAG y contraste adecuado
- 💬 **Comentarios en español** detallados en todo el código SCSS
- 🚫 **Sin estilos inline** - Todo exportado con variables y clases de utilidad
- 🎯 **Componentes listos** para login, registro, upload, alertas, formularios y más

## 📁 Estructura del Proyecto

```
EstilosScssProyectoIntegrado/
├── scss/
│   ├── _variables.scss      # Variables globales (colores, tipografía)
│   ├── _mixins.scss          # Mixins reutilizables (responsive, flex, grid)
│   ├── _reset.scss           # Normalización y clases de utilidad
│   ├── _main.scss            # Archivo orquestador principal
│   ├── components/           # Componentes reutilizables
│   │   ├── _buttons.scss     # Botones primarios y delineados
│   │   ├── _cards.scss       # Tarjetas y alertas
│   │   └── _inputs.scss      # Campos de entrada y formularios
│   ├── layout/               # Estructura de página
│   │   ├── _header.scss      # Cabecera y navegación
│   │   └── _footer.scss      # Pie de página
│   └── pages/                # Estilos específicos de páginas
│       ├── _home.scss        # Página de inicio
│       ├── _login.scss       # Página de login
│       ├── _register.scss    # Página de registro
│       └── _upload.scss      # Página de subida de archivos
├── Index.html                # Demo de todos los componentes
└── README.md                 # Este archivo
```

## 🚀 Instalación

### Prerrequisitos

- Node.js y npm instalados
- Sass instalado globalmente o como dependencia del proyecto

### Instalación de Sass

```bash
npm install -g sass
```

### Compilación

Para compilar el SCSS a CSS:

```bash
sass scss/_main.scss scss/campusHub.css
```

Para compilación automática en desarrollo:

```bash
sass --watch scss/_main.scss:scss/campusHub.css
```

## 💻 Uso

### Importar en tu HTML

```html
<link rel="stylesheet" href="scss/campusHub.css">
```

### Ejemplo de Uso de Componentes

```html
<!-- Botón Primario -->
<button class="boton-primario">Acción Principal</button>

<!-- Botón Delineado -->
<button class="boton-delineado">Acción Secundaria</button>

<!-- Alerta de Éxito -->
<div class="alerta exito">
    <strong>¡Éxito!</strong> Operación completada.
</div>

<!-- Tarjeta -->
<div class="tarjeta-sonido">
    <h3>Título de la Tarjeta</h3>
    <p>Contenido de la tarjeta...</p>
</div>
```

### Clases de Utilidad

El sistema incluye clases de utilidad para evitar estilos inline:

```html
<!-- Espaciado -->
<div class="mt-2">Margen superior 2rem</div>
<div class="mb-1">Margen inferior 1rem</div>

<!-- Layout -->
<div class="flex-gap">Contenedor flex con gap</div>
<div class="ancho-completo">Ancho 100%</div>

<!-- Texto -->
<div class="texto-centrado">Texto centrado</div>
<div class="texto-secundario">Texto secundario</div>

<!-- Separadores -->
<section class="separador-seccion">Sección con borde superior</section>
```

## 🎨 Componentes

### Botones

- `.boton-primario` - Botón de acción principal
- `.boton-delineado` - Botón de acción secundaria
- Estados: `:hover`, `:active`, `:disabled`, `:focus`

### Tarjetas y Alertas

- `.seccion-alterna` - Contenedor base para tarjetas
- `.tarjeta-sonido` - Tarjeta con diseño vertical
- `.alerta` - Sistema de alertas con variantes:
  - `.alerta.exito` - Mensaje de éxito
  - `.alerta.advertencia` - Mensaje de advertencia
  - `.alerta.error` - Mensaje de error
  - `.alerta.info` - Mensaje informativo

### Formularios

- Inputs: `input[type="text"]`, `input[type="email"]`, `input[type="password"]`
- `.barra-busqueda` - Input de búsqueda redondeado
- `.contenedor-inputs` - Grid responsivo para formularios
- `.grupo-input` - Contenedor de label + input

### Layout

- `.cabecera-principal` - Header con navegación
- `.pie-pagina-principal` - Footer con columnas
- `.contenedor` - Contenedor centrado con max-width

### Páginas

- `.pagina-login` - Página de inicio de sesión
- `.pagina-registro` - Página de registro
- `.pagina-upload` - Página de subida de archivos
- `.zona-arrastre` - Área de drag & drop

## 🎨 Variables y Personalización

### Colores Base

```scss
$color-fondo-base: #f2eef0;           // Gris rosado claro
$color-interactivo-principal: #009acd; // Azul cerúleo
$color-borde-estructura: #093370;      // Azul marino profundo
```

### Colores de Texto

```scss
$color-texto-titulo-h1: #093370;  // Azul marino
$color-texto-subtitulo: #1a4d7a;  // Azul intermedio
$color-texto-secundario: #4a4a4a; // Gris oscuro
```

### Tipografía

```scss
$fuente-principal: "Open Sans", Arial, sans-serif;
$peso-regular: 400;
$peso-semi-negrita: 600;
$peso-negrita: 700;
```

Para personalizar los colores, edita el archivo `scss/_variables.scss` y recompila.

## 📱 Responsive Design

El sistema incluye mixins para diseño responsivo:

```scss
@include responsive(movil) {
    // Estilos para móviles (max-width: 768px)
}

@include responsive(tablet) {
    // Estilos para tablets (max-width: 992px)
}

@include responsive(escritorio) {
    // Estilos para escritorio (min-width: 993px)
}
```

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/NuevaCaracteristica`)
3. Commit tus cambios (`git commit -m 'Añadir nueva característica'`)
4. Push a la rama (`git push origin feature/NuevaCaracteristica`)
5. Abre un Pull Request

### Guía de Estilo

- Todos los comentarios deben estar en español
- Usa el formato simple `// Comentario` sin decoraciones
- Mantén la estructura modular del proyecto
- Usa variables para todos los valores (sin hardcoding)
- Sigue la nomenclatura BEM cuando sea apropiado

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo LICENSE para más detalles.

## 👥 Autores

- **Juan Carlos Dorado Lopez** - *Desarrollo inicial*

## 🙏 Agradecimientos

- Inspirado en las mejores prácticas de arquitectura CSS/SCSS
- Diseñado para plataformas educativas modernas
- Construido con accesibilidad y usabilidad en mente

---

⭐ Si este proyecto te ha sido útil, considera darle una estrella en GitHub!
