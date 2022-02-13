# HTML 5

HTML 5 es el último estándar publicado. Incorpora cambios significativos, **agilizando la creación de webs** gracias a
diversas nuevas funciones.

!!! check "DOCTYPE"

    Se introduce un nuevo `DOCTYPE`, reduciendo el número de caracteres y unificando todas las opciones.

    ```html
    <!DOCTYPE html>
    ```

!!! check "Conjunto de caracteres"

    Se introduce un _charset_, o conjunto de caracteres, directamente en las propias etiquetas `meta`.

    ```html
    <meta charset="utf-8">
    ```

!!! check "Declaración de atributos"

    Se permite el uso de mayúsculas y minúsculas en los atributos, y la opción de no usar las comillas.

    ```html
    <div id="daw"/>
    <div id=daw/>
    <div ID="daw"/>
    <div ID=daw/>
    ```

## Nuevas Etiquetas

Además, se crean **nuevas etiquietas con denominación semántica**. A efectos prácticos, se tratarán como `#!html <div>`,
pero ayudarán a estructurar mejor el contenido de las páginas.

![Elementos Semánticos](https://www.w3schools.com/html/img_sem_elements.gif){ align=right }

- `#!html <article>`
- `#!html <aside>`
- `#!html <details>`
- `#!html <figcaption>`
- `#!html <figure>`
- `#!html <footer>`
- `#!html <header>`
- `#!html <main>`
- `#!html <nav>`
- `#!html <section>`
- `#!html <summary>`

Se crean también otras etiquietas para **usar diferentes tipos de recursos**:

- `#!html <audio>`
- `#!html <canvas>`
- `#!html <iframe>`
- `#!html <track>`
- `#!html <video>`

Y otras etiquietas con distintos usos:

- `#!html <mark>`
- `#!html <meter>`
- `#!html <progress>`
- `#!html <time>`

## Otros Cambios

- [Nuevos **atributos**](https://www.w3.org/TR/html5-diff/#new-attributes)
- Acceso mejorado a **elementos DOM** mediante JavaScript
- [Nuevas **API's**](https://www.w3.org/TR/html5-diff/#new-apis) nativas (_se van añadiendo nuevas continuamente_)


*[DOM]: Document Object Model
