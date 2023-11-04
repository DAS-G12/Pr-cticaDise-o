# Gestionar repartos

* Status: proposed
* Date: 2023-11-04

## Context and Problem Statement

Se debe desacoplar la funcionalidad del componente y escoger el algoritmo adecuado en función de la demora del camión

## Decision Drivers

* RF18 - Ver ruta

## Considered Options

* 001-Creación clase GestorRuta
* 002-Creación clase Repartos
* 003-Incorporar método elegirRuta()
* 004-Incorporar método elegirAlgoritmo()
* 005-Relación entre Repartos y GestorPedidos

## Decision Outcome

* 002-Creación clase Repartos
* 003-Incorporar método elegirRuta()
* 004-Incorporar método elegirAlgoritmo()
* 005-Relación entre Repartos y GestorPedidos

## Pros and Cons of the Options

### 001-Creacion clase GestorRuta

Se crea una clase llamada GestorRuta ya que Incidencias reporta dicha incidencia al gestor de la ruta

### 002-Creacion clase Repartos

Dicha clase devuelve la mejor ruta al GestorPedidos

### 003-Incorporar metodo elegirRuta()

Se necesita un método que reciba Pedidos para devolver el tiempo que tardará el repartidor en realizar la ruta

### 004-Incorporar metodo elegirAlgoritmo()

Se necesita un método que reciba el tiempo que va a tardar el repartidor para poder escoger que algoritmo de optimización aplicar, para así devolver la ruta final a realizar.

### 005-Relacion entre Repartos y GestorPedidos

GestorPedidos utiliza el componente Repartos para saber la ruta que debe seguir un pedido
