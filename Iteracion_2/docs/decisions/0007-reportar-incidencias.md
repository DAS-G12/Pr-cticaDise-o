# Reportar incidencias

* Status:
*         Decision 004 - ACCEPTED
*         Decision 003 - REJECTED
* Date: 2023-11-04

## Context and Problem Statement

Es necesario reportar las incidencias que se produzcan en el reparto(camion averiado, reparto no realizado, etc.)

## Decision Drivers

* RF13 - Ver incidencia

## Considered Options

* 001-Creacion clase Incidencias
* 002-Incorporar método reportarIncidencia()
* 003-Relación entre Incidencias y Repartos
* 004-Relación entre Incidencias y GestorPedidos

## Decision Outcome

* 001-Creacion clase Incidencias
* 002-Incorporar método reportarIncidencia()
* 004-Relación entre Incidencias y GestorPedidos


## Pros and Cons of the Options

### 001-Creacion clase Incidencias

Es necesario una clase Incidencias para reportar los problemas que puedan surgir en el reparto

### 002-Incorporar método reportarIncidencia()

Es necesario un método que reporte la incidencia al gestor de repartos (clase Repartos)

### 003-Relación entre Incidencias y Repartos

Incidencias reporta el problema directamente al gestor de ruta (clase Repartos)

* Good, because Comunica la incidencia de forma directa
* Bad, because No cumple el patrón Mediator

### 004-Relación entre Incidencias y GestorPedidos

GestorPedidos utiliza a Incidencias para comunicar dicha incidencia a la clase Reparto

* Good, because Cumple el patrón Mediator
