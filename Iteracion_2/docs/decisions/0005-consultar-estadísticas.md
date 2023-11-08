# Consultar estadísticas

* Status: ACCEPTED
* Date: 2023-11-04

## Context and Problem Statement

Se necesita un componente (Estadisticas) en el cual poder acceder al estado del pedido y a la informacion del cliente

## Decision Drivers

* RF11 - Ver estado del pedido
* RF12 - Ver informacion del cliente

## Considered Options

* 001-relacion entre GestorPedidos y Estadisticas
* 002-incorporar metodo getEstadoPedido()
* 003-incorporar metodo getEstadoVehiculo()
* 004-incorporar metodo getInfoCliente()

## Decision Outcome

Chosen option: "", because comes out best.

### Positive Consequences

* A la hora de desarrollar la aplicación las capas están bastante claras
* El diseño final quedará bastante claro
* Las relaciones entre capas pueden facilitar el proceso de comunicación entre componentes

### Negative Consequences

* Puede ser más difícil de adaptar

## Pros and Cons of the Options

### 001-relacion entre GestorPedidos y Estadisticas

GestorPedidos utiliza el componente Estadisticas para poder acceder a la informacion en tiempo real del camion, y Estadisticas utiliza GestorPedidos para poder acceder a la informacion de los clientes y del pedido

### 002-incorporar metodo getEstadoPedido()

la clase Estadisticas debe poder saber el estado del pedido en todo momento

### 003-incorporar metodo getEstadoVehiculo()

la clase Estadisticas debe poder saber el estado del vehiculo en tiempo real

### 004-incorporar metodo getInfoCliente()

la clase Estadísticas debe poder proporcionar también informacion del cliente
