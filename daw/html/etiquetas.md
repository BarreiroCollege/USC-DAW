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

    ```html hl_lines="11 15"
    <html>
    <head>
        <title>Mi segunda página web</title>
    </head>
    
    <body>
    <h1>Este es el encabezamiento</h1>
    <p>Aquí enlazo con una página <a href="http://www.usc.es">externa</a>.</p>
    <p>
        Aquí enlazo con una posición diferente dentro de esta
        <a href="#otroParrafo">misma página</a>.
    </p>
    <p>Aquí escribo un nuevo párrafo</p>
    <p>
        Aquí marco una posición dentro del párrafo, para ser
        <a id="otroParrafo">referenciada</a> desde otra posición de
        la página.
    </p>
    <h3 id="esteOtroParrafo">Normalmente se referencian las cabeceras</h3>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/enlace.html"></iframe>

### Etiquetas de Listas

- **Listas Ordenadas (`ol`)**: son listas en las cuales el orden lo fijan los números o letras que las acompañan.
- **Listas No Ordenadas (`ul`)**: son listas en las cuales no se fija un orden, simplemente se incluyen los elementos
  de la lista acompañándolos de un símbolo al inicio.
- **Listas de Definición (`dl`)**: son listas en las cuales tampoco se fija un orden, sólamente se incluyen definiciones
  de los diferentes elementos de la lista, sin acompañamiento de ningún símbolo al comienzo de cada ítem.

#### ol, li

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi tercera página web</title>
    </head>
    
    <body>
    <h1>Este es el encabezamiento</h1>
    <p>Ahora vamos a incluir listas.</p>
    <h2>Listas ordenadas</h2>
    <ol>
        <li>Primer elemento</li>
        <li>Segundo elemento</li>
        <li>Etc.</li>
    </ol>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/ol.html"></iframe>

#### ul, li

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi tercera página web</title>
    </head>
    
    <body>
    <h2>Listas no ordenadas</h2>
    <ul>
        <li>Primer elemento</li>
        <li>Segundo elemento</li>
        <li>Etc.</li>
    </ul>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/ul.html"></iframe>

#### dl, dt, dd

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi tercera página web</title>
    </head>
    
    <body>
    <h2>Listas de definición</h2>
    <dl>
        <dt>Primera definición</dt>
        <dd>Texto de la definición</dd>
        <dt>Segunda definición</dt>
        <dd>Texto de la definición</dd>
    </dl>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/dl.html"></iframe>

### Etiqueta de Imágen

- **Imagen**: `<img>`

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi cuarta página web</title>
    </head>
    
    <body>
    <h1>Este es el encabezamiento</h1>
    <p>
        Ahora vamos a insertar imágenes.<br/>
        Se permiten usar los tipos más comunes.
    </p>
    <p>PNG <img src="https://github.com/barreeeiroo.png?s=128"/></p>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/imagen.html"></iframe>

### Etiquetas de Tablas

- **Tabla**: `<table>`
- **Título**: `<caption>`
- **Cabecera** (_Header_): `<thead>`, `<th>`
- **Fila** (_Row_): `<tr>`
- **Datos** (_Data_): `<tbody>`, `<td>`
- **Pie** (_Footer_): `<tfoot>`

!!! faq "Etiquetas semánticas"

    El uso de `<thead>`, `<tbody>` y `<tfoot>` es totalmente opcional: son etiquetas semánticas que ayudan a
    identificar el contenido de la tabla, pero que a nivel de renderizado no se tienen en cuenta.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi quinta página web</title>
    </head>
    
    <body>
    <table>
        <caption>Tabla I</caption>
        <thead>
        <tr>
            <th>Nombre</th>
            <th>Apellidos</th>
        </tr>
        </thead>
        
        <tbody>
        <tr>
            <td>Antonio</td>
            <td>Pérez García</td>
        </tr>
        <tr>
            <td>Carlos</td>
            <td>Rodríguez López</td>
        </tr>
        </tbody>
        
        <tfoot>
        <tr>
            <td>Pepito</td>
            <td>Grillo</td>
        </tr>
        </tfoot>
    </table>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/tabla.html"></iframe>

## HTML 5

### Nuevas Etiquetas

### Otros Cambios
