# Aprende a usar las APIs y Webservice de Prestashop

## Qué son APIs y Webservicesy para qué sirven.

Las APIs y Webservices son interfaces de sistemas para acceder a los mismos mediante desarrollos y programación. Dicho en simple, así como uno ingresa a un sitio web y la pantalla del monitor y/o teléfono celular son interfaces, y el navegador es otra, que nos permiten acceder a información de un programa y/o sitio web, las APIs son interfaces de acceso programático (mediante programación).

Las APIs son una forma de intercomunicar sistemas, sea entre el navegador y el 'programa' que está embebido en la página web, como entre sistemas entre sí, por ejemplo, entre dos sistemas bancarios o entre un sitio web y la plataforma de pagos. La API tiene documentado como acceder (protocolo, permisos, campos disponibles, si es de envío y/o recepción de información o ambas vías), si son privadas o públicas, etc. Los webservices son similares a las APIs, pero un tanto más antiguos.

> A fines prácticos diremos que son como comparar el inglés británico y el inglés americano; ambos son idima inglés, tienen diferente sintaxis y algunas cosas más, pero son comparables (digamos, sin profundizar en lo técnico).

Podemos entender rápidamente a las APIs y Webservices como una línea telefónica, una conversación o chat: hay un emisor, un receptor, un canal y un medio. Tenemos un número de teléfono a donde llamar (un endpoint o url, en caso de APIs), un canal o medio (el protocolo a usar, REST o SOAP, el formato JSON o XML, por ejemplo) y si es solo para hablar o tambièn para preguntar (POST, envío, GET consulta de información, etc).

> Las APIs o Webservice permiten una forma fácil y práctica de acceder a ciertos datos, con suficiente seguridad y posibilidades de restringirlos, sea mediante credenciales, VPN, protocolos, etc.

## APIs y Webservice en Prestashop Ecommerce.

Prestashop tiene desde hace años un Webservice bastante completo que permite integrar diferentes sistemas y módulos a una tienda online. Puedes además consultar mediante API y Webservice de prestashop para hacer reportes, tableros de control, manipular precios, generar facturación, automatizaciones y más.

#### El mismo Webservice de Prestashop es posible consultarlo mediante formato JSON de forma sencilla:

Por parámetro de URL

- `output_format=JSON`
- `io_format=JSON`

Por parámetro en Headers HTTP

- `Io-Format: JSON`
- `Output-Format: JSON`

Más adelante veremos sugerencias de uso y buenas prácticas sobre varios temas, uno de ellos es cuàl de estas modalidades se recomienda usar y por qué...

##### Como CRUD y REST, el Webservice / API de Prestashop admite:

Dependiendo la entidad y permisos activados a una KEY / cuenta / usuario, podremos acceder a realizar diferentes acciones. Aquí una equivalencia rápida y explicativa sobre el tema:

|   HTTP/REST |  CRUD   |   SQL     |
|   ---       |  ---    |   ---     |
|   POST      |	Create  |   INSERT  |
|   GET       |	Read    |	SELECT  |
|   PUT       |	Update  |	UPDATE  |
|   DELETE    |	Delete  |	DELETE  |


### A qué puedes acceder, como habilitarlo, permisos, seguridad y más:

El Webservice de Prestashop, y sus APIs, deben primero activarse en el back-office de la tienda en cuestión, además de generar una credencial o token, a fin de validarnos y que nos identifique. En la misma acción de crear el acceso, es necesario activar los permisos (GET, POST, PUT, DELETE, HEAD) para cada entidad y/o módulo o funcionalidad:



### Comienza a usar las APIs y Webservice de Prestashop con Postman

Una vez que tienes las credenciales que te brindó el administrador de la tienda, puedes probarlas fácil y rápido desde el navegador. Todos los navegadores hacen un GET por defecto, asi que nada más poner la url en el formato de abajo y podrás validar esten ok para comenzar:

1. example.com/api
    - te pedirá usuario y contraseña, al usuario lo dejas en blanco, a la password le pones el token que te compartieron.

2. {token}@example.com/api/
    - ingresas el token @ (arroba) el dominio de la tienda. Esta opción es MUY insegura, ya que pueden capturar el token y usarlo maliciosamente, pero para entornos de prueba va bien.

#### Valida permisos y accesos a la API de Prestashop:

Nada más ingresar con los métodos de arriba o si lo haces con Postman, verás a qué entidades tienes permisos de acceso:

image.png

### Desarrollos posibles y varias ideas para usar las APIs y Webservice de Prestashop