# ADR-0004 Gestion-de-compras-y-acceso-a-plataforma-de-pagos

## Identificador del Requisito

Requisito a tratar: 
* [RF3.2](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf3.2.md) "Módulo de detección de preferencias"
* [RF3.3](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf3.3.md) "Módulo de sistema de pago"

## Contexto y problemas a resolver

El cliente posee un sistema basado en una arquitectura Web de tres capas que desea migrar a una de microservicios. Las decisiones tomadas
se enfocarán en establecer una correcta gestión de las compras de los clienties. Los clientes deberían acceder a la plataforma de pago de una manera correcta y sin problemas,
integrando ésta en la nueva arquitectura de microservicios. Además, el sistema debe detectar las preferencias de los usuarios a la hora de realizar búsquedas, en función de las anteriormente realizadas.

## Decisiones a tratar:

* **Opcion 1**:  La base de datos NoQSL almacenará las preferencias de los usuarios en base a las búsquedas anteriormente realizadas en la aplicación. Cuando el usuario acceda a su perfil, ésta
debe devolver los datos del mismo, para actualizarse en función de las búsquedas que realice mientras esté conectado. Esta base de datos NoSQL debe estar implementada mediante un solo microservicio
con dos API (una para actualizarse en función de búsquedas, y otra para comunicarse con el módulo del cliente) ambas desarrolladas en JAVA. Por otro lado, debe existir un módulo diferenciado para conectarse con la API del banco asociado a la cuenta del usuario.
estos datos se guardarán con el resto de información del usuario en la base de datos NoSQL, y de nuevo, las clases asociadas estarán desarolladas en JAVA.
* **Opcion 2**: La lógica es la misma que en la opción 1, pero las API desarrolladas en Phyton puesto que es un lenguaje más potente e intuitivo.
* **Opcion 3**: La lógica es la misma que en la opción 1, pero las API desarrolladas en Node ya que es una opción perfectamente válida.



## Decisiones tomadas

Opción 1 elegida: Separar ambas las APIs en JAVA parece lo más correcto puesto que permite una mayor modularización de los contenidos, y por tanto, aseguramos una correcta
escalabilidad y flexibilidad en el sistema. Por otro lado, la lógica del sistema seguida por en todas las opciones es la más intuitiva y escalable, por lo que la consideramos, de nuevo, como correcta.

### Consecuencias positivas <!-- optional -->

* Seguridad en implementación con escalabilidad del sistema.
* Seguridad en implementación con flexibilidad del sistema.
* JAVA es un lenguaje preparado para albergar este tipo de aplicaciones, lo que puede ser de ayuda a la hora de implementarlo y escalarlo.
* El sistema de preferencias generado por búsquedas anteriores permite que el usuario encuentre productos parecidos a los que le interesan, y por tanto, que sea una herramienta útil para el cliente.
* La basde de datos NoSQL estaría correctamente conectada con los diferentes módulos del sistemas, y recopilar la información de los diferentes usuarios no es una operación complicada de realizar ni implementar, por lo que
 la escalabilidad se vuelve a respetar en este punto.
* Actualizar la base de datos una vez el usuario ha dejado de navegar por la aplicación con las nuevas preferencia generadas, permitirá que el dicho sistema de preferencias sea flexible y se adapte a los nuevos gustos de los usuarios.
* La forma de conectar con el banco es fácil de implementar puesto que muchas aplicaciones anteriormente han utilizado esta lógica, por lo que podemos encontrar mucha documentación y ejemplos en diferentes webs.

### Consecuencias negativas <!-- optional -->

* Separar en un sistema de dos APIs las implementaciones propuestas podría resultar confuso a la hora de conectarlas con los módulos de usuario e interfaz.
* Otros lenguajes de programación podrían resultar más interesantes para implementar el sistema, como por ejemplo Python, que nos ofrece posibilidades más allá de lo que se nos pide con librerias gratuitas. La escalabilidad podría verse afectada en futuras actualizaciones y mejoras del sistema.
* La lógica no parece revisable.
* La base de datos NoSQL puede verse afectada por una sobrecarga de importancia en la lógica planteada. Podría suponer un problema de escalabilidad.

### Discusión ASC: Arquitectura de Microservicios

+ Bueno, porque respeta los patrones de flexibilidad y escalabilidad
+ Bueno, ya que no presenta retos muy complicado en su implementación, y parece bastante modularizado
+ Bueno, ya que a priori el sistema es sencillo a pesar de estar separado en dos API, por lo que no parece que pueda llegar a causar confusión
+ Bueno, ya que el sistema de pago está probado y es recurrene en otras aplicaciones y servicios, por lo que es bastante genérico
+ Malo, ya que no se presentan diferentes posibilidades para la lógica del sistema.
+ Malo, ya que el lenguaje de programación más apropiado parece ser Python por enicma de JAVA

**Decisión ASC: Opcion 2**

## Decisión final tomada

Opción elegida: Opción 2.

## Capturas CONTROL 
![D0004](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/admentor/D0005.PNG)

## UML de la decisión






