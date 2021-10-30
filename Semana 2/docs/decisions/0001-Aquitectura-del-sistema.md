# ADR-0001 Arquitectura-del-sistema

## Identificador del Requisito

Requisito a tratar: [RF1] () "Elección de arquitectura"

## Contexto y problemas a resolver

El cliente posee un sistema basado en una arquitectura Web de tres capas que desea migrar a una de microservicios.

## Opciones consideradas

* [option1] [Arquitectura de Microservicios](https://docs.microsoft.com/es-es/azure/architecture/guide/architecture-styles/microservices) "Explicación Arquitectura de Microservicios"

## Decisiones tomadas

Opción elegida: [option1] porque es el sistema que quiere el cliente expresamente para mejorar la flexibilidad y escalabilidad.


### Consecuencias positivas <!-- optional -->

* Mejoras en la flexibilidad.
* Mejoras en la escalabilidad.
* Menos problemas para el cliente.
* Código y mantenimiento más legible.
* Facilidad a la hora de aplicar una implementación continua.


### Consecuencias negativas <!-- optional -->

* Posible dificultad a la hora de migrar el sistema.
* Tener verificado en la base de datos todos los microservicios del sistema para un mayor control

### Arquitectura de Microservicios

* Good, because [argument a]
* Good, because [argument b]
* Bad, because [argument c]

## Decisión final tomada

Opción elegida: [Arquitectura de Microservicios](https://docs.microsoft.com/es-es/azure/architecture/guide/architecture-styles/microservices) , porque es el sistema que quiere el cliente expresamente para mejorar la flexibilidad y escalabilidad.

## Capturas CONTROL 

## UML de la decisión

![Captura](https://user-images.githubusercontent.com/63242688/139542383-b1fce519-449d-430a-b3b3-5e0dcce4786a.png)




