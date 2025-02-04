# Ejercicio ProContacto - Salesforce Developer
## Ejercicio 1
### 1. Instalación del IDE (Visual Studio Code)
Para obtener un entorno de desarrollo local es fundamental el uso de un IDE (o editor de código), el cual utilizaremos para escribir el código que dará funcionalidad a nuestro software. La función del mismo es facilitar el proceso de desarrollo otorgando una serie de funcionalidades beneficiosas para programar.  
Si aún no tiene instalado **Visual Studio Code**, puede hacerlo desde [aquí](https://code.visualstudio.com/).  
En mi caso, ya tenía instalada previamente la herramienta por lo que no debí realizar el proceso de instalación.
### 2. Instalación de GIT y GIT Bash
En el desarrollo de software en general, es fundamental el uso de **GIT** para poder llevar un control de versiones. El mismo permite mantener un historial sobre todos los cambios que se hicieron en el código y ofrece diversas funciones para realizar el control.  
Por otro lado, **GIT Bash** es una terminal que soporta todas las funcionalidades de GIT. Se utiliza para poder ejecutar todos los comandos disponibles.  
Para clonar este repositorio en un entorno local usando GIT Bash es necesario:  
1. [Instalar Git y Git Bash](https://git-scm.com/)
2. Realizar la configuración inicial.
3. Ejecutar el comando `git clone https://github.com/TomasFelice/pro-contacto-exercise.git`  
Una vez realizados estos pasos, ya se habrá clonado el repositorio en su computadora local.

## Ejercicio 2
### 1. ¿Qué es un servidor HTTP?
Un servidor HTTP es un software especializado diseñado para procesar, gestionar y responder a solicitudes utilizando el protocolo de comunicación **HTTP** (perteneciente a la capa de aplicación del modelo OSI), o bien, su versión segura **HTTPS**.  
La función principal de estos servidores es facilitar la comunicación entre aplicaciones clientes y servidores, siendo uno de los protocolos de comunicación más utilizados.
### 2. ¿Qué son los verbos HTTP? Mencionar los más conocidos
Los verbos (o métodos) HTTP son acciones definidas por el mismo protocolo que indican la operación que un cliente desea realizar sobre un recurso alojado en el servidor HTTP. Son esenciales para las APIs RESTful. Entre los más conocidos podemos mencionar:
- **GET**: Se utiliza para *obtener información* de un recurso.
- **POST**: Se utiliza para *crear* un recurso
- **PUT**: Se utiliza para *actualizar por completo* un recurso.
- **PATCH**: Se utiliza para *actualizar parcialmente* un recurso.
- **DELETE**: Se utiliza para *eliminar* un recurso.  
Además de los mecionados, existen otros métodos tales como, HEAD, OPTIONS, CONNECT y TRACE. De hecho, también se está trabajando en crear un nuevo método llamado QUERY para solventar ciertas falencias de los métodos GET y POST. Dejo un [artículo](https://newsmarketech.com/tecnologia/nuevo-metodo-http-query-una-alternativa-a-get-y-post/) al respecto
### 3. ¿Qué es un request y un response en una comunicación HTTP? ¿Qué son los headers?
En una comunicación mediante el protocolo HTTP, un request es un mensaje (petición) que el cliente le envía al servidor usando uno de los verbos que mencioné anteriormente. Mientras que un response es todo lo contrario, es la respuesta que devuelve el servidor HTTP hacia el cliente luego de procesar la solicitud.  
En ambos se utilizan los llamados *"headers"*, los cuales consisten en una serie de **metadatos** en forma de `clave: valor` que sirven para indicar aspectos técnicos de la comunicación. 
### 4. ¿Qué es un queryString? (En el contexto de una url)
El queryString es una parte de la URL en la cual se envían datos adicionales al servidor para generar un comportamiento definido (filtrar, ordenar, etc.). El inicio del queryString está definido por un "?", cada parámetro se depara con un "&", y los parámetros se envían en formato de `clave=valor`. El mismo se utiliza en las peticiones que utilizan el método **GET**. Un ejemplo de queryString es: `https://tienda.com/productos?price_max=20000&color=red&order_by=price&direction=asc`. En el mismo se puede ver cómo solicitamos productos con precio máximo de 20000, de color rojo y además indicamos que los resultados se muestren ordenados por precio ascendentemente.
### 5. ¿Qué es el responseCode? ¿Qué significado tiene los posibles valores devueltos?
El respondeCode es un código numérico que indica el estado de la petición. Cada uno tiene un significado propio pero pueden categorizarse según su primer dígito de la siguiente manera:  
- **1XX**: Respuestas informativas
- **2XX**: Respuestas exitosas
- **3XX**: Redirecciones
- **4XX**: Errores en el cliente
- **5XX**: Errores en el servidor
Algunos de los más relevantes son: 200 (OK), 201 (CREATED), 404(NOT FOUND), 500(INTERNAL SERVER ERROR)
### 6. ¿Cómo se envía la data en un GET y cómo en un POST? 
- **GET**: Al realizar una petición GET, la data se envía mediante el queryString (mencionado y ejemplificado anteriormente)
- **POST**: Al realizar una petición POST, la data se envía en el cuerpo (body) de la petición. En este body, hay varias maneras de enviar la data:  
  - **application/x-www-form-urlencoded**: El formato es similar al queryString, con la diferencia de que va en el body. `name=Pepe&username=pepe1234&password=1234pepe`
  - **application/json**: Formato JSON. Es el más utilizado.
    ```json
    {
      "name": "Pepe",
      "username": "pepe1234",
      "password": "1234pepe"
    }
    ```
  - **multipart/form-data**: Utilizado para enviar archivos (imágenes, documentos, etc.).
### 7. ¿Qué verbo http utiliza el navegador cuando accedemos a una página?
Al acceder a una página en el navegador, lo que queremos hacer es *solicitar información* (en esta caso, el contenido de la página) al servidor. Por lo que el verbo HTTP que usaremos será el **GET**.
### 8. Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.
Tanto JSON como XML son formatos que permiten intercambiar información de manera estructurada. Cada una tiene su propia sintaxis, particularidades y casos de uso.
- **JSON**: Es un formato ligero basado en la sintaxis de objetos de Javascript.
  ```json
    {
      "name": "Pepe",
      "username": "pepe1234",
      "password": "1234pepe"
    }
  ```
- **XML**: Está diseñado para almacenar datos y es más complejo y pesado que JSON. El mismo se basa en el uso de tags personalizados y admite enviar *metadatos*.
  ```xml
    <user>
      <name>Tomás</name>
      <age>21</age>
      <hobbies>
        <hobbie>programar</hobbie>
        <hobbie>leer</hobbie>
      </hobbies>
      <address>
        <city>Buenos Aires</city>
        <postalCode>1768</postalCode>
      </address>
    </user>
  ```
### 9. Explicar brevemente el estándar SOAP
El estándar de comunicación SOAP se utiliza para intercambiar información estructurada en servicios web. Utiliza XML como formato de mensaje y opera sobre protocolos como HTTP, SMTP o TCP. Es conocido por su robustez, seguridad y capacidad para entornos empresariales complejos.
### 10. Explicar brevemente el estándar RESTful
El estándar de comunicación RESTful es utilizado para diseñar servicios web escalables y eficientes. Se basa en principios que aprovechan las capacidades nativas del protocolo HTTP, enfocándose en recursos identificables y operaciones estándar. Es ampliamente usado en APIs modernas por su simplicidad y flexibilidad. Utiliza los verbos que estuve mencionando anteriormente.
### 11. ¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
Como mencioné anteriormente, los headers en un request consisten en una serie de **metadatos** en forma de `clave: valor` que sirven para indicar aspectos técnicos de la comunicación. Estos pares clave-valor brindan información adicional sobre la solicitud, como el tipo de datos enviados, el formato esperado en la respuesta, credenciales de autenticación, o detalles técnicos del cliente. Son fundamentales para controlar cómo el servidor procesa la solicitud. En especial, el Content-type se utiliza para indicar el formato de los datos enviados en el body, el mismo es esencial para métodos como POST, PUT o PATCH.  
## Ejercicio 3
Al realizar la primer petición **GET** a la URL solicitada, podemos ver la respuesta en formato JSON que contiene un listado de "Contactos".
```json
{
    "-O8UTVzeBfYD61ak2RNs": {
        "email": "nicolas.cartechini@procontacto.com.mx",
        "name": "Nicolas Cartechini"
    },
    "-O8UVh-OxewafCq1p8Eq": {
        "email": "nicolas.cartechini@procontacto.com.mx",
        "name": "Nicolas Cartechini"
    },
    "-O9J8hAEN3clx__fFhSj": {
        "email": "jordan.godoy@procontacto.com.mx",
        "name": "Jordan"
    },
    "-O9Q1T_yfuXVda9wU8IF": {
        "email": "Thiago.kuperman@procontacto.com.mx",
        "name": "Thiago"
    },
    "-O9Q1yYchGkusWhmJMsM": {
        "email": "Thiago.kuperman@procontacto.com.mx",
        "name": "Thiago Kuperman"
    },
    "-O9Q2FBnAJZJbaHhLdOw": {
        "email": "Thiago.kuperman@procontacto.com.mx",
        "name": "Thiago Kuperman"
    },
    "-O9l377eitlf4Be_5jmz": {
        "name": "mighty moose"
    },
    "-OAxVxSBV0xh7pxO82yQ": {
        "email": "leonel.fuente@procontacto.com.mx",
        "name": "Leonel"
    },
    "-OBbRTCM2-76g2mjI33x": {
        "email": "leonardo.leon@procontacto.com.mx",
        "name": "Leonardo León"
    },
    "-OGCe47ypruh26oxhnvX": {
        "email": "sebastian.alamina@procontacto.com.mx",
        "name": "Sebastián"
    },
    "-OHid4-otgAe8VTAXoPV": {
        "email": "Federico.Gomez@procontacto.com.mx",
        "name": "Federico"
    }
}
```
Luego, al realizar la petición **POST** a la misma URL con los siguientes parámetros:  
```json
{
    "name":"Tomás Felice",
    "email":"tomas.felice@procontacto.com.mx"
}
```
Estamos creando un nuevo contacto con la información enviada. En la respuesta podemos ver lo que sería el "name" interno del contacto creado:
```json
{
    "name": "-OIHdERR-3t2lzAiY47u"
}
```
Por último, al volver a hacer la misma petición **GET**, podemos ver que se agregó un nuevo registro crrespondiente a los datos de la petición **POST** realizada:
```json
{
    "-O8UTVzeBfYD61ak2RNs": {
        "email": "nicolas.cartechini@procontacto.com.mx",
        "name": "Nicolas Cartechini"
    },
    "-O8UVh-OxewafCq1p8Eq": {
        "email": "nicolas.cartechini@procontacto.com.mx",
        "name": "Nicolas Cartechini"
    },
    "-O9J8hAEN3clx__fFhSj": {
        "email": "jordan.godoy@procontacto.com.mx",
        "name": "Jordan"
    },
    "-O9Q1T_yfuXVda9wU8IF": {
        "email": "Thiago.kuperman@procontacto.com.mx",
        "name": "Thiago"
    },
    "-O9Q1yYchGkusWhmJMsM": {
        "email": "Thiago.kuperman@procontacto.com.mx",
        "name": "Thiago Kuperman"
    },
    "-O9Q2FBnAJZJbaHhLdOw": {
        "email": "Thiago.kuperman@procontacto.com.mx",
        "name": "Thiago Kuperman"
    },
    "-O9l377eitlf4Be_5jmz": {
        "name": "mighty moose"
    },
    "-OAxVxSBV0xh7pxO82yQ": {
        "email": "leonel.fuente@procontacto.com.mx",
        "name": "Leonel"
    },
    "-OBbRTCM2-76g2mjI33x": {
        "email": "leonardo.leon@procontacto.com.mx",
        "name": "Leonardo León"
    },
    "-OGCe47ypruh26oxhnvX": {
        "email": "sebastian.alamina@procontacto.com.mx",
        "name": "Sebastián"
    },
    "-OHid4-otgAe8VTAXoPV": {
        "email": "Federico.Gomez@procontacto.com.mx",
        "name": "Federico"
    },
    // Aquí está el contacto creado
    "-OIHdERR-3t2lzAiY47u": {
        "email": "tomas.felice@procontacto.com.mx",
        "name": "Tomás Felice"
    }
}
```
