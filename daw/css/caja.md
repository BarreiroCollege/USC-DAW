# Modelo de Caja

A la hora de diseñar una página, el motor del navegador representará cada elemento como un cuadro rectangular según
el estándar **modelo de caja de CSS**. CSS determina el tamaño, posición y propiedades (color, fondo, etc.) de estos
cuadros.[^1]

La caja se compone de cuatro elementos:

- **Límite de contenido**: con su ancho y alto, es el espacio práctico donde se renderizan los hijos.
- **Límite de relleno** (_padding_): se denomina _padding_ al espacio que hay entre el borde y el límite del contenido.
- **Límite del borde** (_border_): será el espacio que ocuparán los bordes de la caja.
- **Límite del margen** (_margin_): es el espacio que hay entre la caja y las otras cajas (dos márgenes de dos 
  elementos distintos "no" se solaparán).

??? summary "Clica aquí para ver los elementos"

    ![Caja](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model/boxmodel-(3).png)


[^1]: Tomado de [Introducción al Modelo de Caja de CSS](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model),
      de MDN Web Docs.
