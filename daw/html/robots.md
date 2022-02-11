# Robots

Otro estándar de la Web es el conocido como **`robots.txt`**. Este define el comportamiento de los "robots indexadores"
de los motores de búsqueda dentro de las páginas web.

Para usarlo, basta con definir un archivo `robots.txt` en la raiz de la página web, y especificar las directivas de
comportamiento.

## Directivas

| Directiva             | Significado                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `all`                 | No hay restricciones de indexación ni presentación de contenido. _Es el valor por defecto._                                           |
| `noindex`             | No se muestra ni esta página ni un enlace "en caché" de los resultados de búsqueda.                                                   |
| `nofollow`            | No se siguen los enlaces de esta página.                                                                                              |
| `none`                | Equivalente a `noindex`, `nofollow`.                                                                                                  |
| `noarchive`           | No se muestra ningún enlace "en caché" en los resultados de búsqueda.                                                                 |
| `nosnippet`           | No se muestra ningún fragmento en los resultados de búsqueda de esta página.                                                          |
| `noodp`               | No se utilizan metadatos del proyecto [Open Directory](http://odp.org/) para los títulos o fragmentos que se muestran en esta página. |
| `notranslate`         | No se ofrece una traducción de esta página en los resultados de búsqueda.                                                             |
| `noimageindex`        | No se indexan las imágenes de esta página.                                                                                            |
| `unavailable_after:X` | No se muestra esta página en los resultados de búsqueda después de la fecha y hora especificadas en formato RFC 850.                  |

## Etiquetas meta

Se crea una etiqueta `meta` en la cabecera del documento con el siguiente contenido:

````html
<meta name="robots" content="noindex,nofollow"/>
````

## robots.txt

Se permite especificar los directorios a los que no pueden acceder los robots. Por ejemplo, si sólo se quiere permitir
el acceso al robot de Google, el contenido del archivo sería:

```text
User-agent: Google
Disallow:

User-agent: *
Disallow: /
```
