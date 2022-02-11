# Codificación

Dado que HTML pretende ser un documento en formato de texto universal, **es necesario declarar el conjunto de símbolos
utilizado** (es decir, la _codificación de caracteres_).

Esto se consigue con la etiquieta `<meta>`, la cual tiene otras funciones:

```html hl_lines="3"
<html>
  <head>
    <meta http-equiv="content-type" content="text/html; charset=[encoding]"/>
    <title>Desarrollo de Aplicaciones Web</title>
  </head>
  
  <body>
    <h1>Bienvenidos a la página web de DAW</h1>
    <p>
      Esta página web de la asignatura...
    </p>
  </body>
</html>
```

## Valores a usar

Los valores disponibles aparecen en la [lista de W3C](http://www.w3.org/International/O-Charset-lang.html). Por
ejemplo, para el español sería `iso-8859-1`.

Sin embargo, estos valores se encuentran obsoletos en la actualidad. Hoy en día se utiliza la codificación `UTF-8`, la
cual incluye casi todos los caracteres ya de manera universal:

```html
<meta http-equiv="content-type" content="text/html; charset=utf8"/>
```
