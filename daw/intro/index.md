# Evolución de la Computación

Para hablar sobre la historia de la computación, es necesario empezar hablando de **cómo empezó la
computación a nivel personal**.

!!! info "Ordenadores"

    * **Años 40**: Ordenadores personales "armario".
    * **Años 50**: Servidores con múltiples clientes a modo de ordenador personal (KVM).
    * **Años 80**: Ordenadores personales sobremesa.
    * **2007...**: Dispositivos móviles

Y en lo relativo a la web, como han ido evolucionando la **conexión por red** entre varias computadoras.

!!! info "Redes"

    * **Finales 80's - Primera mitad 90's**: LAN sin conexiones exteriores.
    * **Segunda mitad 90's**: Internet.

Con la incorporación de Internet a la vida cotidiana, aparecen unas **aplicaciones cliente/servidor
las cuales facilitan la transmisión de información**. Tradicionalmente, en estas aplicaciones era
necesario codificar la propia aplicación para la transmisión de datos. Sin embargo, en este caso las
aplicaciones ya vienen dadas (**navegadores web**) y lo que **se "programa" es el contenido a enviar**.

Aparece entonces también la distinción entre frontend y backend:

* **Frontend**: Parte de la aplicación que interactúa con el usuario (lado cliente).
    * Tipos de letra, colores, efectos del ratón, teclado, movimientos, desplazamientos, efectos visuales...
* **Backend**: El interior de la aplicación.
    * Servidores, bases de datos, aplicación en sí...

## Estadísticas

!!! warning "Estimaciones"

    Es imposible conocer a ciencia cierta estadísticas de uso de cualquier cosa en la web. Los datos mostrados
    aquí se basan en estimaciones y datos publicados en buena fé por algunas fuentes. Es por esto que, aunque
    parezca que cierta tecnología sea dominante, en realidad esté obsoleta hoy en día o pueda incluso representar
    vulnerabilidades de seguridad.

Se aprecia también un cambio de tendencia en cuanto al tipo de dispositivo dominante. En el último año
**caen las ventas de dispositivos en general**, pero afectando en mayor medida a los ordenadores y tablets:

| **Device Type** | **2021 Shipments (_Millions_)** | **2021 Growth (_%_)** | **2022 Shipments (_Millions_)** | **2022 Growth (_%_)** |
|-----------------|--------------------------------:|----------------------:|--------------------------------:|----------------------:|
| PC              |                             342 |                  11.0 |                             310 |                  -9.5 |
| Tablet          |                             156 |                  -0.8 |                             142 |                  -9.0 |
| Mobile Phone    |                            1567 |                   5.0 |                            1456 |                  -7.1 |
| Total Devices   |                            2065 |                   5.5 |                            1907 |                  -7.6 |

En cuanto a otras estadísticas de uso, se pueden destacar las siguientes:

!!! tip "Sistemas operativos más usados por clientes web"

    1. Android (_o basado en_): 40.76%
    2. Windows: 31.63%
    3. Apple iOS: 16.52%

!!! tip "Sistemas operativos de escritorio más usados para navegar"

    1. Windows: 73.72%
    2. macOS: 15.33%
    3. Desconocido: 6.67%

!!! tip "Sistemas operativos más usados para alojar páginas web"

    1. Unix: 80.5%
    2. Windows: 19.8%

## Evolución del Frontend

Hasta los primeros **años 2000**, la tecnología usada estaba restringida a lo más **básico de los estándares
HTML, CSS y JavaScript**. La construcción de una aplicación web se limitaba a:

1. Escribir y guardar el código en un editor de texto plano.
2. Abrir localmente, mediante un navegador los ficheros escritos, para chequear su correcto funcionamiento.
3. Desplegar los ficheros en un servidor web.

En el **2007 Apple presenta el iPhone 3**, y la computación doméstica se traslada a al **bolsillo**. Esto tiene varias
implicaciones:

1. Nuevos formatos de pantalla, totalmente incompatibles.
2. Nuevas versiones de navegadores que incluyen algunas etiquetas y otras no a medida que se va estandarizando.
3. Nuevas aplicaciones que incluyen contenido multimedia, cada vez más utilizado, redes sociales, localización.
4. Nuevos desarrollos, más completos compitiendo con las apps de los móviles.
5. Necesidad de reducción de ancho de banda y surgimiento de aplicaciones SPA.

