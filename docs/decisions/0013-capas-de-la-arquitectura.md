# Capas de la arquitectura

* Status: accepted
* Date: 2023-11-09

## Context and Problem Statement

Hemos decidido utilizar una estructura por 4 capas horizontales. Para ello hemos creado la capa del cliente, la capa de presentación, la capa de gestor negocios y la capa de datos.

## Decision Drivers

* Todos los requisitos se han tenido en cuenta para tomar esta decisión.

## Considered Options

* 001 - Crear capa de cliente
* 002 - Crear capa de presentación
* 003 - Crear capa de gestor de negocios
* 004 - Crear capa de datos

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 001

La capa de cliente debe contener la clase Usuario y las clases heredadas Cliente y Trabajador ya que en dicha capa se encuentran los usuarios que tienen acceso en el sistema.

### 002

La capa de presentación debe contener la clase GestorPedidos ya que es la que ve el usuario, presenta el sistema al usuario, le comunica la información y permite la comunicación entre los distintos componentes.

### 003

La capa de negocios debe contener las clases PlataformaPago, Repartos, Estadísticas e Incidencias, porque en esta capa se realizan las funciones principales de la aplicación (microservicios).

### 004

La capa de datos debe contener las clases Gateway y las dos bases de datos (Database_Clientes y Database_Pedidos) ya que se encarga de almacenar los datos (base de datos) y acceder a los mismos.
