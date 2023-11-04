# ADD01-Almacenar pedidos

* Status: accepted
* Date: 2023-11-04

## Context and Problem Statement

Se busca diseñar un sistema que permita recibir los pedidos realizados por los clientes y almacenarlos en una base de datos

## Decision Drivers

* RF06 - Hacer pedido
* RF11 - Ver estado del pedido

## Considered Options

* 001-Crear las clases correspondientes
* 002-Aplicar patrón Mediator para la clase GestorPedidos
* 003-Aplicar patrón Singleton para la clase GestorPedidos

## Decision Outcome

Chosen option: "001-Crear las clases correspondientes", because La clase Gateway se encargará de la comunicación con las bases de datos y la clase GestorPedidos se comunicará con el cliente y la clase Gateway

## Pros and Cons of the Options

### 001-Crear las clases correspondientes

Se crean la clase Gateway y GestroPedidos

### 002-Aplicar patrón Mediator para la clase GestorPedidos

La clase GestorPedidos hace de intermediario entre las clases Reportos, Incidencias, Estadísticas, PlataformaPago y Gateway para que una clase que se puede relacionarse con varias, pueda hacerlo a través de esta. Por lo tanto el uso del patron Mediator podría ser adecuado.

### 003-Aplicar patrón Singleton para la clase GestorPedidos

La clase GestorPedidos gestiona la información de un único pedido que puede consultar en la base de datos, por lo tanto el uso del patron Singleton podría ser adecuado.
