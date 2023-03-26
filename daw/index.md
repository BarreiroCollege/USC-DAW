# Apuntes DAW

El desarrollo web, a grandes rasgos, se puede diferenciar en dos grandes facciones:

- **Frontend**: es la parte que se muestra al usuario, la parte "bonita" donde se visualizan los datos y se
  interacciona con el contenido.
- **Backend**: es la parte servidor, donde se procesan los datos, la cual está protegida ante ingerencias externas, y 
  que se comunica con el frontend para visualizar los datos.

Hoy en día hay **múltiples formas de desarrollar una página web**. Algunas de las opciones más populares se listan a
continuación:

!!! summary "El servidor genera el propio frontend"

    Este método lo utilizan lenguajes como PHP o Python, los cuales son capaces de generar dinámicamente el contenido a
    visualizar. Por ejemplo, Laravel (un framework de PHP) se encargará de generar con anterioridad la página web en el
    propio servidor y mostrarla directamente al usuario.  
    El mayor inconveniente de este método es bastante difícil de hacer páginas webs "interactivas", en el sentido de
    que se actualice el contenido sin realizar una recarga de página.

!!! summary "El servidor se separa del frontend"

    Esta última opción es la más común hoy en día, y que sufrió un auge en los últimos años. Gracias a este método se
    pueden separar dos profesiones y permitir que los desarrolladores se centren en bien el frontend o bien el backend.
    De todas formas, es posible hacer ambas partes al mismo tiempo (denomindado "full-stack").  
    La base de este método radica en que el servidor (backend) será una API con JSON o similar, y la interfaz web
    (frontend) hará llamadas con JavaScript para obtener esos datos, generando y renderizando la interfaz en el propio
    navegador cliente.

## Apuntes

- **Tema 1**: [Introducción](intro/index.md)
- **Tema 2**: [HTML](html/index.md)
- **Tema 3**: [CSS](css/index.md)
