---
documentclass: scrreprt
title: "HTML y CSS: PEC 1"
author: Ignacio Casares Ruiz
colorlinks: true
header-includes:
 - \usepackage{fvextra}
 - \DefineVerbatimEnvironment{Highlighting}{Verbatim}{breaklines,commandchars=\\\{\}}
---

## Pregunta 1. Sobre accesibilidad web.

### 1.1 ¿Qué entendemos por accesibilidad web?

La accesibilidad hace referencia a la propiedad de las páginas web de ser utilizada (o accessible) por la mayor cantidad de usuarios posible. Esto implica la implementación de aspectos que permitan que ciertas personas con una capacidad de interacción menor puedan interaccionar con los aspectos de la web en las condiciones similares a las del resto de usuarios, con el objetivo de proporcionar igualdad de acceso a ese servicio.

### 1.2 ¿Qué son las WCAG?

WCAG es un acrónimo de _Web Content Accessibility Guidelines_. Son una serie de directrices propugnadas por el Consorcio WWW (W3C) que describen cómo construir contenido web de forma que este sea más accesible para personas discapacitadas.

### 1.3 ¿Qué técnicas de accesibilidad has podido aplicar en los archivos de la parte práctica de esta PEC?

A través de la realización de esta práctica, he podido aplicar diferentes técnicas para adaptarla a los criterios de accesibilidad de la W3C:

