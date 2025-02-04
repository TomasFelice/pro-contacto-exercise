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
### 6. ¿Cómo se envía la data en un Get y cómo en un POST? 
### 7. ¿Qué verbo http utiliza el navegador cuando accedemos a una página?
### 8. Explicar brevemente qué son las estructuras de datos JSON y XML dando ejemplo de estructuras posibles.
### 9. Explicar brevemente el estándar SOAP
### 10. Explicar brevemente el estándar REST Full
### 11. ¿Qué son los headers en un request? ¿Para qué se utiliza el key Content-type en un header?
