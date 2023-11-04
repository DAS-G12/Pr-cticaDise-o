# Almacenar pedidos

* Status: accepted
* Date: 2023-11-04

## Context and Problem Statement

Se busca diseñar un sistema que permita recibir los pedidos realizados por los clientes y almacenarlos en una base de datos

## Decision Drivers

* RF06 - Hacer pedido
* RF11 - Ver estado del pedido

## Considered Options

* 001-Crear las clases correspondientes

## Decision Outcome

Chosen option: "001-Crear las clases correspondientes", because La clase Gateway se encargará de la comunicación con las bases de datos y la clase GestorPedidos se comunicará con el cliente y la clase Gateway

## Pros and Cons of the Options

### 001-Crear las clases correspondientes

Se crean la clase Gateway y GestroPedidos
