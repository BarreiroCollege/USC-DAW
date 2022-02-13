# CSS

CSS, por sus siglas en inglés de _Hoja de Estilo en Cascada_, es el **lenguaje de estilos utilizado para describir la
presentación de documentos HTML**. CSS describe como debe ser renderizado el elemento estructurado en la pantalla, en
papel, o en el habla o en otros medios.[^1]

!!! tip "Datos rápidos"

    - Es el mecanismo para **insertar estilo** en las páginas webs.
    - El estilo se refiere a colores, formatos, posicionamiento, etc. (e incluso animaciones) de los elementos en la
      página.
    - Posibilita la **separación de contenidos** y **presentación** en una página web, siendo en la actualidad una
      recomendación de W3C.

## Estructura Básica

Toda regla de estilo incluida en una hoja de estilos consta de dos partes:

- Un **selector**: especifica que elementos se ven afectados.
- La **declaración**: uno (o más) pares de propiedad-valor, que especifican los cambios de estilo.

```css
h1 { /* (1) */
    color: red; /* (2) */
    background: yellow;
}
```

1. `#!css h1` hace referencia al **selector**, y las llaves abren el inicio de la **declaración**.
2. `#!css color` es la propiedad a afectar (_el color del texto en este caso_) y `#!css red` es el valor (_rojo_).

En CSS, hay 3 formas distintas de aplicar los estilos a los elementos HTML:

- Usando el **atributo `#!css style`** de cualquier elemento HTML (en este caso no hay selector).
- Usando **hojas de estilo internas**.
- Usando **hojas de estilo externas**, importándolas o bien en el HTML o en otras hojas CSS.

!!! info "Hoja de estilos **en cascada**"

    Por norma general, los cambios que afectan a un elemento afectarán y se propagarán a los hijo.


[^1]: Tomado de CSS: [Hojas de estilo en cascada](https://developer.mozilla.org/es/docs/Web/CSS), de MDN Web Docs.

*[CSS]: Cascading Style Sheet
