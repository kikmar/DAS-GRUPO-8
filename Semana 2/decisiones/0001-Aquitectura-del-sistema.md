# ADR-0001 Arquitectura-del-sistema

## Identificador del Requisito

Requisito a tratar: 
* [RF1](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf1.md) "Elección de arquitectura" 
* [RF1.1](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf1.1.md) "Arquitectura de microservicios"

## Contexto y problemas a resolver

El cliente posee un sistema basado en una arquitectura Web de tres capas que desea migrar a una de microservicios.

## Opciones consideradas

* Opcion 1: [Arquitectura de Microservicios](https://docs.microsoft.com/es-es/azure/architecture/guide/architecture-styles/microservices) "Explicación Arquitectura de Microservicios"

## Decisiones tomadas

Opción 1 elegida (Arquitectura de Microservicios) porque es el sistema que quiere el cliente expresamente para mejorar la flexibilidad y escalabilidad.


### Consecuencias positivas <!-- optional -->

* Mejoras en la flexibilidad.
* Mejoras en la escalabilidad.
* Menos problemas para el cliente.
* Código y mantenimiento más legible.
* Facilidad a la hora de aplicar una implementación continua.
* Es el que ha solicitado el cliente.


### Consecuencias negativas <!-- optional -->

* Posible dificultad a la hora de migrar el sistema.
* Tener verificado en la base de datos todos los microservicios del sistema para un mayor control

### Discusión ASC: Arquitectura de Microservicios

* Bueno, porque es la arquitectura que ha solicitado el cliente
* Bueno, porque los microservicios son más fáciles de mantener y testear, puesto que son servicios pequeños que hacen una sóla cosa, pero la hacen bien.
* Bueno, ya que al no estar integrados en el sistema principal, son de fácil despliegue.
* Bueno, ya que pueden tener una escalabilidad independiente y es más sencillo aislar fallos a un microservicio concreto, en vez de una sección o funcionalidad de la aplicación.
* Malo, porque hay que lidiar con la complejidad adicional de los sistemas distribuidos.
* Malo, porque hay que implementar dependencias de un servicio a otro, comunicación interna entre servicios, etc.
* Malo, porque implica un mayor consumo de recursos, puesto que cada microservicio tiene su propio SO y dependencias.

**Decisión ASC: arquitectura aceptada**

## Decisión final tomada

Opción elegida: [Arquitectura de Microservicios](https://docs.microsoft.com/es-es/azure/architecture/guide/architecture-styles/microservices) , porque es el sistema que quiere el cliente expresamente para mejorar la flexibilidad y escalabilidad.

## Capturas CONTROL 

## UML de la decisión

![Captura](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/uml/Captura.png)




