# Gestionar repartos

* Status: ACCEPTED
* Date: 2023-11-04

## Context and Problem Statement

Se debe desacoplar la funcionalidad del componente y escoger el algoritmo adecuado en funcion de la demora del camion

## Decision Drivers

* RF18 - Ver ruta

## Considered Options

* 001-Creacion clase GestorRuta
* 002-Creacion clase Repartos
* 003-Incorporar metodo elegirRuta()
* 004-Incorporar metodo elegirAlgoritmo()
* 005-Relacion entre Repartos y GestorPedidos

## Decision Outcome

* 001-Creacion clase GestorRuta
* 002-Creacion clase Repartos
* 003-Incorporar metodo elegirRuta()
* 004-Incorporar metodo elegirAlgoritmo()
* 005-Relacion entre Repartos y GestorPedidos

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
