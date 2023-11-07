# Almacenar pedidos

* Status: accepted
* Date: 2023-11-04

## Context and Problem Statement

Se busca diseñar un sistema que permita recibir los pedidos realizados por los clientes y almacenarlos en una base de datos

## Decision Drivers

* R01 - La aplicación debe ser capaz de manejar la parte del usuario
* R02 - La aplicación debe tener un "nexo" que es el GestorPedidos
* R03 - La aplicación debe permitir pagar mediante una plataforma externa
* R04 - La aplicación debe ser capaz de manejar la parte de los repartidores
* R05 - La aplicación debe separar las responsabilidades de cada parte
* R06 - La aplicación debe desacoplar la funcionalidad del componente de reparto de ruta

## Considered Options

* 001-Crear las clases correspondientes
* 002-Aplicar patrón Mediator para la clase GestorPedidos
* 003-Aplicar patrón Singleton para la clase GestorPedidos

## Decision Outcome

Chosen option: "001-Crear las clases correspondientes", because La clase Gateway se encargará de la comunicación con las bases de datos y la clase GestorPedidos se comunicará con el cliente y la clase Gateway

### Positive Consequences

* A la hora de desarrollar la aplicación las capas están bastante claras
* El diseño final quedará bastante claro
* Las relaciones entre capas pueden facilitar el proceso de comunicación entre componentes

### Negative Consequences

* Puede ser más difícil de adaptar

## Pros and Cons of the Options

### 001-Crear las clases correspondientes

Se crean la clase Gateway y GestroPedidos

* Good, because Facilidad a la hora de realizar interacciones con el servidor y datos
* Good, because De cara a ciertas funcionalidades puede ser muy útil
* Bad, because La arquitectura de cara al problema que tenemos puede resultar poco clara
* Bad, because En el caso de muchas peticiones el servidor puede colapsar

### 002-Aplicar patrón Mediator para la clase GestorPedidos

La clase GestorPedidos hace de intermediario entre las clases Reportos, Incidencias, Estadísticas, PlataformaPago y Gateway para que una clase que se puede relacionarse con varias, pueda hacerlo a través de esta. Por lo tanto el uso del patron Mediator podría ser adecuado.

* Good, because Permite separar claramente cada parte del programa o funcionalidad
* Good, because Tal y cómo se describe el programa, sus distintas funcionalidades se relacionan en un orden determinado
* Good, because Las capas están bastantes claras, lo que ayudará a no violar los principios de diseño
* Bad, because No se pueden hacer llamadas directas, lo cual para ciertos casos resultaría útil
* Bad, because Al estar separado por capas es más difícil implementar cararcterísticas que no encajen fácilmente en una capa existente
* Bad, because Es más difícil adaptar los cambios en requisitos

### 003-Aplicar patrón Singleton para la clase GestorPedidos

La clase GestorPedidos gestiona la información de un único pedido que puede consultar en la base de datos, por lo tanto el uso del patron Singleton podría ser adecuado.
