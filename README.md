# 🎨 CampusHub - Sistema de Diseño SCSS

> Arquitectura de estilos SCSS modular y escalable para plataformas educativas. Este repositorio centraliza la identidad corporativa, componentes reutilizables y guías de implementación para proyectos académicos.

[![SCSS](https://img.shields.io/badge/SCSS-CC6699?style=for-the-badge&logo=sass&logoColor=white)](https://sass-lang.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/es/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/es/docs/Web/CSS)

---

## 📋 Tabla de Contenidos

- [Características Principales](#-características-principales)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Instalación y Uso](#-instalación-y-uso)
- [Arquitectura SCSS](#-arquitectura-scss)
- [Sistema de Diseño](#-sistema-de-diseño)
- [Componentes](#-componentes)
- [Páginas](#-páginas)
- [Personalización](#-personalización)
- [Guía de Contribución](#-guía-de-contribución)
- [Licencia](#-licencia)

---

## ✨ Características Principales

### 🎯 Sistema Modular
- **Arquitectura SCSS organizada** siguiendo la metodología 7-1 Pattern
- **Componentes reutilizables** independientes y fácilmente integrables
- **Variables centralizadas** para mantener consistencia visual
- **Mixins avanzados** para responsive design y utilidades comunes

### 🎨 Identidad Visual Profesional
- **Paleta de colores académica** cuidadosamente seleccionada
- **Tipografía moderna** con Open Sans y Fira Code
- **Sistema de espaciado consistente** basado en rem
- **Accesibilidad WCAG 2.1** con estados de foco visibles

### 📱 Diseño Responsive
- **Mobile-first approach** con breakpoints optimizados
- **Grid system flexible** con CSS Grid y Flexbox
- **Componentes adaptables** a diferentes tamaños de pantalla
- **Navegación responsive** con menú colapsable

### 🚀 Optimización y Rendimiento
- **CSS compilado optimizado** con source maps
- **Selectores eficientes** sin anidación excesiva
- **Transiciones suaves** con aceleración por hardware
- **Carga rápida** con estilos minificados

---

## 📁 Estructura del Proyecto

```
EstilosScssProyectoIntegrado/
│
├── Index.html                    # Demo completa de todos los componentes
├── README.md                     # Documentación del proyecto
│
├── assets/
│   └── img/
│       └── logo.png.png         # Logo de CampusHub
│
└── scss/
    ├── CampusHub.scss           # Archivo principal de compilación
    ├── CampusHub.css            # CSS compilado (generado)
    ├── CampusHub.css.map        # Source map para debugging
    │
    ├── _variables.scss          # Variables globales de diseño
    ├── _mixins.scss             # Mixins reutilizables
    ├── _reset.scss              # Reset CSS normalizado
    ├── _main.scss               # Orquestador de imports
    │
    ├── components/              # Componentes reutilizables
    │   ├── _buttons.scss        # Estilos de botones
    │   ├── _cards.scss          # Tarjetas y alertas
    │   └── _inputs.scss         # Campos de entrada
    │
    ├── layout/                  # Estructura de layout
    │   ├── _header.scss         # Cabecera y navegación
    │   └── _footer.scss         # Pie de página
    │
    └── pages/                   # Estilos específicos de páginas
        ├── _home.scss           # Página de inicio
        ├── _login.scss          # Página de login
        ├── _register.scss       # Página de registro
        └── _upload.scss         # Página de subida de archivos
```

---

## 🚀 Instalación y Uso

### Prerrequisitos

- **Navegador web moderno** (Chrome, Firefox, Safari, Edge)
- **Compilador SCSS** (Dart Sass, Node-sass, o Live Sass Compiler para VS Code)
- **Editor de código** (VS Code recomendado)

### Instalación Rápida

1. **Clonar el repositorio**
```bash
git clone https://github.com/tu-usuario/EstilosScssProyectoIntegrado.git
cd EstilosScssProyectoIntegrado
```

2. **Compilar SCSS** (si usas Dart Sass)
```bash
sass scss/CampusHub.scss scss/CampusHub.css --watch
```

3. **Abrir en el navegador**
```bash
# Abre Index.html en tu navegador
# O usa un servidor local como Live Server
```

### Uso en Proyectos Existentes

#### Opción 1: Importar CSS Compilado
```html
<link rel="stylesheet" href="ruta/a/scss/CampusHub.css">
```

#### Opción 2: Importar SCSS Modular
```scss
// En tu archivo SCSS principal
@use 'ruta/a/scss/variables' as *;
@use 'ruta/a/scss/mixins' as *;
@use 'ruta/a/scss/components/buttons';
```

#### Opción 3: Copiar Componentes Específicos
Copia solo los archivos que necesites:
- `_variables.scss` (requerido)
- Componentes específicos de la carpeta `components/`
- Páginas específicas de la carpeta `pages/`

---

## 🏗️ Arquitectura SCSS

### Metodología 7-1 Pattern

Este proyecto sigue el patrón 7-1 adaptado para máxima modularidad:

```scss
// CampusHub.scss - Punto de entrada
@use 'main';
```

```scss
// _main.scss - Orquestador
@use 'variables';
@use 'mixins';
@use 'reset';
@use 'layout/header';
@use 'layout/footer';
@use 'components/buttons';
@use 'components/cards';
@use 'components/inputs';
@use 'pages/home';
@use 'pages/login';
@use 'pages/register';
@use 'pages/upload';
```

### Orden de Carga

1. **Configuración** → Variables y mixins
2. **Base** → Reset CSS
3. **Layout** → Estructura global (header, footer)
4. **Componentes** → Elementos reutilizables
5. **Páginas** → Estilos específicos de vistas

---

## 🎨 Sistema de Diseño

### Paleta de Colores

#### Colores Principales
```scss
$color-fondo-base: #f2eef0;           // Gris rosado claro
$color-interactivo-principal: #009acd; // Azul cerúleo
$color-borde-estructura: #093370;      // Azul marino profundo
$color-texto-principal: #000000;       // Negro
```

#### Colores de Texto
```scss
$color-texto-titulo-h1: #093370;       // Azul marino
$color-texto-subtitulo: #1a4d7a;       // Azul intermedio
$color-texto-secundario: #4a4a4a;      // Gris oscuro
$color-texto-deshabilitado: #999999;   // Gris medio
```

#### Estados Interactivos
```scss
$color-hover-interactivo: #007ba3;     // Hover azul oscuro
$color-activo-interactivo: #005f82;    // Estado activo
$color-deshabilitado-interactivo: #b3d9e8; // Deshabilitado
$sombra-foco-accesibilidad: #009acd;   // Foco WCAG
```

#### Alertas y Retroalimentación
```scss
$color-alerta-exito: #2d7a4f;          // Verde académico
$color-alerta-advertencia: #d68e2e;    // Naranja conservador
$color-alerta-error: #c4324d;          // Rojo profesional
$color-alerta-info: #009acd;           // Azul informativo
```

#### Fondos Estructurales
```scss
$color-fondo-puro: #ffffff;            // Blanco puro
$color-fondo-tarjeta: #ffffff;         // Fondo de tarjetas
$color-fondo-barra-lateral: #e8e4e6;   // Gris claro
$color-fondo-pie-pagina: #093370;      // Azul marino
```

#### Acentos Académicos
```scss
$color-acento-resaltado: #fff4cc;      // Amarillo marcador
$acento-borde-cita: #009acd;           // Borde de citas
$acento-fondo-cita: #f7fbfd;           // Fondo de citas
$acento-fondo-codigo: #f5f5f5;         // Fondo de código
$acento-texto-codigo: #2c3e50;         // Texto de código
```

### Tipografía

#### Familias de Fuentes
```scss
$fuente-principal: "Open Sans", Arial, sans-serif;
$fuente-codigo: "Consolas", "Monaco", "Courier New", monospace;
$fuente-cita: italic;
```

#### Pesos de Fuente
```scss
$peso-regular: 400;
$peso-semi-negrita: 600;
$peso-negrita: 700;
```

#### Escala Tipográfica
```css
h1 { font-size: 2.5rem; }    /* 40px */
h2 { font-size: 2rem; }      /* 32px */
h3 { font-size: 1.5rem; }    /* 24px */
p  { font-size: 1rem; }      /* 16px */
small { font-size: 0.875rem; } /* 14px */
```

### Mixins Disponibles

#### Responsive Design
```scss
@include responsive(movil) {
  // Estilos para móvil (max-width: 768px)
}

@include responsive(tablet) {
  // Estilos para tablet (max-width: 992px)
}

@include responsive(escritorio) {
  // Estilos para escritorio (min-width: 993px)
}
```

#### Flexbox Centrado
```scss
@include flex-center;
// Genera: display: flex; justify-content: center; align-items: center;
```

#### Grid Automático
```scss
@include grid-auto(250px, 1rem);
// Genera grid responsive con columnas mínimas de 250px y gap de 1rem
```

---

## 🧩 Componentes

### 1. Botones (`_buttons.scss`)

#### Botón Primario
```html
<button class="boton-primario">Texto del Botón</button>
<button class="boton-primario" disabled>Deshabilitado</button>
```

**Características:**
- Fondo azul cerúleo (`#009acd`)
- Texto blanco con peso semi-negrita
- Transiciones suaves en hover/active
- Estados de foco accesibles (WCAG 2.1)
- Cursor `not-allowed` cuando está deshabilitado

#### Botón Delineado
```html
<button class="boton-delineado">Texto del Botón</button>
<button class="boton-delineado" disabled>Deshabilitado</button>
```

**Características:**
- Borde azul de 2px con fondo transparente
- Efecto de relleno sutil en hover (10% opacidad)
- Ideal para acciones secundarias
- Mismo sistema de accesibilidad que botón primario

### 2. Tarjetas (`_cards.scss`)

#### Tarjeta Estándar
```html
<div class="tarjeta-sonido">
  <h3>Título de la Tarjeta</h3>
  <p>Descripción del contenido...</p>
  <button class="boton-primario">Acción</button>
</div>
```

**Características:**
- Fondo blanco con borde sutil
- Sombra suave (`0 4px 6px rgba(0,0,0,0.05)`)
- Padding de 1.5em y border-radius de 6px
- Layout flex-column con gap de 1rem
- Responsive y adaptable

#### Sección Alterna
```html
<section class="seccion-alterna">
  <div class="contenedor">
    <!-- Contenido -->
  </div>
</section>
```

**Uso:** Contenedor genérico para secciones destacadas

### 3. Alertas (`_cards.scss`)

#### Tipos de Alertas
```html
<!-- Éxito -->
<div class="alerta exito">
  <strong>¡Éxito!</strong> Operación completada correctamente.
</div>

<!-- Información -->
<div class="alerta info">
  <strong>Información:</strong> Nueva versión disponible.
</div>

<!-- Advertencia -->
<div class="alerta advertencia">
  <strong>Advertencia:</strong> Tu sesión está a punto de expirar.
</div>

<!-- Error -->
<div class="alerta error">
  <strong>Error:</strong> No se pudo conectar con el servidor.
</div>
```

**Características:**
- Borde izquierdo de 5px con color temático
- Fondos con ajuste de luminosidad (+40%)
- Texto con contraste optimizado (-20% luminosidad)
- Border-radius de 4px
- Padding de 1em

#### Texto Resaltado en Alertas
```html
<div class="alerta info">
  Mensaje con <span class="textoResaltado">texto destacado</span>
</div>
```

### 4. Inputs (`_inputs.scss`)

#### Campos de Texto
```html
<div class="grupo-input">
  <label class="texto-secundario">Etiqueta</label>
  <input type="text" placeholder="Escribe algo...">
</div>

<div class="grupo-input">
  <label class="texto-secundario">Email</label>
  <input type="email" placeholder="tu@email.com">
</div>

<div class="grupo-input">
  <label class="texto-secundario">Contraseña</label>
  <input type="password" placeholder="********">
</div>
```

**Características:**
- Borde de 1px gris que cambia a azul en foco
- Box-shadow azul con 20% opacidad en estado activo
- Padding de 0.75rem
- Transiciones suaves (0.3s ease)
- Placeholder con color gris medio
- Estado deshabilitado con fondo gris rosado

#### Select
```html
<div class="grupo-input">
  <label class="texto-secundario">Selecciona una opción</label>
  <select>
    <option>Opción 1</option>
    <option>Opción 2</option>
    <option>Opción 3</option>
  </select>
</div>
```

#### Barra de Búsqueda
```html
<div class="grupo-input">
  <label class="texto-secundario">Buscar</label>
  <input type="text" class="barra-busqueda" placeholder="Buscar en CampusHub...">
</div>
```

**Características especiales:**
- Border-radius de 50px (completamente redondeada)
- Padding horizontal de 1.5rem
- Ideal para búsquedas globales

#### Contenedor de Inputs
```html
<div class="contenedor-inputs">
  <div class="grupo-input">...</div>
  <div class="grupo-input">...</div>
  <div class="grupo-input">...</div>
</div>
```

**Características:**
- Grid automático con columnas mínimas de 250px
- Gap de 1.5rem entre elementos
- Responsive: se adapta automáticamente

---

## 📄 Páginas

### 1. Header (`layout/_header.scss`)

```html
<header class="cabecera-principal">
  <div class="contenedor contenedor-header">
    <a href="#" class="logo">
      <img src="assets/img/logo.png" alt="Logo" class="icono-logo">
      CampusHub
    </a>
    
    <nav class="nav-principal">
      <ul>
        <li><a href="#" class="activo">Inicio</a></li>
        <li><a href="#">Cursos</a></li>
        <li><a href="#">Comunidad</a></li>
        <li><a href="#">Recursos</a></li>
      </ul>
    </nav>
  </div>
</header>
```

**Características:**
- Fondo blanco con borde inferior azul marino (2px)
- Logo con icono circular y tipografía negrita
- Navegación con efecto de subrayado animado
- Estado activo con color azul y peso negrita
- Responsive: menú se apila verticalmente en móvil

### 2. Footer (`layout/_footer.scss`)

```html
<footer class="pie-pagina-principal">
  <div class="contenedor">
    <div class="contenedor-footer">
      <div>
        <h4>CampusHub</h4>
        <p>Tu compañero en el viaje del aprendizaje.</p>
      </div>
      
      <div>
        <h4>Enlaces</h4>
        <ul>
          <li><a href="#">Inicio</a></li>
          <li><a href="#">Cursos</a></li>
          <li><a href="#">Blog</a></li>
        </ul>
      </div>
      
      <div>
        <h4>Soporte</h4>
        <p>ayuda@campushub.edu</p>
      </div>
    </div>
    
    <div class="copyright">
      © 2024 CampusHub. Todos los derechos reservados.
    </div>
  </div>
</footer>
```

**Características:**
- Fondo azul marino con texto blanco
- Grid responsive de 3 columnas (auto-fit)
- Títulos con borde inferior y color amarillo
- Enlaces con hover amarillo y subrayado
- Copyright centrado con borde superior

### 3. Página de Inicio (`pages/_home.scss`)

#### Grid de Dos Columnas
```html
<div class="grid-dos-columnas">
  <div class="tarjeta-sonido">...</div>
  <div class="tarjeta-sonido">...</div>
</div>
```

**Responsive:** Se convierte en 1 columna en móvil

#### Filtros de Categoría
```html
<div class="filtros-categoria">
  <button class="boton-primario">Todos</button>
  <button class="boton-delineado">Desarrollo</button>
  <button class="boton-delineado">Diseño</button>
  <button class="boton-delineado">Marketing</button>
</div>
```

**Características:**
- Flexbox con gap de 1rem
- Flex-wrap para múltiples líneas
- Ideal para navegación por categorías

### 4. Página de Login (`pages/_login.scss`)

```html
<section class="contenedor pagina-login">
  <div class="contenedor-formulario">
    <h2 style="text-align: center;">Iniciar Sesión</h2>
    <form>
      <div style="margin-bottom: 1rem;">
        <label for="email" class="texto-secundario">Correo Electrónico</label>
        <input type="email" id="email" placeholder="tu@email.com">
      </div>
      <div style="margin-bottom: 1rem;">
        <label for="password" class="texto-secundario">Contraseña</label>
        <input type="password" id="password" placeholder="********">
      </div>
      <button type="submit" class="boton-primario" style="width: 100%;">Entrar</button>
    </form>
  </div>
</section>
```

**Características:**
- Centrado vertical y horizontal con flexbox
- Formulario con ancho máximo de 400px
- Fondo blanco con sombra suave
- Border-radius de 8px
- Altura mínima de 80vh para centrado vertical

### 5. Página de Registro (`pages/_register.scss`)

```html
<section class="contenedor pagina-registro">
  <div class="contenedor-formulario">
    <h2 style="text-align: center;">Crear Cuenta</h2>
    <form>
      <div class="fila-nombres">
        <div>
          <label for="nombre" class="texto-secundario">Nombre</label>
          <input type="text" id="nombre" placeholder="Juan">
        </div>
        <div>
          <label for="apellido" class="texto-secundario">Apellido</label>
          <input type="text" id="apellido" placeholder="Pérez">
        </div>
      </div>
      
      <div style="margin-bottom: 1rem;">
        <label for="email" class="texto-secundario">Correo Electrónico</label>
        <input type="email" id="email" placeholder="tu@email.com">
      </div>
      
      <div class="terminos">
        <input type="checkbox" id="terminos">
        <label for="terminos">Acepto los términos y condiciones</label>
      </div>
      
      <button type="submit" class="boton-primario" style="width: 100%;">Registrarse</button>
    </form>
  </div>
</section>
```

**Características:**
- Ancho máximo de 600px (más amplio que login)
- Fila de nombres con grid 2 columnas
- Checkbox de términos con flexbox
- Responsive: nombres se apilan en móvil

### 6. Página de Subida de Archivos (`pages/_upload.scss`)

```html
<section class="contenedor pagina-upload">
  <h2>Subida de Archivos</h2>
  
  <div class="zona-arrastre">
    <div class="icono-upload">☁️</div>
    <p>Arrastra y suelta tus archivos aquí</p>
    <button class="boton-delineado">O selecciona archivos</button>
  </div>
  
  <div class="alerta info">
    <strong>Nota:</strong> Tamaño máximo: 50MB. Formatos: PDF, DOCX, JPG.
  </div>
</section>
```

**Características:**
- Zona de arrastre con borde punteado azul
- Fondo azul con 5% opacidad
- Hover cambia a 10% opacidad y borde más oscuro
- Icono grande (3rem) centrado
- Cursor pointer para indicar interactividad
- Transiciones suaves (0.3s ease)

---

## 🎯 Personalización

### Cambiar Colores Principales

Edita `scss/_variables.scss`:

```scss
// Cambia el color principal de azul a verde
$color-interactivo-principal: #28a745; // Verde

// Actualiza los estados relacionados
$color-hover-interactivo: darken(#28a745, 10%);
$color-activo-interactivo: darken(#28a745, 20%);
```

### Añadir Nuevos Breakpoints

Edita `scss/_mixins.scss`:

```scss
@mixin responsive($breakpoint) {
  @if $breakpoint == movil-pequeno {
    @media (max-width: 480px) {
      @content;
    }
  }
  // ... otros breakpoints
}
```

### Crear Nuevos Componentes

1. Crea un archivo en `scss/components/_mi-componente.scss`
2. Importa las variables necesarias:
```scss
@use '../variables' as *;
```
3. Define tus estilos
4. Importa en `scss/_main.scss`:
```scss
@use 'components/mi-componente';
```

### Extender Botones

```scss
// En tu archivo SCSS personalizado
.boton-peligro {
  @extend .boton-primario;
  background-color: $color-alerta-error;
  
  &:hover {
    background-color: darken($color-alerta-error, 10%);
  }
}
```

---

## 🛠️ Compilación SCSS

### Usando Dart Sass (Recomendado)

```bash
# Instalación global
npm install -g sass

# Compilación única
sass scss/CampusHub.scss scss/CampusHub.css

# Watch mode (recompilación automática)
sass scss/CampusHub.scss scss/CampusHub.css --watch

# Compilación comprimida para producción
sass scss/CampusHub.scss scss/CampusHub.css --style=compressed
```

### Usando VS Code Extension

1. Instala **Live Sass Compiler** de Glenn Marks
2. Configura en `settings.json`:
```json
{
  "liveSassCompile.settings.formats": [
    {
      "format": "expanded",
      "extensionName": ".css",
      "savePath": "/scss"
    }
  ],
  "liveSassCompile.settings.generateMap": true
}
```
3. Click en "Watch Sass" en la barra inferior

### Usando Node.js Script

Crea `package.json`:
```json
{
  "name": "campushub-styles",
  "version": "1.0.0",
  "scripts": {
    "build": "sass scss/CampusHub.scss scss/CampusHub.css",
    "watch": "sass scss/CampusHub.scss scss/CampusHub.css --watch",
    "build:prod": "sass scss/CampusHub.scss scss/CampusHub.css --style=compressed"
  },
  "devDependencies": {
    "sass": "^1.69.0"
  }
}
```

Ejecuta:
```bash
npm install
npm run watch
```

---

## 📚 Guías de Uso

### Integración en Proyectos HTML Estáticos

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mi Proyecto</title>
  
  <!-- Fuentes -->
  <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap" rel="stylesheet">
  
  <!-- Estilos CampusHub -->
  <link rel="stylesheet" href="scss/CampusHub.css">
</head>
<body>
  <!-- Tu contenido aquí -->
</body>
</html>
```

### Integración en Frameworks (React, Vue, Angular)

#### React
```jsx
// En tu componente
import './scss/CampusHub.css';

function MiComponente() {
  return (
    <button className="boton-primario">
      Click aquí
    </button>
  );
}
```

#### Vue
```vue
<template>
  <button class="boton-primario">Click aquí</button>
</template>

<style>
@import './scss/CampusHub.css';
</style>
```

#### Angular
```typescript
// En angular.json
"styles": [
  "src/scss/CampusHub.css"
]
```

---

## 🧪 Testing y Validación

### Validación CSS

```bash
# Usando W3C CSS Validator
npm install -g css-validator
css-validator scss/CampusHub.css
```

### Accesibilidad

- ✅ Contraste de colores WCAG AA compliant
- ✅ Estados de foco visibles (outline de 3px)
- ✅ Tamaños de fuente escalables (rem)
- ✅ Áreas de click mínimas (44x44px)

### Compatibilidad de Navegadores

| Navegador | Versión Mínima |
|-----------|----------------|
| Chrome    | 90+            |
| Firefox   | 88+            |
| Safari    | 14+            |
| Edge      | 90+            |

---

## 🤝 Guía de Contribución

### Flujo de Trabajo

1. **Fork** el repositorio
2. **Crea una rama** para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. **Commit** tus cambios (`git commit -m 'Añade nueva funcionalidad'`)
4. **Push** a la rama (`git push origin feature/nueva-funcionalidad`)
5. **Abre un Pull Request**

### Convenciones de Código

#### Nombres de Clases
- Usa **kebab-case**: `.boton-primario`, `.contenedor-formulario`
- Prefijos descriptivos: `.pagina-`, `.contenedor-`, `.grupo-`
- Evita nombres genéricos como `.box`, `.item`

#### Estructura de Archivos SCSS
```scss
// 1. Imports
@use '../variables' as *;

// 2. Comentarios descriptivos
// Descripción del componente

// 3. Estilos base
.mi-componente {
  // Propiedades
}

// 4. Modificadores
.mi-componente--variante {
  // Variaciones
}

// 5. Estados
.mi-componente:hover,
.mi-componente:focus {
  // Estados interactivos
}
```

#### Comentarios
```scss
// ✅ Buenos comentarios
// Botón principal para acciones primarias
// Ajuste de luminosidad para fondos de alerta

// ❌ Comentarios innecesarios
// Color azul
// Padding de 1rem
```

### Checklist de Pull Request

- [ ] El código compila sin errores
- [ ] Se han actualizado los comentarios
- [ ] Se ha probado en Chrome, Firefox y Safari
- [ ] Los cambios son responsive
- [ ] Se mantiene la accesibilidad WCAG 2.1
- [ ] Se ha actualizado la documentación si es necesario

---

## 📖 Recursos Adicionales

### Documentación Oficial
- [Sass Documentation](https://sass-lang.com/documentation)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### Herramientas Recomendadas
- [ColorZilla](https://www.colorzilla.com/) - Selector de colores
- [CSS Grid Generator](https://cssgrid-generator.netlify.app/) - Generador de grids
- [Can I Use](https://caniuse.com/) - Compatibilidad de navegadores

### Inspiración de Diseño
- [Dribbble](https://dribbble.com/tags/education) - Diseños educativos
- [Behance](https://www.behance.net/search/projects?search=education%20platform) - Plataformas educativas
- [Awwwards](https://www.awwwards.com/) - Mejores diseños web

---

## 📝 Changelog

### v1.0.0 (2024-12-01)
- ✨ Lanzamiento inicial del sistema de diseño
- 🎨 Paleta de colores académica completa
- 🧩 Componentes: botones, tarjetas, alertas, inputs
- 📄 Páginas: home, login, registro, upload
- 🏗️ Layout: header y footer responsive
- 📱 Sistema responsive mobile-first
- ♿ Accesibilidad WCAG 2.1 AA

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

```
MIT License

Copyright (c) 2024 CampusHub

Se concede permiso, de forma gratuita, a cualquier persona que obtenga una copia
de este software y archivos de documentación asociados (el "Software"), para usar
el Software sin restricciones, incluyendo sin limitación los derechos de usar,
copiar, modificar, fusionar, publicar, distribuir, sublicenciar y/o vender copias
del Software, y permitir a las personas a quienes se les proporcione el Software
hacer lo mismo, sujeto a las siguientes condiciones:

El aviso de copyright anterior y este aviso de permiso se incluirán en todas las
copias o porciones sustanciales del Software.

EL SOFTWARE SE PROPORCIONA "TAL CUAL", SIN GARANTÍA DE NINGÚN TIPO, EXPRESA O
IMPLÍCITA, INCLUYENDO PERO NO LIMITADO A LAS GARANTÍAS DE COMERCIABILIDAD,
IDONEIDAD PARA UN PROPÓSITO PARTICULAR Y NO INFRACCIÓN.
```

---

## 👥 Autores y Reconocimientos

### Equipo de Desarrollo
- **Arquitectura SCSS** - Sistema modular y escalable
- **Diseño Visual** - Paleta de colores académica profesional
- **Componentes** - Elementos reutilizables y accesibles

### Agradecimientos
- Comunidad de Sass por las mejores prácticas
- Google Fonts por Open Sans
- Inspiración en sistemas de diseño educativos modernos

---

## 📞 Soporte y Contacto

### ¿Necesitas Ayuda?

- 📧 **Email**: ayuda@campushub.edu
- 🐛 **Issues**: [GitHub Issues](https://github.com/tu-usuario/EstilosScssProyectoIntegrado/issues)
- 💬 **Discusiones**: [GitHub Discussions](https://github.com/tu-usuario/EstilosScssProyectoIntegrado/discussions)

### Preguntas Frecuentes

**¿Puedo usar este sistema en proyectos comerciales?**
Sí, está bajo licencia MIT que permite uso comercial.

**¿Cómo reporto un bug?**
Abre un issue en GitHub con una descripción detallada y pasos para reproducir.

**¿Aceptan contribuciones?**
¡Por supuesto! Lee la guía de contribución y envía tu PR.

**¿Hay soporte para temas oscuros?**
Actualmente no, pero está en el roadmap para futuras versiones.

---

## 🗺️ Roadmap

### v1.1.0 (Próximamente)
- [ ] Tema oscuro (dark mode)
- [ ] Más variantes de botones (éxito, peligro, advertencia)
- [ ] Componente de modal/diálogo
- [ ] Sistema de notificaciones toast
- [ ] Animaciones avanzadas

### v1.2.0 (Futuro)
- [ ] Componente de tabla responsive
- [ ] Sistema de tabs/pestañas
- [ ] Breadcrumbs de navegación
- [ ] Paginación
- [ ] Skeleton loaders

### v2.0.0 (Visión a Largo Plazo)
- [ ] Migración a CSS Variables
- [ ] Soporte para múltiples temas
- [ ] Componentes de gráficos
- [ ] Sistema de iconos integrado
- [ ] Documentación interactiva con Storybook

---

<div align="center">

**⭐ Si este proyecto te ha sido útil, considera darle una estrella en GitHub ⭐**

Hecho con ❤️ para la comunidad educativa

[⬆ Volver arriba](#-campushub---sistema-de-diseño-scss)

</div>
