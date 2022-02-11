# Publicación de una Página Web

Para entender la publicación de páginas web estáticas, es necesario entender la estructura de las direcciones URL:

- **`https://www.lawebdepepe.com/index.html`**
    - **`https`**: Protocolo con el que se accede.
    - **`www.lawebdepepe.com`**: Nombre del servidor (asociado a una IP, con _excepciones_). [^1]
        - **`www`**: Subdominio del dominio (cabe mencionar que se pueden crear múltiples subdominios a diferente nivel, ya
          que una vez se tiene el dominio, _todo lo anterior_ es personalizable).
        - **`lawebdepepe.com`**: Dominio de la página.
            - **`com`**: TLD, o dominio de nivel superior.
    - **`index.html`**: Ruta a la que acceder del servidor. Se deberá definir el origen en el servidor.
  
## Disponibilidad

Para "servir" una página web y hacerla disponible al público, es necesario disponer de un ordenador conectado a
Internet. Esto puede cumplirse, por ejemplo, con alguna de estas opciones:

- **Inserción en servidor web propio**: se dispone de un servidor propio, y se configura para servir la página web al
  público.
- **Hosting**: se subcontrata un servicio de alojamiento y se mantiene sin requerir una ubicación física propia.

## Organizaciones Involucradas

En caso de querer **hacer pública una web a través de un nombre de dominio**, es necesario ser propietario de algún
dominio, los cuales son de pago y se **renuevan anualmente**. [^2]  
El proceso de registro de dominio es bastante sencillo, pero hay varios tipos de empresas y organizaciones involucradas:

- **ICANN**: _Corporación de Internet para la Asignación de Nombres y Números_. Son una organización sin ánimo de lucro,
  de la cual se podría decir que depende todo Internet. Gestionan la asignación de dominios de nivel superior. Se
  llevan unos pocos céntimos de cada registro/renovación/transferencia.
- **Registry**: Empresa/Organización encargada de gestionar un dominio de nivel superior (`.com`, `.gal`, etc.).
  Mantiene los datos de quien ha registrado cada dominio sobre su TLD.
- **Registrar**: Empresa/Organización autorizada por el _Registry_ para vender y asignar los dominios. Suele haber
  varias para un mismo TLD.

Y finalmente, a la persona que registra un dominio a través de un _Registrar_, se le conoce como **Registrant**.

!!! tip "Google como Registry y Registrar"

    Una norma que tiene la ICANN sobre **los _Registry_ y los _Registrar_ deben ser entidades separadas**. Un _Registry_
    nunca podrá vender ni asignar dominios, solo mantener los datos como lugar "centralizado" para evitar el caos. Sin
    embargo, Google es capaz de ser tanto _Registry_ como _Registrar_, ya que ellos tienen sus propios TLD (como
    `.google` o `.dev`).  
    Esto lo consiguen operando como _Registry_ bajo otro nombre: **Charleston Road Registry**. Es decir, a la hora de
    comprar un dominio a través de Google, Google (_Registrar_) registrará el dominio y notificará a CRR (_Registry_)
    de que ese dominio ha sido registrado.

Simplemente mencionar además, que hay todo un mercado por detrás de los dominios de compra-venta. Existen revendedores
de dominio que se encargan de adquirir dominios no renovados y venderlos a una cantidad superior al coste, o empresas
enteras que compran dominios "comunes" para luego venderlos a mayor precio a quien lo necesite.

### Datos de Dominio

Cuando se registra un dominio en Internet, **los datos del que registra el dominio (el propietario) se guardan** en una
base de datos pública que funciona con el **protocolo WHOIS**. Este protoclo es universal, y los _Registrar_ que venden
un dominio tendrán que ser capaces de devolver los datos del _Registrant_ a través de este protocolo.

Hay 4 puntos de contacto que se deben almacenar:

- **Registrant**: datos de la persona que registró el dominio.
- **Administrator**: datos de la persona que está administrando el dominio.
- **Technical**: datos de la persona con los conocimientos técnicos para configurar el DNS y la puesta en marcha.
- **Billing**: datos de facturación del dominio.

Los datos que se almacenan son, entre otros: nombre y apellidos, dirección, teléfono e email. Sin embargo, **es muy
común que esas 4 personas sean la misma**.


[^1] Es posible asociar los nombres de dominios a otros nombres de dominios (registros `CNAME`), pero en algún punto
     deberá haber una IP para poder resolver la dirección final.
[^2] Hay una serie de dominios que son gratis, los cuales son adquiribles a través de [Freenom](https://freenom.com).
     Sin embargo, por este mismo motivo de ser gratis, suelen tener mala reputación por ser causa frecuente de
     actividades maliciosas.

*[URL]: Uniform Resource Locator
*[TLD]: Top-Level Domain
*[ICANN]: Internet Corporation for Assigned Names and Numbers
*[DNS]: Domain Name System
