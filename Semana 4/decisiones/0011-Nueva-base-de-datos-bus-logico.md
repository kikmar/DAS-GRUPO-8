# ADR-0011 Creación nueva base de datos y bus lógico

## Identificador del Requisito

Requisito a tratar: 
* [RF7](../Requisitos/rf7.md) "Creación nueva base datos "
* [RF8](../Requisitos/rf8.md) "Integración bus eventos lógicos"

## Contexto y problemas a resolver



## Decisiones a tratar:





## Decisiones tomadas

//las bases de datos deben comunicarse guardando la coherencia como dice el enunciado. Este bus, entre otras cosas debe generar los mensajes que le llegan a las aplicaciones moviles. Ejs: 
restock de productos incluidos en las preferencias del usuario, pedido enviado, devolucion completada, etc.

### Consecuencias positivas <!-- optional -->



### Consecuencias negativas <!-- optional -->


### Discusión ASC: Arquitectura de Microservicios
+ Bueno, ya que ofrece una persistencia y una gestión de los datos muy conveniente.
+ Bueno, ya que posee un sistema robusto en caso de fallo de un microservicio.
+ Bueno, ya que una buena sincronización entre las comunicaciones y las peticiones es algo indispensable en un sistema como el que pide el cliente.
- Malo, complejidad adicional de los sistemas distribuido.
- Malo, mayor consumo de recursos, puesto que cada microservicio tiene su propio Sistema Operativo y dependencias.

**Decisión ASC: Opcion 2**

## Decisión final tomada



## Capturas CONTROL 


## UML de la decisión