Luego, en el 2018, **Google cambia su algoritmo de posicionamiento hacia una política "Mobile First Indexing"**.
Esto significa que Google mostrará en los dispositivos móviles las páginas que estén optimizadas para móviles, antes
que otras que no lo están. Por tanto, la responsividad (_capacidad de una página para responder a cambios de
tamaño_) se hace más importante.

Como consecuencia de todos estos cambios, la codificación de la página web se vuelve extremadamente compleja. Como
solución, el **JavaScript se convierte en protagonista en el desarrollo y aparecen nuevos frameworks y librerías**.

| **Nombre** | **Año** | **Creador**               | **Tipo**  | **Lenguaje**   |
|------------|---------|---------------------------|-----------|----------------|
| jQuery     | 2006    | John Resig                | Library   | JavaScript     |
| Backbone   | 2010    | Jeremy Ashkenas           | Library   | JavaScript     |
| AngularJS  | 2010    | Misko Hevery (Google)     | Framework | JavaScript     |
| Bootstrap  | 2011    | Mark Otto, Jacob Thornton | Library   | CSS/JavaScript |
| Ember      | 2011    | Yehuda Katz               | Framework | JavaScript     |
| React      | 2013    | Jordan Walke (Facebook)   | Library   | JavaScript     |
| Vue        | 2014    | Evan You (Google)         | Framework | JavaScript     |
| Angular    | 2016    | Google                    | Framework | JavaScript     |
| Svelte     | 2016    | Rich Harris               | Framework | JavaScript     |

A pesar de la aparición de tantas nuevas opciones, **jQuery sigue siendo el más dominante en todo el histórico** de
páginas web. Sin embargo, en los últimos años sí que se aprecia como **tecnologías más modernas van tomando terreno**
al facilitar el desarrollo de estas páginas más complejas.

Como consecuencia de esta evolución, la programación web en 2020 se ha orientado más a la **elección de
herramientas de desarrollo** que a la codificación en sí, por lo que se prima el uso de cajas negras.

| **Herramienta**     | **Uso**                               |
|---------------------|---------------------------------------|
| Angular Material UI | Formularios                           |
| Redux / MobX        | Manejo de flujos y control de estados |
| D3                  | Manipulación DOM                      |
| Moment.js           | Formateo de fechas                    |
| React DnD           | Drag & Drop Interfaces                |

La lengua más utilizada a día de hoy sigue siendo el **inglés**, con más del 55% del share.

## Evolución del Backend

El backend está muy influenciado por las preferencias del lenguaje de programación, utilizados por los
programadores.

!!! tip "Preferencia en lenguajes de programación según IEEE 2022 (normalizado)"

    1. Python: 100%
    2. C: 96.8%
    3. C++: 88.58%
    4. C#: 86.99%
    5. Java: 70.22%

Según el ranking TIOBE, se aprecia como **Java deja de ser el más predominante** los últimos años en favor de **Python
y C**. Sin embargo, estos rankings son de programación genéricos. Mirando exclusivamente el desarrollo de backends,
encontramos las siguientes preferencias:

!!! tip "Lenguajes más usados en backends"

    1. PHP: 78.1%
    2. ASP.NET: 7.9%
    3. Ruby: 6.0%
    4. Java: 3.7%
    5. Scala: 2.3%

PHP es el lenguaje predominante, pero **no es el mejor en cuanto a rendimiento con alto tráfico**. En este caso, **Java
y ASP.NET se comportan de mejor manera**.

En cuanto a los servidores de backend, también hay unos claros predominantes:

!!! tip "Servidores más utilizados"

    1. Nginx: 34.0%
    2. Apache: 33.1%
    3. Cloudflare Server (_proxy virtual, requiere de otro servidor por detrás_): 20.1%

## Desarrollo

A la hora de desarrollar aplicaciones web, se usarán estos 3 componentes en la asignatura:

* Frontend
  * HTML
  * CSS
  * JavaScript (_.jQuery, Bootstrap_)
* Backend
  * Java (_JSP_)
* Web Server
  * Apache
  * Tomcat


*[KVM]: Keyboard Video Mouse
*[LAN]: Local Area Networks
*[SPA]: Single Page Application
