# Seleccion-Estilo-Arquitectura

* Status: proposed
* Date: 2023-10-24

## Context and Problem Statement

Para este proyecto de desarrollo software, hemos decidido implementar una arquitectura por capas, ya que a priori, creemos que es la que mejor se adapta a nuestra aplicación,  debido a ciertos requisitos y a la comunicación entre módulos. No obstante, la arquitectura cliente-servidor nos puede resultar útil de cara a implementar ciertas funcionalidades dentro de los módulos. Por lo tanto, la arquitectura por capas será la principal, sin embargo, no descartamos usar la arquitectura cliente-servidor dentro de algún módulo o capa.

## Decision Drivers

* R01 - La aplicación debe ser capaz de manejar la parte del usuario
* R02 - La aplicación debe tener un "nexo" que es el GestorPedidos
* R03 - La aplicación debe permitir pagar mediante una plataforma externa
* R04 - La aplicación debe ser capaz de manejar la parte de los repartidores
* R05 - La aplicación debe separar las responsabilidades de cada parte
* R06 - La aplicación debe desacoplar la funcionalidad del componente de reparto de ruta

## Considered Options

* 0001-1-Arquitectura-Cliente-Servidor
* 0001-2-Arquitectura-Por-Capas

## Decision Outcome

Chosen option: "0001-2-Arquitectura-Por-Capas", because Teniendo en cuenta el problema propuesto, aparentemente es la arquitectura que mejor se adapta

### Positive Consequences

* A la hora de desarrollar la aplicación las capas están bastante claras
* El diseño final quedará bastante claro
* Las relaciones entre capas pueden facilitar el proceso de comunicación entre componentes

### Negative Consequences

* Puede ser más difícil de adaptar

## Pros and Cons of the Options

### 0001-1-Arquitectura-Cliente-Servidor

Los clientes acceden a los datos y aplicaciones en los servidores

* Good, because Facilidad a la hora de realizar interacciones con el servidor y datos
* Good, because De cara a ciertas funcionalidades puede ser muy útil
* Bad, because La arquitectura de cara al problema que tenemos puede resultar poco clara
* Bad, because En el caso de muchas peticiones el servidor puede colapsar

### 0001-2-Arquitectura-Por-Capas

Cada capa soporta una parte del programa o una API que se relaciona con una capa superior

* Good, because Permite separar claramente cada parte del programa o funcionalidad
* Good, because Tal y cómo se describe el programa, sus distintas funcionalidades se relacionan en un orden determinado
* Good, because Las capas están bastantes claras, lo que ayudará a no violar los principios de diseño
* Bad, because No se pueden hacer llamadas directas, lo cual para ciertos casos resultaría útil
* Bad, because Al estar separado por capas es más difícil implementar cararcterísticas que no encajen fácilmente en una capa existente
* Bad, because Es más difícil adaptar los cambios en requisitos
