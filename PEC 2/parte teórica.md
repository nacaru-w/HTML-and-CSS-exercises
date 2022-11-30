---
title: "PEC 2"
subtitle: "HTML y CSS: Universitat Oberta de Catalunya"
date: "Diciembre de 2022"
author: "Ignacio Casares Ruiz"
documentclass: scrreprt
colorlinks: true
header-includes:
 - \usepackage{fvextra}
 - \DefineVerbatimEnvironment{Highlighting}{Verbatim}{breaklines,commandchars=\\\{\}}
 - \renewcommand{\figurename}{Imagen}
---

## Pregunta 1

Sobre la utilización de tablas, responde a las siguientes preguntas:

### 1. Explica el uso de los elementos `thead`, `tbody` y `tfoot` dentro de una tabla.

* `thead` se utiliza para delimitar las filas que corresponden a la cabecera de la tabla.
* `tbody` por su parte, se usa para delimitar las filas que corresponden al cuerpo de la tabla.
* `tfood` se emplea para englobar aquellas filas que comprenden el pie de la tabla.

La presencia de estas etiquetas permite una interpretación más eficaz por parte de los lectores de pantalla, por lo que son importantes a la hora de mejorar la accesibilidad de la página.

### 2. Las WCAG 2.1 indican que es importante el uso de la etiqueta `caption` y del atributo `scope`; explica de qué manera su uso mejora la accesibilidad de las tablas.

`caption` es una etiqueta que contiene una descripción de los elementos de que conforman la tabla. Esto permite que los lectores y los usuarios que utilicen lectores de pantalla puedan conocer de forma resumida los contenidos de la tabla de forma rápida para después decidir si examinarla con mayor deteminimiento o no.

`scope` es un atributo que permite definir qué celdas están comprendidas en el elemento `header`. Este puede completarse con los valores `col` o `row`, permitiendo delimitar de forma más eficaz qué filas o columnas son parte del encabezado de la tabla. 


## Pregunta 2

Sobre la utilización de formularios, responde a las siguientes preguntas:

### 1. Explica para qué se utilizan los siguientes atributos propios de los formularios:

* `action` y `method`: ambos son atributos del elemento `form`, el primero permite establecer una ruta en la cual se procesará la información proveída por el usuario a través del formulario. En el caso del atributo `method`, permite especificar la forma en la que se enviarán los datos recogidos por el formulario a la URL establecida a través de `action`; puede contener los valores `post`, `get` y `dialog`. 
* `required`: se trata de un atributo que se aplica a los diferentes campos que conforman el formulario, obliga al usuario a completarlo para poder procesarlo.
* `minlength` y `maxlength`: son controles de valores que permiten delimitar el número de caractéres presentes en el campo. Se usan como atributos del elemento `input`.
* `pattern`: este control de valor permite limitar la entrada de datos a una serie de características definidas a través de expresiones regulares. Al igual que en el caso anterior, se usan como atributos del elemento `input`.

### 2. Explica para qué sirve y cómo debe usarse la etiqueta `label` dentro de un formulario. ¿Qué importancia tiene esta etiqueta en relación con la accesibilidad de los formularios?

`label` permite configurar etiquetas con texto descriptivo asociadas a las diferentes entidades del formulario. La asociación se hace mediante dos formas:

* Usando el atributo `for`, cuyo valor debe de ser igual al del atributo `id` del elemento `input` al que se quiere relacionar:

```html
<label for="ejemplo">Esto es un ejemplo de etiqueta</label>
<input type="textbox" name="nombre_de_ejemplo" id="ejemplo">
```
* Incluyendo el elemento `input` dentro del elemento `label`:

```html
<label>
    Esto es un ejemplo de etiqueta
    <input type="textbox" name="nombre_de_ejemplo" id="ejemplo">
</label>
```

La etiqueta `label` permite una mayor accesibilidad al poder ser identificada por lectores de pantalla y otros tipos de tecnología asistida, y permite a los usuarios acceder al campo a través de la selección de la etiqueta.

## Pregunta 3

Sobre CSS, responde a las siguientes preguntas:

### 1. ¿Qué entendemos por modelo de cajas en CSS? ¿Qué diferencia hay entre el modelo de cajas estándar y el modelo de cajas alternativo? ¿Con qué propiedad podemos activar el modelo de cajas alternativo?

### 2. Investiga sobre las funciones `calc()`, `var()`, y `clamp()` de CSS. ¿Para qué las podemos usar? Aporta un ejemplo de cóidgo de cada una de ellas dentro de una hoja de estilos.