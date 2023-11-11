# Herencia Usuario

* Status: ACCEPTED
* Date: 2023-11-09

## Context and Problem Statement

Nos encontramos con dos tipos de usuarios de la aplicación: clientes (los que realizan pedidos) y los trabajadores (los que se ocupan de la logística). Por lo tanto necesitamos diferenciar estos dos tipos de usuarios.

## Decision Drivers

* RF16 - Marcar pedido como entregado
* RF18 - Ver ruta pedido

## Considered Options

* 001-Creación clase Usuario
* 002-Creación clase Cliente
* 003-Creación clase Trabajador
* 004-Aplicar patrón Factory Method para la clase Usuario

## Decision Outcome

* 001-Creación clase Usuario
* 002-Creación clase Cliente
* 003-Creación clase Trabajador
* 004-Aplicar patrón Factory Method para la clase Usuario

## Pros and Cons of the Options

### 001-Creación clase Usuario

Debe haber una clase padre para los métodos que compartan los clientes y los trabajadores

* Good, because Evita que se repita el mismo código en clases distintas

### 002-Creación clase Cliente

La clase Cliente hereda de Usuario para poder realizar los métodos de la clase Usuario (necesarios para el cliente)

### 003-Creación clase Trabajador

La clase Trabajador hereda de Usuario para poder realizar los métodos de la clase Usuario (necesarios para el trabajador)

### 004-Aplicar patrón Factory Method para la clase Usuario

Se aplica el patrón Factory Method para poder crear objetos distintos (Cliente y Trabajador) a partir de una misma clase (Usuario)

* Good, because Permite reutilizar código y que cada clase hija tenga sus propios métodos concretos
