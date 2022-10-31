---
documentclass: scrartcl
title: "HTML y CSS: PEC 1"
author: Ignacio Casares Ruiz
header-includes:
 - \usepackage{fvextra}
 - \DefineVerbatimEnvironment{Highlighting}{Verbatim}{breaklines,commandchars=\\\{\}}
---

## Pregunta 1. Sobre accesibilidad web.

### 1.1 _¿Qué entendemos por accesibilidad web?_

La accesibilidad hace referencia a la propiedad de las páginas web de ser utilizada (o accessible) por la mayor cantidad de usuarios posible. Esto implica la implementación de aspectos que permitan que ciertas personas con una capacidad de interacción menor puedan interaccionar con los aspectos de la web en las condiciones similares a las del resto de usuarios, con el objetivo de proporcionar igualdad de acceso a ese servicio.

### 1.2 _¿Qué son las WCAG?_

WCAG es un acrónimo de _Web Content Accessibility Guidelines_. Son una serie de directrices propugnadas por el Consorcio WWW (W3C) que describen cómo construir contenido web de forma que este sea más accesible para personas discapacitadas.

### 1.3 _¿Qué técnicas de accesibilidad has podido aplicar en los archivos de la parte práctica de esta PEC?_

## Pregunta 2. Sobre las etiquetas.

Respecto a las etiquetas `abbr`, `cite`, `q`, `blockquote`, `figure`, `pre`, `address`, `iframe`, `i` y `time`:

### 2.1 ¿Qué marca cada una de ellas?

* `abbr` es una etiqueta HTML que se utiliza para marcar abreviaciones o acrónimos.
* `cite` permite marcar referencias a obras de creación.
* `q` se usa para citas dentro de una línea.
* `blockquote` se usa para citas paragrafadas que a menudo incluyen sangría propia.
* `figure` se emplea para contener contenido gráfico (imágenes, diagrafmas,etc.), permitiendo la adición de un pie o subtítulo a través de la etiqueta `figcaption`.
* `pre` se usa para marcar texto preformateado, que se mostrará tal y como se ha escrito.
* `address` denota información de contacto.
* `iframe` permite crear contextos de navegación anidados, lo cual permite la inserción de fragmentos de otra página HTML.
* `i` muestra texto diferenciado del texto normal. Originalmente este se colocaba en cursiva, y es por eso que ha conservado la letra «i» para su marcado (del inglés: _italics_).

### ¿Las habéis tenido que utilizar en las actividades prácticas de esta PEC? En caso afirmativo, poned un ejemplo del uso que habéis hecho de la correspondiente etiqueta.

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