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

    <iframe width=700, height=500 frameBorder=0 src="ejemplos/tipografia.html"></iframe>

### Etiquetas de Formateo de Texto

### Etiqueta de Hiperenlace

### Etiquetas de Listas

### Etiqueta de Imágen

### Etiquetas de Tablas

## HTML 5

### Nuevas Etiquetas

### Otros Cambios
