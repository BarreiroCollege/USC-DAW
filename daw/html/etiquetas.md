# Etiquetas

La estructura básica de las etiquetas es la siguiente:

```html
<tag attr="..."> ... </tag>
<tag attr="..."/>
```

Ambos tipos de etiquetas son equivalentes: **la primera tiene contenido** y **la segunda no**. Dependiendo de la
etiquieta, la correcta puede ser una u otra, o ambas. Las etiquetas **pueden tener atributos** con contenido de texto.

También es posible hacer comentarios con las siguientes indicaciones:

```html
<!-- Esto es un comentario -->
```

## Tipos de Etiqueta

En HTML existen dos tipos de etiqueta:

- **Etiquetas de bloque**: aquellas cuyo uso supone (por defecto) una ruptura de línea, antes y después de su uso
  (`h1`, `p`, ...). Tienen las propiedades de ancho y alto.
- **Etiquetas de línea**: aquellas cuyo uso no supone (por defecto) una ruptura con el texto en el que se hayan
  insertado (`a`, `img`, ...). No tienen las propiedades de ancho y alto.

Un **elemento de bloque puede contener tanto elementos de bloque como de línea**, pero un **elemento de líena no debe
contener ningún elemento de bloque**. Sin embargo, esta distinción _no se aplica para HTML 5_, ya que hay otras
categorías.

### Etiquetas de Tipografía

- **Heading** (cabecera): `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`
- **Párrafo**: `<p>`
- **Enlace**: `<a>`
- **Cita**: `<blockquote>`

=== "Ejemplo"
   
    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <h1>Este es el encabezamiento</h1>
    <p>Aquí incluyo el texto que acompaña el encabezamiento</p>
    <h2>Aquí encabezo una sección</h2>
    <p>Este es el texto de la sección, donde referencio a la página <a href="laotra.html">la otra página</a></p>
    <blockquote>
        Además podemos marcar de forma especial algunas partes del texto, utilizando etiquetas de tipo "blockquote"
    </blockquote>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/tipografia.html"></iframe>

### Etiquetas de Formateo de Texto

- **Negrita**: `<strong>`, `<b>`
- **Cursiva**: `<em>`, `<i>`
- **Comillas**: `<q>`
- **Salto de línea**: `<br>`
- **Bloque de código**: `<pre>`

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi segunda página web</title>
    </head>
    
    <body>
    <h1>Este es el encabezamiento</h1>
    <p>
        Aquí incluyo el texto que acompaña al encabezamiento. Puedo incluir
        <strong>negrita</strong>, <em>cursiva</em> y <q>comillas</q> (esto último
        si no se usa Internet Explorer.
        También existe el salto <br/> de línea.
        <pre>
        Finalmente,
        tengo la opción de escribir
        de forma literal
        </pre>
    </p>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/formateo.html"></iframe>

### Etiqueta de Hiperenlace

- **Enlace** o **Ancla**: `<a>`

=== "Ejemplo"

    ```html hl_lines="9 12"
    <html>
    <head>
        <title>Mi segunda página web</title>
    </head>
    
    <body>
    <h1>Este es el encabezamiento</h1>
    <p>Aquí enlazo con una página <a href="http://www.usc.es">externa</a>.</p>
    <p>Aquí enlazo con una posición diferente dentro de esta <a href="#otroParrafo">misma página</a>.</p> <!-- (1) -->
    <p>Aquí escribo un nuevo párrafo</p>
    <p>
        Aquí marco una posición dentro del párrafo, para ser <a id="otroParrafo">referenciada</a>
        desde otra posición de la página.
    </p>
    <h3 id="esteOtroParrafo">Normalmente se referencian las cabeceras</h3>
    </body>
    </html>
    ```
    
    1. Se puede referenciar identificadores dentro de páginas externas, por ejemplo,
       `#!html href="otraPagina.html#otraCosa"`.

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/enlace.html"></iframe>

### Etiquetas de Listas

### Etiqueta de Imágen

### Etiquetas de Tablas

## HTML 5

### Nuevas Etiquetas

### Otros Cambios
