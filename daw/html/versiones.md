# Versiones de HTML

En **HTML 4** y **XHTML 1**, se definieron varios tipos de versiones, siendo unas más flexibles que otras para poder
usar (o no) etiquetas personalizadas.

Vienen definidas por DTD, y se incluyen en el `DOCTYPE`. Estas ya **no son necesarias en HTML 5**, pero W3C sigue
manteniendo el validador [validator.w3.org](http://validator.w3.org/).

## Estricta

=== "HTML"

    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
    "http://www.w3.org/TR/html4/strict.dtd">
    ```

=== "XHTML"

    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
    ```

Sólo se permite el uso de etiquetas actualmente aprobadas.

## Transitoria

=== "HTML"

    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
    "http://www.w3.org/TR/html4/loose.dtd">
    ```

=== "XHTML"

    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
    ```

Se permite el uso de etiquetas no aprobadas y obsoletas (como `<font>`).

## Conjunto de Marcos

=== "HTML"

    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN"
    "http://www.w3.org/TR/html4/frameset.dtd">
    ```

=== "XHTML"

    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
    ```

Al igual que en la transitoria, se permite el uso de etiquetas no aprobadas y obsoletas, pero además se permite el uso
de marcos (_frames_, `<frameset>`), los cuales están desaconsejados por W3C en la actualidad.


*[DTD]: Document Type Definition
