# Formularios

Los formularios permiten la realización de aplicaciones interactivas, proporcionando un mecanismo para **recopilación de
información propia del usuario**.

La creación de formularios consta de dos partes:

* La creación de la estructura donde se solicita/incluye la información solicitada (etiquetas `input`, `textarea`,
`select` y otras).
* La realización de una acción con la información solicitada (etiqueta `form`).

## Formularios

La etiqueta **`form` permite definir la acción (y como) que se realizará para enviar el formulario al servidor**. Para
ello, se hacen uso de los siguientes atributos:

* **`action`**: la URL que procesará la información enviada (la URL "destinataria" del formulario).
* **`method`**: el método por el cual se enviará (`GET` o `POST`).

```html
<form name="Pedido" action="/programa_servidor.jsp" method="GET">
...
</form>
```

### Labels

Dentro del formulario, se pueden asociar "etiquetas de nombre" a los campos a cubrir. Esto se realiza con la etiqueta
`label`. En la etiqueta `label` se especifica el atributo `for` con el ID del campo a asociar.

```html
<!-- OPCIÓN 1 (Recomendada): Es necesario incluir el atributo "for" -->
<label for="txt">Texto:</label>
<input type="text" size="20" name="txt_1" id="txt"/>

<!-- Opción 2: Se puede llegar a omitir -->
<label>
    Texto:
    <input type="text" size="20" name="txt_1"/>
</label>
```

### Fieldset y Legend

Para agrupar la información y hacerlo más visual, se pueden utilizar dos atributos adicionales: `fieldset` y `legend`.
De esta forma, campos similares se pueden agrupar e indicar una leyenda para los mismos.

```html
<fieldset>
<legend>Campo 1:</legend>
    ...
</fieldset>
```

### Ejemplo

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <form action="#" method="get">
        <fieldset>
            <legend>Campo 1</legend>
            <label for="field1">Nombre 1</label>
            <input type="text" name="name1" id="field1"/>
            <label for="field2">Nombre 2</label>
            <input type="text" name="name2" id="field2"/>
        </fieldset>
        <fieldset>
            <legend>Campo 2</legend>
            <label for="field3">Opción 1</label>
            <input type="checkbox" name="check" id="field3"/>
            <label for="field4">Opción 2</label>
            <input type="checkbox" name="check" id="field4" checked/>
        </fieldset>
        <input type="submit" value="Enviar">
    </form>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/form.html"></iframe>

## Etiqueta `input`

Permite crear diferentes elementos gráficos para la captura de información. Su estructura, con los atributos más
comunes, es la siguiente:

```html
<input type="..." name="..." value="..."/>
```

* `type`: tipo de control (botón, texto, contraseña, enviar, resetear, oculto, archivo, etc.)
* `name`: nombre del campo a capturar (se enviará después al servidor)
* `value`: valor actual del campo

Al igual que cualquier otro elemento HTML, los `input` tiene asignados una serie de métodos para poder responder a
ciertos eventos dados. Dependiendo del `type`, es posible que haya alguno más disponible.

### Botón

Permite realizar una acción al hacer click sobre el botón.

=== "Ejemplo"
   
    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="button" name="btn_1" value="Pulsar"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_button.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)

### Texto

Permite la introducción de datos en forma de texto en una sola línea.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="text" size="20" name="txt_1" value="Este es el texto por defecto"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_text.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado
    * `onSelect`: se ha seleccionado un valor en el elemento

### Contraseña

Permite la introducción de datos en forma de texto oculto al usuario.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="password" size="20" name="pwd_1" value="Texto por defecto"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_password.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado
    * `onSelect`: se ha seleccionado un valor en el elemento

### Oculto

Permite la introducción de datos útiles para el servidor de manera programática, ocultos al usuario.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="hidden" name="oculto_1" value="Información enviada"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_hidden.html"></iframe>

!!! info "Métodos Disponibles"

    * `onChange`: el valor del elemento ha cambiado

### Enviar

Permite el envío de los datos del formulario al servidor.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="submit" name="sub_1" value="Pulsar para enviar"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_submit.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)

### Resetear

Permite el restablecimiento de los datos del formulario al servidor.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="reset" name="rst_1" value="Pulsa para reestablecer">
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_reset.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)

### Archivo

Permite seleccionar archivos locales para "subirlos" al servidor.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="file" name="arch_1" size="30/">
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_file.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

### Checkboxes

Permite seleccionar varias opciones de una lista predefinida.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="checkbox" name="chk_1"/>Opción 1
    <input type="checkbox" name="chk_1" checked/>Opción 2
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_checkbox.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

### Radios

Permite seleccionar una opción de una lista predefinida.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="radio" name="radio_1"/>Opción 1
    <input type="radio" name="radio_1" checked/>Opción 2
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_radio.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

### Imagen

Permite crear botones de envío gráficos, es decir, que adoptan la forma de una imagen en lugar de texto.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="image" src="imagen.gif" name="coord"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_image.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

### Range

Permite crear un elemento gráfico de tipo "slide" para poder seleccionar un rango de valores.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="range" min="18" max="70" value="35" id="age"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_range.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

### Fechas y Horas

Permite seleccionar una fecha, ya sea un día (`date`), semana (`week`) o mes (`month`). También se pueden seleccionar
horas (`time`) o ambas a la vez (`datetime-local`).

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="date" name="day"/>
    <input type="week" name="week"/>
    <input type="month" name="month"/>
    <input type="time" name="time"/>
    <input type="datetime-local" name="datetime"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_date.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

### Color

Permite seleccionar un color de la paleta de colores.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="color" name="color"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/input_color.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado

## Etiqueta `textarea`

Esta etiqueta permite enviar texto multilínea al servidor. Es similar al `<input type="text">`, pero con la diferencia
de permitir introducir retornos de carro.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <textarea name="texto_1" rows="5" cols="30">
    Introduzca
    el texto
    deseado
    </textarea>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/textarea.html"></iframe>

!!! info "Métodos Disponibles"

    * `onClick`: se ha realizado click en el elemento
    * `onFocus`: se ha realizado focus en el elemento (_click pero sin llegar a levantar_)
    * `onBlur`: se ha dejado de hacer focus en el elemeneto (_se ha levantado el click_)
    * `onChange`: el valor del elemento ha cambiado
    * `onSelect`: se ha seleccionado un valor en el elemento
    * `onKeyPress`: se ha pulsado una tecla del teclado
    * `onKeyDown`: se ha pulsado una tecla del teclado pero no se ha levantado la pulsación todavía
    * `onKeyUp`: se ha levantado la pulsación de la tecla del teclado

## Etiqueta `datalist`

Esta etiquieta permite crear listas de valores por defecto que ayudan a encontrar posibles nombres por defecto.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <input type="text" list="nombres" name="txt_1"/>
    <datalist id="nombres">
        <option value="Pedro"></option>
        <option value="Antonio"></option>
        <option value="Manuel"></option>
        <option value="Pablo"></option>
    </datalist>
    <input type="submit"/>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/datalist.html"></iframe>

## Etiqueta `select`

Esta etiqueta permite crear un desplegable y seleccionar una (o varias) opciones de una lista.

=== "Ejemplo"

    ```html
    <html>
    <head>
        <title>Mi primera página web</title>
    </head>
    
    <body>
    <select name="lista_1" size="1">
        <option value="valor_1" selected>Opción 1</option>
        <option value="valor_2">Opción 2</option>
        <option value="valor_3">Opción 3</option>
    </select>
    </body>
    </html>
    ```

=== "Previsualización"

    <iframe width="700" height="300" frameBorder="0" src="/html/ejemplos/select.html"></iframe>
