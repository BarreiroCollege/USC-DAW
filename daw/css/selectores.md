# Selectores

En una hoja de estilos, es necesario especificar a que elementos les afectan las reglas. Estas especificaciones se
llaman **selectores**, los cuales permiten usarse de diferente forma en función de lo que se quiere modificar:

| **Selector**     | **Ejemplo**                                            |
|------------------|--------------------------------------------------------|
| Universal        | `#!css * { }`                                          |
| Tipo de etiqueta | `#!css h1 { }`                                         |
| Clase            | `#!css .nombre { }` --> `#!html <tag class="nombre"/>` |
| Identificador    | `#!css #nombre { }` --> `#!html <tag id="nombre"/>`    |
| Atributo         | `#!css [attr=valor]` --> `#!html <tag attr="valor"/>`  |

Además, hay una serie de **combinadores** que permiten hacer un CSS más condicional y personalizado:

| **Combinador**           | **Ejemplo**                                                                         |
|--------------------------|-------------------------------------------------------------------------------------|
| Descendiente de selector | `#!css li a { }` --> `#!html <li><a/></li>`                                         |
| Hijo de selector         | `#!css li > a { }` (_a diferencia del anterior, los "nietos" no se ven afectados_)  |
| Hermano adyacente        | `#!css h1 + p { }` --> `#!html <h1/><p/><p/>` (solo afecta el primer `#!html <p/>`) |
| Hermano general          | `#!css h1 ~ p { }` --> `#!html <h1/><p/><p/>` (afecta a ambos `#!html <p/>`)        |

Finalmente, existen también una serie de selectores por **pseudo-clases**. Estos permiten afectar a cualquiera de los
selectores anteriormente descritos cuando se cumple alguna condición. La lista completa de pseudo-clases se encuentra en
[este enlace](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes#indice_de_las_pseudo-clases_est%C3%A1ndar), y
algunas de las más comunes son:

| **Pseudo-clase**           | **Acción**                            |
|----------------------------|---------------------------------------|
| `#!css a:link { }`         | Enlace "no visitado"                  |
| `#!css a:visited { }`      | Enlace "ya visitado"                  |
| `#!css button:active { }`  | Botón siendo activado por el usuario  |
| `#!css li:first-child { }` | Primer elemento de una lista          |
| `#!css p:hover { }`        | El ratón está sobre el texto          |
| `#!css input:focus { }`    | Se está esperando la entrada de texto |

## Especificidad

La **especificidad** se define como la manera mediante la cual los navegadores deciden qué valores de una propiedad
son más relevantes para un elemento y, por tanto, serán aplicados.[^1]

Se aplica la siguiente norma de prioridad (cuanto mayor sea el número, más prioridad tiene):

0. **Selectores de tipo**
1. **Selectores de clase**, **selectores de atributos** y **pseudo-clases**
2. **Selectores de identificador**

Por lo tanto, si a un mismo elemento se está referenciando desde un selector de clase y otro de identificador, **tendrá
prioridad el de identificador** y **sus propiedades sobreescribirán a las de clase**. Véase el siguiente ejemplo:

=== "hoja.css"

    ```css
    .elemento {
        color: red;
        font-family: sans-serif;
    }

    #elemento {
        color: blue;
    }
    ```

=== "index.html"

    ```html
    <!-- El elemento se renderizará con las siguientes propiedades: -->
    <p
        id="elemento" class="elemento"
        style="color: blue; font-family: sans-serif;"/>
    ```

!!! warning "Selectores iguales"

    Si por algún motivo hubiese dos selectores idénticos, tendrá preferencia el último leído. Las propiedades se
    sobreescribirán en caso de conflicto a las últimas leídas.

### Modificador `#!css !important`

En CSS existe un modificador denominado `#!css #!important`, el cual dará "sobreescribe" las reglas de prioridad.
Sin embargo, por este motivo, usarlo supone una **mala práctica** y está **totalmente desaconsejado**, ya que rompe
la filosofía de cascada del propio lenguaje.

Siempre se deberá buscar una alternativa antes de usar `#!css !important`. En el ejemplo anterior, el renderizado
sería diferente:

=== "hoja.css"

    ```css
    .elemento {
        color: red !important;
        font-family: sans-serif;
    }

    #elemento {
        color: blue;
    }
    ```

=== "index.html"

    ```html hl_lines="4"
    <!-- El elemento se renderizará con las siguientes propiedades: -->
    <p
        id="elemento" class="elemento"
        style="color: red; font-family: sans-serif;"/>
    ```

## Herencia

Dependiendo de las propiedades CSS, **algunas se heredarán y otras no**. Esto se puede saber mirando la documentación
de cualquier propiedad en la web de [MDN Web Docs](https://developer.mozilla.org/es/docs/Web/CSS/Reference).

Las propiedades se pueden categorizar en dos tipos:

- **Propiedades heredadas**: su valor por defecto se computará con respecto al valor del "padre".
- **Propiedades no heredadas**: su valor por defecto está fijado a `initial`.

!!! tldr "Ejemplo"

    Los colores de letra (`#!css color`) son propiedades heredadas, mientras que los bordes (`#!css border`) no lo son.

### Palabras Clave

Al hablar de herencia, es necesario hablar de **4 palabras clave**, las cuales se pueden usar como valor en
prácticamente cualquier propiedad. Estas tienen diferentes efectos:

|                     | **Efecto**                                                                                                                                                                          | **Ejemplo**                      |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| **`#!css initial`** | Toma el valor inicial de la propiedad.                                                                                                                                              | `#!css color: initial;`          |
| **`#!css inherit`** | Fuerza (si es una propiedad no heredada) el valor al valor del elemento padre.                                                                                                      | `#!css border: inherit;`         |
| **`#!css revert`**  | _Revierte_ el valor en cascada del elemento, o al por defecto si no está siendo heredado.                                                                                           | `#!css color: revert;`           |
| **`#!css unset`**   | Si la propiedad es no heredada, tiene el mismo efecto que `#!css initial`, y de `#!css inherit` en caso contrario (_es decir, "resetea" cualquier propiedad al valor por defecto_). | `#!css background-color: unset;` |


[^1]: Tomado de [Especificidad](https://developer.mozilla.org/es/docs/Web/CSS/Specificity), MDN Web Docs.
