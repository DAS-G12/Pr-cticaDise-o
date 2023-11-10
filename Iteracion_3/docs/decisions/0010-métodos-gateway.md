# Métodos Gateway

* Status: accepted
* Date: 2023-11-08

## Context and Problem Statement

Necesita una clase Gateway que se comunique con la base de datos y con el GestorPedidos, ya que el GestorPedidos necesita consultar los datos del pedido o del usuario que se encuentran en la DataBase_Pedidos y en la DataBase_Clientes con frecuencia.

## Decision Drivers

* RF01 - Registrarse
* RF02 - Iniciar sesión
* RF03 - Ver perfil
* RF04 - Modificar perfil
* RF06 - Hacer pedido
* RF07 - Ver producto
* RF08 - Introducir datos
* RF10 - Introducir dirección
* RF11 - Ver estado del pedido
* RF12 - Ver información del cliente
* RF13 - Ver incidencia
* RF16 - Marcar pedido como entregado
* RF17 - Añadir a la cesta
* RF18 - Ver ruta pedido

## Considered Options

* 001-Incorporar método getInfo()
* 002-Incorporar método setInfo()
* 003-Incorporar método connectDB()
* 004-Incorporar método disconnectDB()

## Decision Outcome

* 001-Incorporar método getInfo()
* 002-Incorporar método setInfo()
* 003-Incorporar método connectDB()
* 004-Incorporar método disconnectDB()

## Pros and Cons of the Options

### 001-Incorporar método getInfo()

Debe haber un método getInfo() que devuelva la información de la base de datos

### 002-Incorporar método setInfo()

Debe haber un método getInfo(HTTP_Request) que reciba un HTTP request y que guarde o modifique la información en la base de datos

### 003-Incorporar método connectDB()

El Gateway debe contar con un método que le permita conectarse con las bases de datos.

### 004-Incorporar método disconnectDB()

El Gateway debe contar con un método que le permita desconectarse de las bases de datos.
