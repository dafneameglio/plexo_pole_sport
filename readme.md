# PLEXO Pole Sport

Sitio web desarrollado para **PLEXO Pole Sport** como proyecto final del curso Desarrollo Web de Coderhouse.

El sitio presenta información sobre el espacio, las clases y las actividades de PLEXO Pole Sport. Fue desarrollado con HTML5, CSS3 y SCSS, aplicando diseño responsive y el enfoque **Mobile First**.

## Sitio web

**Sitio publicado:** [https://plexopolesport.vercel.app/](https://plexopolesport.vercel.app/)

**Repositorio:** [https://github.com/dafneameglio/plexo_pole_sport](https://github.com/dafneameglio/plexo_pole_sport)

## Páginas del sitio

El proyecto está compuesto por cinco páginas:

- `index.html`: página principal.
- `pages/sobre_nosotros.html`: información sobre PLEXO y su filosofía.
- `pages/clases.html`: presentación de las clases y modalidades.
- `pages/faq.html`: preguntas frecuentes.
- `pages/contacto.html`: información y formulario de contacto.

## Tecnologías utilizadas

- HTML5.
- CSS3.
- SCSS.
- Bootstrap 5.3.8.
- AOS 2.3.4 (Animate On Scroll).
- Google Fonts (Abel).
- CSS Grid y Flexbox.
- Media Queries.
- Git y GitHub.
- Vercel.

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

### Visualizar el sitio

Se puede abrir `index.html` en un navegador o utilizar una extensión como Live Server desde Visual Studio Code.

### Compilar SCSS

El archivo principal de SCSS es `scss/main.scss`. Para compilar los estilos manualmente:

```bash
sass scss/main.scss styles/styles.css
```

Para observar y compilar automáticamente los cambios durante el desarrollo:

```bash
sass --watch scss/main.scss styles/styles.css
```

## Estructura del proyecto

```text
plexo_pole_sport/
│
├── index.html
├── pages/
│   ├── sobre_nosotros.html
│   ├── clases.html
│   ├── faq.html
│   └── contacto.html
│
├── assets/
│   └── imágenes del sitio
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
├── .gitignore
└── readme.md
```

## Arquitectura SCSS

Los estilos se organizan mediante parciales para mantener una estructura modular y facilitar el mantenimiento del código.

- `utilities/`: variables y mixins reutilizables.
- `base/`: estilos generales y tipografía.
- `layout/`: encabezado, pie de página y navegación.
- `components/`: botones, tarjetas, imágenes y grillas.

El archivo `main.scss` funciona como punto de entrada e importa los parciales mediante `@use`.

Se utilizan variables para centralizar valores visuales, mixins parametrizados para reutilizar estilos, anidamiento y `@extend` para compartir declaraciones.

El CSS compilado se encuentra en `styles/styles.css`.

## Diseño responsive

El sitio fue desarrollado siguiendo el enfoque **Mobile First**, adaptándose a dispositivos móviles, tablets y escritorio.

Se utilizan:

- CSS Grid.
- Flexbox.
- `grid-template-areas`.
- Unidades relativas como `fr`.
- Propiedad `gap`.
- Media Queries.

Los principales breakpoints utilizados son:

- `768px`: adaptación para tablets.
- `1024px`: adaptación para pantallas de escritorio.

Se verificó el comportamiento visual en diferentes anchos de pantalla, incluyendo 360, 768, 1024 y 1440 píxeles.

## Bootstrap

Se utiliza Bootstrap 5.3.8 para incorporar componentes y funcionalidades responsive.

Entre los componentes implementados se encuentran:

- Navbar responsive con menú hamburguesa.
- Carrusel de imágenes.
- Acordeón de preguntas frecuentes.

## Animaciones

El proyecto incorpora animaciones mediante:

- **AOS:** animaciones al desplazarse por la página.
- **CSS y SCSS:** transiciones para elementos interactivos.
- **`@keyframes`:** animaciones nativas para efectos visuales.

También se contemplan preferencias de accesibilidad relacionadas con la reducción del movimiento.

## SEO y accesibilidad

Se incorporaron mejoras de SEO on-page y accesibilidad:

- Etiquetas HTML semánticas.
- Títulos y descripciones específicos para cada página.
- Meta keywords por página.
- Textos alternativos descriptivos en las imágenes.
- Navegación accesible.
- Etiquetas asociadas a los campos del formulario.
- Consideraciones de contraste y estados de foco.
- Adaptaciones para usuarios que prefieren reducir las animaciones.

## Formulario de contacto

La página de contacto incluye un formulario visual para facilitar las consultas. El formulario forma parte de la interfaz estática y no cuenta con conexión a un backend.

## Despliegue

El sitio se encuentra publicado mediante **Vercel**, conectado al repositorio de GitHub.

Cada actualización enviada a la rama principal `main` permite generar un nuevo despliegue de producción.

**URL de producción:** [https://plexopolesport.vercel.app/](https://plexopolesport.vercel.app/)