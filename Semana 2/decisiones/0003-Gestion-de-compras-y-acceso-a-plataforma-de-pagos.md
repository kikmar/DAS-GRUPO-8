# ADR-0001 Migración-nueva-arquitectura

## Identificador del Requisito

Requisito a tratar: 
* [RF2](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf2.md) "Control y gestión de compras de clientes" 
* [RF2.1](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf2.1.md) "Gestión de preferencias para compras"
* [RF2.2](https://github.com/kikmar/DAS-GRUPO-8/blob/feature/Semana2/Semana%202/Requisitos/rf2.2.md) "Acceso a sistemas de pago "

## Contexto y problemas a resolver

El cliente posee un sistema basado en una arquitectura Web de tres capas que desea migrar a una de microservicios. Las decisiones tomadas
se enfocarán en establecer una correcta gestión de las compras de los clienties. Los clientes deberían acceder a la plataforma de pago de una manera correcta y sin problemas,
integrando ésta en la nueva arquitectura de microservicios.

## Decisiones a tratar:



## Decisiones tomadas

La decisión tomada para estos requisitos es comprobar durante el desarrollo de la migración la sostenibilidad de las funcionalidades en cuanto a escalabilidad
y flexibilidad. No podemos implementarlas como tal, pero sí asegurar mediante la creación de las clases, que éstas serán escalables y flexibles.

### Consecuencias positivas <!-- optional -->

* Seguridad en implementación de escalabilidad.
* Seguridad en implementación de flexibilidad.
* Revisión continua de estas características.
* Nivel detallado de estas características.


### Consecuencias negativas <!-- optional -->

* No se vislumbra una escalabilidad palpable desde el comienzo del desarrollo de la migración
* Posible pérdida del contacto con estos requisitos durante el desarrollo de la migración

### Discusión ASC: Arquitectura de Microservicios

En esta decisión, los ASC no toman parte del proceso porque se encargarán de revisarlo periodicamente durante el desarrollo de la migración y la implementación
de la arquitectura de microservicio.

**Decisión ASC: arquitectura suspendida**

## Decisión final tomada

Opción elegida: Revisión de la escalabilidad y flexibilidad de la arquitectura.

## Capturas CONTROL 

## UML de la decisión

No se realiza ningún esquema UML debido a que es una decisión general de arquitectura sin tratar ninguna clase en concreto.