* Se ha aplicado la técnica G94 «Providing short text alternative for non-text content that serves the same purpose and presents the same information as the non-text content» en los casos en los que se mostraban imágenes simples (situación A), como ha sido en la utilización del archivo `fakenews-pastors.jpg`; concretamente a través de H37: utilización del atributo `alt` en elementos `img`. Se ha hecho a través de una descripción en texto completa de la imagen en el atributo. Esto se ha realizado con el objetivo de responder al criterio de conformidad 1.1.1 «Non-text content», que corresponde a un nivel A.
* También se ha aplicado la técnica G95 «Providing short text alternatives that provide a brief description of the non-text content». La imagen `fakenews-trump-awards.jpg` muestra una captura de pantalla de una página web con una gran variedad de elementos en su interior (situación B). En este caso, a través, de nuevo, de H37, se ha realizado una descripción esta vez breve de la misma, en la que se resume el contenido de la captura. Esto responde al mismo criterio de conformidad 1.1.1 «Non-text content», que corresponde a un nivel A, de la misma forma que el punto anterior.
* Se han empleado las técnicas H48: «Using ol, ul and dl for lists or groups of links» y H42: «Using h1-h6 to identify headings», a través del empleo de las correspondientes etiquetas en los diferentes archivos `.html`, para satisfacer el criterio de conformidad 1.3.1 (Info and relationships), correspondiente al nivel A.
* Igualmente, se han empleado las técnicas C6: «Positioning content based on structural markup» y C8: «Using CSS letter-spacing to control spacing within a word». Tal y como se describe en [C6](https://www.w3.org/WAI/WCAG21/Techniques/css/C6.html), la estructura del artículo es mantenida cuando no se aplican la hoja de estilo CSS, de forma que el texto mantiene la progresividad en los casos en los que el intérprete no acepte CSS. En ocasiones también se ha usado [C8](https://www.w3.org/WAI/WCAG21/Techniques/css/C8.html) para mejorar la apariencia visual del texto aún manteniendo la progresividad: por ejemplo a través de la inclusión de la declaración `letter-spacing: 0.025em;` en el selector `main blockquote`. Se ha procurado, en la medida de lo posible, utilizar la técnica [C27](https://www.w3.org/WAI/WCAG21/Techniques/css/C27.html) para equiparar el orden del DOM al orden visual en la hoja de estilos, pero teniendo en cuenta que esta se comparte en tres archivos `.html` diferentes, existe cierta limitación en cuanto a su aplicación. Las técnicas descritas anteriormente se han empleado para satisfacer el criterio 1.3.2 «Meaningful Sequence», que corresponde a un nivel A. El empleo de C8 también permite satisfacer el criterio 1.4.12 «Text Spacing», nivel AA.
* A través de la técnica C14: «Using em units for font sizes», se ha asegurado que el tamaño del texto varía de forma relativa sin perder funcionalidad o contenido. Esto se ha realizado mediante el uso de `em` como unidad en la tipificación de los valores para las propiedades `font-size` en la hoja de estilos CSS. Esto permite satisfacer el criterio 1.4.4 «Resize text», que corresponde a un nivel AA.
* Mediante la técnica C38: «Using CSS width, max-width and flexbox to fit labels and inputs», se ha asegurado que no es necesario realizar _scrolling_ horizontal incluso cuando se produce un cambio de tamaño de la página de más del 40%. Esto se ha conseguido a través del uso de las propiedades `width` y `max-width` en las diferentes secciones, asociadas a un valor percentual que estabiliza y asegura que la estructura permanece fija ante variaciones en el tamaño de la página de hasta un +400%. Esto permite satisfacer el criterio 1.4.10 «Reflow», asociado a un nivel AA.
* Se ha empleado C21: «Specifying line spacing in CSS», a través de la modificación de la propiedad `line-height` en la sección `main` del documento para los selectores `p`, `li` y `blockquote`, siempre con valores mayores o iguales a 1.5`em`. Esto ha permitido satisfacer el criterio 1.4.12 «Text Spacing», que corresponde a un nivel AA.
* A través del empleo de H25: «Providing a title using the title element», se ha especificado el título de cada página a través del empleo del elemento `title` en cada una de las páginas. Esto permite satisfacer el criterio 2.4.2 «Page titled», correspondiente a un nivel A.
* Mediante el empleo de H33, se ha asegurado que los enlaces proporcionan información descriptiva a través del atributo `title`. Esto permite satisfacer el criterio 2.4.4 «Link Purpose (In Context)», correspondiente a un nivel A.
* Se ha empleado H57 para determinar el idioma de la página a través del elemento `html`, específicamente el atributo `lang` con el valor `es`. Esto ha permitido satisfacer el criterio 3.1.1 «Language of page», correspondiente a un nivel A.
* Mediante H58, se ha especificado el idioma de los términos de origen extranjero a través del atributo `lang` en las etiquetas `i`; y a través del atributo `hreflang` en las etiquetas `a` para especificar el idioma del sitio externo. Esto permite satisfacer el criterio 3.1.2 «Language of Parts», que corresponde a un nivel AA.
* Mediante la técnica H40, se han empleado listas de descripción (elemento `dl`) para términos que se consideran argot que podrían resultar desconocidos al lector en la página de `terminología.html`. Esto permite responder al criterio 3.1.3 «Unusual Words», que corresponde a un nivel AAA.
* Mediante G61, los diferentes componentes y secciones (`header`, `main` y `footer`) de las páginas se presentan de forma que permanecen consistentes cuando se navega a través de los diferentes archivos. Al poseer reglas comunes en la hoja de estilos, esto permite que también se dé una consistencia visual. Esto permite satisfacer el criterio 3.2.3 «Consistent Navigation», nivel AA.

## Pregunta 2. Sobre las etiquetas.

Respecto a las etiquetas `abbr`, `cite`, `q`, `blockquote`, `figure`, `pre`, `address`, `iframe`, `i` y `time`:

### 2.1 ¿Qué marca cada una de ellas?

* `abbr` es una etiqueta HTML que se utiliza para marcar abreviaciones o acrónimos.
* `cite` permite marcar referencias a obras de creación.
* `q` se usa para citas dentro de una línea.
* `blockquote` se usa para citas paragrafadas que a menudo incluyen sangría propia.
* `figure` se emplea para contener contenido gráfico (imágenes, diagramas, etc.), permitiendo la adición de un pie o subtítulo a través de la etiqueta `figcaption`.
* `pre` se usa para marcar texto preformateado, que se mostrará tal y como se ha escrito.
* `address` denota información de contacto.
* `iframe` permite crear contextos de navegación anidados, lo cual permite la inserción de fragmentos de otra página HTML.
* `i` muestra texto diferenciado del texto normal. Originalmente este se colocaba en cursiva, y es por eso que ha conservado la letra «i» para su marcado (del inglés: _italics_).

### ¿Las habéis tenido que utilizar en las actividades prácticas de esta PEC? En caso afirmativo, poned un ejemplo del uso que habéis hecho de la correspondiente etiqueta.

Sí, muchas de ellas han sido empleadas en la realización de esta PEC. Como ejemplo, se ha utilizado la etiqueta `cite` para marcar las diferentes obras de creación que se han mencionado en el artículo. Un ejemplo específico de ese uso es cuando se ha usado para marcar _El Resplandor_ como obra de creación.

## Pregunta 3. Selectores CSS.

Escribid el selector que permita acceder a los elementos siguientes:

### 3.1 Elemento `a`, único hijo de un `li`.

```CSS

li a:only-child

```

### 3.2 Elemento `i`, descendiente de un `p`.

```CSS

p > i

```

### 3.3 Elemento `p` de clase `intro`.

```CSS

p.intro

```

### 3.4 Elemento `h2` hermano adyacente de un `figure`.

```CSS

h2 + figure

```

### 3.5 Elemento `li` primer hijo su `ol`.

```CSS

ol li:first-child

```

### 3.6 Elementos `li` que ocupan una posición impar dentro de su `ol`.

```CSS

ol li:nth-child(odd)

```

### 3.7 Elemento `a` que no tiene atribuida la clase `extern`.

```CSS

a:not(.extern)

```

### 3.8 Elemento `img` cuyo atributo `src` empiece con la cadena de texto `icon`.

```CSS

img[src^="icon-"]

```

### 3.9 Cualquier elemento descendiente del elemento `header`.

```CSS

header *

```

### 3.10 La primera letra de un elemento p.

```CSS

p::first-letter

```

# Explicación de las entidades HTML y CSS utilizadas
## Explicación de las entidades HTML
En la elaboración de los diferentes documentos `html` que conforman la PEC, se han utilizado las siguientes etiquetas:

* Se ha empleado la declaración `<!DOCTYPE html>` para englobar al los documentos `.html`, con el objetivo de asegurarnos de que el navegador pueda seguir las especificaciones pertinentes en su interpretación del código.
* Se ha especificado el idioma de las páginas mediante el uso de la etiqueta `<html>` y, concretamente, el atributo `lang` con el valor `es`. Esto permite que los navegadores identifiquen el idioma en el que está desarrollado el documento como español.
* Se ha utilizado `<head>` para incluir metadatos, en él se han contenido las etiquetas `<meta>`, `<link>` y `<title>`, utilizadas para especificar el set de caracteres como utf-8, habilitar la ruta de la hoja de estilo CSS y especificar el título de la página, respectivamente.
* Se ha utilizado la etiqueta `<body>` para contener la parte visual del documento. En él, se han dividido las diferentes secciones a través de los elementos `<header`, `<main>` y `<footer>`. Estos contienen la cabecera, el cuerpo y el pie del artículo, respectivamente.
    * Dentro del elemento `<header>` hallamos:
        * Un menú de navegación especificado mediante el elemento `<nav>`, a través del cual se puede acceder a las diferentes páginas que conforman el proyecto.
            * Este contiene una lista no ordenada `<ul>`, que contiene enlaces a los diferentes archivos `.html`. La página en la que se sitúa el usuario contiene el atributo `class="currentpage"` dentro de su elemento `<li>`, al que se le aplican reglas CSS específicas.
        * El otro componente de `<header>` es un elemento `<h1>` con el título principal de la página, «DigitalLAB», como valor.
            * La parte «LAB» está contenida en un elemento `<span>` con un atributo `class="LAB"` que servirá para modificar el formato de ese texto a través de la hoja de estilos.
    * Dentro del elemento `<main>` se hallan:
        * Un elemento `<h1>`, que representa el título principal de esta sección en cada página. También se hallan elementos `<h2>` para títulos inferiores en la jerarquía dentro del documento `index.html`. 
        * Dentro de `index.html`, dos elementos `<div>` para definir el subtítulo que aparece inferior al título principal y el autor del artículo, con los atributos `id="mainsubtitle"` y `id="author"` respectivamente.
        * Elementos `<figure>` en los que se contienen tanto las imágenes como los vídeos de YouTube incrustados en el artículo.
            * En el caso de las imágenes, el elemento `<figure>` contiene un elemento `<img>`, que permite representar la imagen, y un elemento `<figcaption>`, para el pie de imagen. Los elementos `<img>` contienen el atributo `alt`, que describe la imagen; y el atributo `src`, que indica la ruta de la imagen desde el directorio principal.
            * Para los vídeos incrustados de YouTube, se ha utilizado `<iframe>`.
        * Elementos `<p>`, usados para identificar los diferentes párrafos que conforman el texto.
        * Elementos `<blockquote>`, que contienen citas a obras de autor con un formato diferente al del resto del texto.
        * Algunas palabras del texto se han identificado mediante el elemento `<i>`, que designa extranjerismos o calcos de otro idioma, en ellos se ha especificado el idioma de origen mediante el atributo `lang`.
        * De forma similar, en ocasiones se ha usado `<cite>` para identificar obras de autor. Aunque se encuentra fuera de esta sección, también se ha usado en el pie de la página.
        * Asimismo, se ha empleado `<strong>` para destacar algunos conceptos dentro del artículo.
            * A algunos de estos, que contienen la palabra «FAKE», se les ha aplicado el atributo `class="FAKE"` para poder modificar su color a través de la hoja de estilos CSS.
        * De igual manera, se ha empleado `<em>` para expresar _énfasis_ dentro del texto.
        * Se han empleado el elemento `<ul>` en los archivos `guia.html` y `terminologia.html` para construir una lista con viñetas. Esta contiene elementos `<li>` que contienen los diferentes puntos que conforman la misma. En el caso de `guia.html` existen listas anidadas, con elementos `<ul>` que contienen elementos `<li>` que a su vez contienen elementos `<ul>` con sus respectivos elementos `<li>`.
        * Dentro del archivo `terminologia.html`, se ha empleado el elemento `<dl>` para designar una lista de descripción. Este contiene, a su vez, elementos `<dt>` (_description term_) que hacen referencia a los términos de la lista, mientras que los elementos `<dd>` (_description details_) contienen definiciones para los términos descritos previamente.
    * Dentro del elemento `<footer>` encontramos:
        * Dos elementos `<div>`. Uno, con el atributo `id="authorship"`, identifica el autor de la PEC; el otro, con el atributo `id="fineprint"`, ofrece información adicional en letra pequeña.
* Todos los enlaces dentro del artículo se hallan etiquetados a través de `<a>`, que incluye los atributos `href`, para denotar la ruta; `title`, para describir el contenido del enlace; y `hreflang` para especificar el idioma del contenido del enlace.

## Explicación de las entidades CSS

Para la hoja de estilos CSS, se han empleado los selectores siguientes:

El selector `body`, que se ha empleado para especificar la propiedad `margin` global de 0 (este será más tarde modificado por selectores para cada sección) y `font-family`.

### Entidades del `header`

El selector `header` contiene tres propiedades: `margin`, `width` y `text-align`. Estas se han utilizado para centrar los elementos, especificar el ancho de la sección y centrar el texto, respectivamente.

* El selector `header h1` se ha usado para darle formato al título principal «digitalLAB». Contiene las siguientes propiedades:
    * `font-family`, que se ha empleado para cambiar de la familia de fuente global a un más específica con serifa.
    * `letter-spacing`, que se ha reducido para conseguir un estilo similar al de la captura-modelo proporcionada.
    * `font-size`, igualmente, su valor se ha aumentado para conseguir un aspecto visual más parecido al del modelo.
    * `margin-top` se ha usado para aumentar ligeramente el margen superior, mientras que el `margin-bottom` se ha reducido.
* El selector `header .LAB` se ha empleado para darle formato al texto «LAB» del título principal. Este solo incluye la declaración `color: #ea6628;`. Se ha decidido usar una clase y no una `id` para mayor comodidad por si se repite ese formato en algún momento futuro.
* Para el menú de navegación, se han empleado los siguientes selectores:
    * `nav a` se ha usado para modificar el formato de los enlaces de navegación. Se ha hecho uso de las propiedades `color` y `text-decoration` para ese fin, a las que se han aplicado los valores `unset` y `none` respectivamente. 
        * Se ha usado el selector `nav a:hover` para cumplir el requisito de modificación del formato de la PEC al colocar el ratón encima del enlace: a través de la declaración `color: #666` este cambia a gris.
    * `nav ul` se ha utilizado para modificar el aspecto de la lista que conforma el menú de navegación. Se han usado la declaración `list-style-type: none`, para eliminar la viñeta; `padding-left: 0` para eliminar el espacio correspondiente a la viñeta; y `font-weight: bold` para modificarla a negrita.
    * `nav ul li` se ha usado para modificar aspectos particulares de los elementos de esa lista. Se ha empleado la declaración `white-space: nowrap` para evitar que se dé un salto de línea al reducir el tamaño de la ventana; así como las propiedades `padding-top` y `padding-bottom` con el valor `0.25em` para añadir un poco de separación entre las opciones.
        * Mediante el selector `nav .currentpage` se ha aumentado el tamaño del elemento de la lista que corresponde a la página actual, a través de la declaración `font-size: 1.4em`.

### Entidades de `main`

Dentro del elemento `main` se ha especificado un margen global a través de la declaración `margin: 3em auto 3em auto`, y se ha habilitado una anchura máxima del 60% del total a través de `max-width: 60%;`.

* El selector `main p` se ha empleado para aumentar el interlineado, a través de la declaración `line-height: 1.65em`.
* `main figure` se ha usado para darle formato a los contenedores de las imágenes y vídeos incrustados. Aquí se han usado las propiedades `margin-top` y `margin-bottom`, con un valor de `2em` en cada una, para aumentar ligeramente la distancia entre este tipo de elementos y el resto del texto, tal y como se muestra en la imagen modelo.
    * `main figure > *` contenía las declaraciones `margin: 0 auto`, `display: block` y `max-width: 100%`. Estas tienen como objetivo cualquier elemento contenido en
    `figure` y asegurarse de que ocupa el espacio completo de esta sección.
* `main figcaption` se emplea para configurar el texto del pie de imagen de las imágenes y vídeos incrustados. Aquí se han empleado las propiedades `text-align`, `margin`, `font-size`, `letter-spacing`, `font-weight` y `padding-bottom` para asemejarlo a la captura-modelo de la PEC.
* `main blockquote` modifica el formato de las citas en bloque. Aquí se ha cambiado la fuente a una con serifa mediante la declaración `font-family: Georgia, 'Times New Roman', Times, serif`, se ha aumentado el tamaño de la fuente a mediante `font-size: 1.2em`, así como el espaciado a través de `letter-spacing: 0.025em`, y se ha reducido ligeramente el interlineado (respecto al general) a través de `line-height: 1.5em` para compensar el aumento del tamaño de la fuente.
* Para los selectores `main h1` y `main h2` se han usado las propiedades `font-weight` y `font-size` para adaptarlos al tamaño de la imagen modelo. En el caso de `main h1`, se ha centrado a través de la declaración `text-align: center`. Para `main h2`, también se han modificado los márgenes superior e inferior.
* Se ha empleado `main a` para modificar los enlaces de esta sección según las especificaciones de la PEC. Usando las declaraciones `text-decoration: none` y `color: #0066cc`, se ha eliminado el subrayado por defecto y se ha modificado el color.
    * Se ha usado `main a:hover` para añadir subrayado a los enlaces al pasar el ratón por encima tal y como se especifica en el enunciado de la PEC.
* A través del selector `main .FAKE` se ha aplicado color rojo a todas las instancias de la palabra «FAKE» que aparecen en color rojo.
* Mediante `main li`, se ha aumentado ligeramente el interlineado a través de la propiedad `line-height`.
* Los selectores de id `#mainsubtitle` y `#author` se usan para modificar el texto inmediatamente inferior al título principal de esta sección, y contienen las propiedades `text-align`, `margin-top` y `margin-bottom`.

Dentro de los selectores específicos para elementos del archivo `guia.html`, se han usado:

* `main ul.book>li` es un selector que se ha empleado para dar formato a las viñetas de esta sección mediante la declaración `list-style: url("../img/book.png")`. También se alteró el tamaño usando la propiedad `font-size`. Asimismo, se ha usado el selector `main ul.book>li>ul` con el objetivo de modificar el estilo de las sub-viñetas de esa lista: a través de la declaración `list-style: circle`; tambíen, con el objetivo de mantener el tamaño inicial, se declaró `font-size: initial`. Igualmente, el `padding` fue modificado ligeramente para aumentar el espacio entre los elementos.

Dentro de los específicos del archivo `terminologia.html`, encontramos:

* `main dt`, aplicable a los términos de la lista de descripción, a los que se les modificó el color, el tamaño de la fuente, el formato de la fuente y la familia de fuente mediante las propiedades `color`, `font-size`, `font-weight` y `font-family`, respectivamente.
* `main dd`, al cual se le han modificado las propiedades `margin-left`, `padding-top` y `padding-bottom` para ajustarlo al tamaño del modelo.

### Entidades de `footer`

Para el selector `footer`, se han usado las declaraciones `margin: 0 auto` y `background-color: #91d3c5` para ajustarlo al estilo solicitado en el enunciado. Después, más especificamente, se han usado los selectores:

* `footer a`. Para alterar el formato por defecto de los enlaces de esta sección se han empleado las declaraciones `text-decoration: none` y `color: 167763`.
    * `footer a:hover` modifica el formato al pasar el ratón por encima del enlace de esta sección mediante la declaración `text-decoration: underline`.
* Las declaraciones `#authorship` y `#fineprint` se emplean para configurar el formato del texto de esta sección. Se hace a través de las propiedades `padding`, `text-align`, `font-size`, `text-align` y `padding`.