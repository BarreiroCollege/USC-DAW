# Uso de CSS

## Atributo `#!css style`

!!! warning "NO hay selector"

    Al usar el atributo `#!css style`, el selector va implícito (afecta al propio elemento). Por lo tanto, lo que se ha
    de escribir es la propia declaración.  
    Y por este mismo motivo, **no es una buena práctica usar el atributo `#!css style`**, ya que hace más difícil el
    averiguar desde donde vienen los cambios en la cascada de estilos.

Esta es la forma más básica de usar estilos. **Se indica en los propios elementos los cambios a realizar.**

=== "HTML"

    ```html
    <html>
    <head>
        <title>Desarrollo de Aplicaciones Web</title>
    </head>
    
    <body>
    <h1>Bienvenidos a la página web de DAW</h1>
    <div style="color: red;">
        <p>Esta es la página web de la asignatura.</p>
        <p style="color: black;">
            Los cambios se propagan a los hijos, por lo que habría que
            forzar un reset.
        </p>
        <p>Aquí encontrarás todo el material...</p>
    </div>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/css/ejemplos/style.html"></iframe>

## Hoja Interna

Un poco más _profesional_, con este método se puede **separar el estilo del HTML** en el propio archivo. Como se puede
ver, por lo general tendrá más prioridad el atributo `#!css style`. 

=== "HTML"

    ```html
    <html>
    <head>
        <title>Desarrollo de Aplicaciones Web</title>
        <style>
            h1 {
                font-family: sans-serif;
            }
    
            p {
                color: red;
            }
        </style>
    </head>
    
    <body>
    <h1>Bienvenidos a la página web de DAW</h1>
    <p>Esta es la página web de la asignatura.</p>
    <p style="color: black;">Aquí encontrarás todo el material...</p>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/css/ejemplos/hinterna.html"></iframe>

## Hoja Externa

Esta es la forma **más común** de usar CSS. Se utiliza un **archivo totalmente distinto al HTML** para especificar los
estilos. El contenido es el mismo que el de la hoja interna, pero al ser ya un archivo con **extensión `.css`**, no es
necesario indicar que se trata de estilos.

=== "index.html"

    ```html hl_lines="4"
    <html>
    <head>
        <title>Desarrollo de Aplicaciones Web</title>
        <link rel="stylesheet" href="hoja.css"/>
    </head>
    
    <body>
    <h1>Bienvenidos a la página web de DAW</h1>
    <p>Esta es la página web de la asignatura.</p>
    <p style="color: black;">Aquí encontrarás todo el material...</p>
    </body>
    </html>
    ```

=== "hoja.css"

    ```css
    h1 {
        font-family: sans-serif;
    }

    p {
        color: red;
    }
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/css/ejemplos/hexterna.html"></iframe>

!!! info "Importar CSS desde CSS"

    Es posible importar CSS desde otra hoja CSS (incluirlos hojas entre ellas). Hay dos formas de hacerlo en un
    archivo **`.css`**:

    === "hoja.css"

        ```css
        @import "hoja2.css";
        @import url("hoja3.css");
        ```
