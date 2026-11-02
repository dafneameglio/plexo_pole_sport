# PLEXO Pole Sport

Sitio web desarrollado para **PLEXO Pole Sport** como proyecto final del curso Desarrollo Web de Coderhouse.

El proyecto presenta información sobre el estudio, sus profesores, las clases y modalidades de entrenamiento, preguntas frecuentes y medios de contacto.

Se desarrolló utilizando HTML5, SCSS, CSS y Bootstrap, con un enfoque **Mobile First**, diseño responsive y criterios de accesibilidad y SEO on-page.

## Sitio web

**Sitio desplegado:** [Agregar URL de Vercel una vez realizado el despliegue]

## Páginas del sitio

El proyecto está compuesto por cinco páginas HTML:

- `index.html` — Página principal.
- `pages/sobre_nosotros.html` — Información sobre PLEXO y sus profesores.
- `pages/clases.html` — Clases y modalidades de entrenamiento.
- `pages/faq.html` — Preguntas frecuentes.
- `pages/contacto.html` — Información y formulario de contacto.

## Tecnologías utilizadas

- HTML5.
- CSS3.
- SCSS (Sass).
- Bootstrap 5.3.8.
- AOS (Animate On Scroll) 2.3.4.
- Google Fonts (Abel).
- CSS Grid.
- Flexbox.
- Media Queries.
- Git y GitHub.
- Vercel para el despliegue.

## Cómo descargar y ejecutar el proyecto

### Clonar el repositorio

Desde una terminal:

```bash
git clone https://github.com/dafneameglio/plexo_pole_sport.git
```

Ingresar a la carpeta:

```bash
cd plexo_pole_sport
```

### Ejecutar el proyecto

Para visualizar el sitio, se puede abrir `index.html` en un navegador o utilizar una extensión como Live Server desde Visual Studio Code.

Los recursos externos, como Bootstrap, AOS y Google Fonts, se cargan mediante CDN, por lo que requieren conexión a Internet.

### Compilar SCSS

Los estilos fuente se encuentran en la carpeta `scss/` y se compilan en `styles/styles.css`.

Para compilar automáticamente los cambios durante el desarrollo, ejecutar desde la raíz del proyecto:

```bash
sass --watch scss/main.scss styles/styles.css
```

Se requiere tener Sass instalado y disponible desde la terminal.

## Estructura del proyecto

```text
plexo_pole_sport/
│
├── index.html
│
├── pages/
│   ├── sobre_nosotros.html
│   ├── clases.html
│   ├── faq.html
│   └── contacto.html
│
├── scss/
│   ├── main.scss
│   ├── utilities/
│   │   ├── _variables.scss
│   │   └── _mixins.scss
│   ├── base/
│   │   ├── _base.scss
│   │   └── _tipografia.scss
│   ├── layout/
│   │   ├── _header.scss
│   │   ├── _footer.scss
│   │   └── _nav.scss
│   └── components/
│       ├── _buttons.scss
│       ├── _cards.scss
│       ├── _images.scss
│       └── _grids.scss
│
├── styles/
│   ├── styles.css
│   └── styles.css.map
│
├── assets/
│   └── ...
│
└── readme.md
```

## Arquitectura SCSS

Los estilos están organizados mediante parciales para facilitar el mantenimiento y la reutilización del código.

La estructura se divide en:

- **utilities/**: variables globales y mixins reutilizables.
- **base/**: estilos generales, configuración inicial y tipografía.
- **layout/**: encabezado, navegación y pie de página.
- **components/**: botones, tarjetas, imágenes y grillas.

El archivo `scss/main.scss` funciona como punto de entrada e importa los parciales mediante `@use`.

En el proyecto se aplican:

- Variables para centralizar colores y otros valores.
- Nesting para organizar selectores relacionados.
- Mixins con parámetros para reutilizar estilos.
- `@extend` mediante placeholders para compartir declaraciones.
- Media queries para adaptar los estilos a distintos dispositivos.

El CSS compilado se encuentra en `styles/styles.css`.

## Diseño responsive y Mobile First

El sitio fue desarrollado siguiendo el enfoque **Mobile First**: los estilos base contemplan primero las pantallas pequeñas y luego se incorporan adaptaciones para dispositivos de mayor tamaño.

Se utilizan principalmente los siguientes breakpoints:

```scss
@media (min-width: 768px) {
    // Adaptaciones para tablet
}

@media (min-width: 1024px) {
    // Adaptaciones para escritorio
}
```

Para conseguir una distribución adaptable se utilizan:

- CSS Grid.
- Flexbox.
- `grid-template-areas`.
- Unidades relativas como `fr`.
- `gap`.
- Media queries.

El diseño fue comprobado en diferentes tamaños de pantalla, incluyendo 360, 390, 768, 1024 y 1440 píxeles.

## Bootstrap

Se utiliza Bootstrap 5.3.8 para incorporar componentes y facilitar la adaptación responsive.

Entre sus implementaciones se encuentran:

- Navbar responsive con menú hamburguesa.
- Carrusel de imágenes.
- Acordeón de preguntas frecuentes.

Los componentes se personalizan mediante los estilos propios desarrollados en SCSS.

## Animaciones y efectos visuales

El sitio incorpora animaciones para acompañar la navegación y mejorar la experiencia visual.

### Librería AOS

Se utiliza AOS (Animate On Scroll) para aplicar animaciones a los elementos cuando ingresan en el área visible de la pantalla.

Se utilizan efectos como:

- `fade-up`.
- `fade-left`.
- `zoom-in`.

La configuración contempla una duración de 700 milisegundos, ejecución única y desplazamiento de 100 píxeles.

También se contempla la preferencia del sistema para reducir el movimiento mediante `prefers-reduced-motion`.

### Animaciones con CSS y SCSS

Se incorporan transiciones y animaciones propias mediante:

- `transition`.
- `@keyframes`.
- `transform`.
- `opacity`.

Estos efectos se aplican en botones, controles del carrusel, acordeón y elementos visuales del sitio.

## SEO y accesibilidad

Se incorporan mejoras de SEO on-page y accesibilidad:

- Títulos descriptivos y específicos para cada página.
- Meta descriptions individuales.
- Meta keywords específicas por página.
- Textos alternativos (`alt`) descriptivos en las imágenes.
- Uso de etiquetas HTML semánticas.
- Asociación entre etiquetas `label` y campos del formulario.
- Indicadores visuales de foco para elementos interactivos.
- Consideraciones de contraste de colores.
- Soporte para la preferencia de reducción de movimiento.

## Formulario de contacto

La página de contacto incluye un formulario con campos para nombre, correo electrónico y mensaje.

El formulario es parte de la interfaz visual del proyecto y actualmente no está conectado a un backend ni a un servicio externo de recepción de consultas.

## Despliegue

El proyecto se prepara para su publicación mediante **Vercel**, conectado al repositorio de GitHub.

Una vez realizado el despliegue, la URL pública se incorporará en la sección inicial de este README.

---

## Objetivo del proyecto

El objetivo del proyecto final es integrar los conocimientos adquiridos durante el curso Desarrollo Web, desarrollando un sitio estático de cinco páginas que combine estructura semántica, estilos avanzados, diseño responsive, componentes de Bootstrap, animaciones, SEO y accesibilidad.

Se busca construir una experiencia visual coherente con la identidad de PLEXO Pole Sport y facilitar el acceso a la información desde distintos dispositivos.