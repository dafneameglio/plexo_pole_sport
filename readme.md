# PLEXO Pole Sport

Sitio web desarrollado para **PLEXO Pole Sport** como proyecto de Desarrollo Web.

El sitio presenta información sobre las clases y actividades de PLEXO Pole Sport, utilizando HTML y CSS con un enfoque **Mobile First** y diseño responsive.

## Sitio web

[Visitar sitio](https://dafneameglio.github.io/plexo_pole_sport/)

## Cómo descargar y ejecutar el proyecto


### Clonar el repositorio

Desde una terminal:

```bash
git clone https://github.com/dafneameglio/plexo_pole_sport.git
```

Luego ingresar a la carpeta del proyecto:

```bash
cd plexo_pole_sport
```

### Ejecutar el proyecto

El proyecto está desarrollado con HTML, CSS y SCSS. No requiere instalación de dependencias de JavaScript.

Para visualizarlo, se puede abrir `index.html` en un navegador o utilizar una extensión como Live Server desde Visual Studio Code.

Para compilar automáticamente los cambios de SCSS durante el desarrollo, ejecutar desde la raíz del proyecto:

```bash
sass --watch scss/main.scss styles/styles.css
```


# Páginas evaluadas

Para la Preentrega 4 se consideran principalmente:

* `index.html` — página principal.
* `pages/clases.html` — página de clases.

Ambas páginas utilizan la hoja de estilos `styles/styles.css` y fueron desarrolladas contemplando diferentes tamaños de pantalla.

---

# Requisitos de la Preentrega 4

## Mobile First

El sitio fue desarrollado siguiendo el enfoque **Mobile First**.

Los estilos base se encuentran fuera de las media queries y están pensados inicialmente para pantallas pequeñas. Luego se incorporan adaptaciones para pantallas de mayor tamaño mediante:

```css
@media (min-width: 768px)
```

y:

```css
@media (min-width: 1024px)
```

Los estilos se encuentran en:

```text
styles/styles.css
```

Para comprobar el enfoque Mobile First, se puede abrir `index.html` o `pages/clases.html`, utilizar las herramientas para desarrolladores del navegador y probar diferentes anchos de viewport.

---

## CSS Grid

Se utiliza **CSS Grid** para organizar diferentes secciones del sitio.

El uso de Grid se encuentra principalmente en `pages/clases.html`, mediante contenedores como:

```css
.modalidad_sport
.modalidad_flexi
.modalidad_libre
.modalidad_straps
```

Estos contenedores utilizan:

```css
display: grid;
```

para organizar las imágenes y adaptar su distribución según el tamaño de pantalla.

---

## `grid-template-areas`

Se utiliza `grid-template-areas` para definir la distribución visual de los elementos dentro de las grillas.

Por ejemplo, en la sección de Pole Sport:

```css
grid-template-areas:
    "sofi_polesport"
    "josu_polesport"
    "lu_polesport";
```

En tamaños de pantalla mayores, la distribución se modifica mediante diferentes áreas, por ejemplo:

```css
grid-template-areas:
    "sofi_polesport lu_polesport"
    "josu_polesport lu_polesport";
```

Las áreas corresponden a las clases de los elementos HTML y permiten reorganizar visualmente el contenido mediante CSS Grid.

---

## Unidad `fr`

Dentro de las grillas se utiliza la unidad `fr` de CSS Grid.

La unidad `fr` representa una fracción del espacio disponible del contenedor.

Por ejemplo:

```css
grid-template-columns: 1fr 2fr;
```

También se utiliza:

```css
grid-template-columns: repeat(2, 1fr);
```

Esto permite distribuir el espacio disponible entre las columnas de manera flexible.

---

## `gap`

Se utiliza la propiedad `gap` para establecer espacios entre filas y columnas de los elementos organizados mediante Grid.

Por ejemplo:

```css
gap: 5px;
```

También se utiliza `gap` en elementos organizados mediante Flexbox.

---

## Breakpoint de `1024px`

El diseño incorpora el breakpoint:

```css
@media (min-width: 1024px)
```

A partir de este ancho se realizan modificaciones en la distribución de determinados elementos para adaptar el diseño a pantallas de escritorio.

Por ejemplo, en las modalidades de Pole Sport y Flexibilidad se modifica la distribución de las imágenes mediante CSS Grid.

---

## Diseño Responsive

El sitio fue desarrollado para adaptarse a diferentes tamaños de pantalla.

La adaptación responsive se realiza principalmente mediante:

* CSS Grid.
* `grid-template-areas`.
* Unidades relativas como `fr`.
* `gap`.
* Media queries.
* Breakpoints de `768px` y `1024px`.

### Cómo comprobar el responsive

1. Abrir `index.html` o `pages/clases.html`.
2. Abrir las herramientas para desarrolladores del navegador.
3. Activar el modo de dispositivo responsive.
4. Probar diferentes anchos de pantalla.
5. Observar cómo cambia la distribución de los elementos.

Se puede comprobar especialmente el comportamiento antes y después de los breakpoints de `768px` y `1024px`.

---

# Estructura del proyecto


plexo_pole_sport/
│
├── index.html
├── pages/
│   ├── sobre_nosotros.html
│   ├── clases.html
│   ├── faq.html
│   └── contacto.html
│
├── scss/
│   ├── main.scss
│   ├── utilities/
│   ├── base/
│   ├── layout/
│   └── components/
│
├── styles/
│   ├── styles.css
│   └── styles.css.map
│
├── images/
│   └── ...
│
└── readme.md

## Tecnologías utilizadas

* HTML5
* CSS3
* CSS Grid
* Flexbox
* Media Queries
* Bootstrap
* Git y GitHub

---

## Objetivo de la implementación

El objetivo de esta etapa del proyecto es construir una interfaz web estructurada y responsive, aplicando los conceptos de HTML y CSS trabajados durante el módulo, especialmente:

* Diseño Mobile First.
* CSS Grid.
* Flexbox.
* `grid-template-areas`.
* Unidades `fr`.
* `gap`.
* Media queries.
* Diseño responsive.

El proyecto continúa evolucionando en las siguientes etapas del curso, incorporando nuevas tecnologías y mejoras sobre la estructura desarrollada inicialmente.




## Evidencias

Las siguientes capturas permiten verificar la implementación responsive
y el uso de CSS Grid en las páginas evaluadas.

### Responsive

- `index-mobile-1.png`: vista mobile del inicio.
- `index-mobile-2.png`: continuación de la vista mobile del inicio.
- `index-tablet.png`: vista tablet del inicio.
- `index-desktop.png`: vista desktop del inicio.
- `clases-mobile-1.png`: vista mobile de la página de clases.
- `clases-mobile-2.png`: continuación de la vista mobile de la página de clases.
- `clases-desktop.png`: vista desktop de la página de clases.

### Código CSS

- `css-modalidad-straps-mobile-first.png`: implementación de CSS Grid
  en Mobile First para la modalidad Straps.
- `css-modalidad-straps-tablet-768px.png`: adaptación del Grid
  de Straps mediante el breakpoint de 768px.
- `css-breakpoint-1024px.png`: implementación del breakpoint
  de 1024px mediante `@media`.

## Animaciones y efectos visuales

El proyecto incorpora animaciones para mejorar la experiencia visual y acompañar la navegación por el sitio.

### Librería AOS

Se utiliza la librería AOS (*Animate On Scroll*) para aplicar animaciones a elementos cuando aparecen en el área visible de la pantalla.

La configuración incluye una duración de 700 milisegundos, la ejecución de las animaciones una sola vez y un desplazamiento de 100 píxeles.

Los efectos se aplican mediante atributos `data-aos`, utilizando animaciones como `fade-up`, `fade-left` y `zoom-in`.

### Animaciones con CSS y SCSS

También se utilizan transiciones CSS para generar efectos en botones, controles del carrusel y elementos interactivos.

Se incorporan animaciones nativas mediante `@keyframes`, combinando propiedades como `opacity` y `transform` para producir efectos de aparición y desplazamiento.

### Diseño responsive

El sitio contempla ajustes para pantallas pequeñas mediante media queries. Se adaptan los tamaños tipográficos y los espacios interiores del encabezado, pie de página y botones.

El diseño se verificó en anchos de pantalla de 360, 768, 1024 y 1440 píxeles.

## Arquitectura SCSS

Los estilos del proyecto se organizan mediante SCSS, utilizando parciales para separar las responsabilidades del código.

La carpeta `scss/` contiene:

- `utilities/`: variables y mixins reutilizables.
- `base/`: estilos generales y tipografía.
- `layout/`: estilos de encabezado, pie de página y navegación.
- `components/`: estilos de botones, tarjetas, imágenes y grillas.

El archivo `scss/main.scss` importa los parciales mediante `@use` y funciona como punto de entrada para compilar los estilos.

### Compilación de SCSS

El archivo fuente `scss/main.scss` se compila en `styles/styles.css`, que es la hoja de estilos utilizada por las páginas HTML.

Para compilar automáticamente los cambios durante el desarrollo, ejecutar desde la raíz del proyecto:

`sass --watch scss/main.scss styles/styles.css`
