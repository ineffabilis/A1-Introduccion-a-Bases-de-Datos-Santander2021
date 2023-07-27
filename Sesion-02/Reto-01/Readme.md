[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 1`
	
## Reto 1: Agrupamientos y subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Qué artículos incluyen la palabra `Pasta` en su nombre?
```mysql
SELECT * FROM articulo WHERE nombre LIKE '%pasta%'
```
- ¿Qué artículos incluyen la palabra `Cannelloni` en su nombre?
```mysql
SELECT * FROM articulo WHERE nombre LIKE '%Cannelloni%'
```
- ¿Qué nombres están separados por un guión (`-`) por ejemplo `Puree - Kiwi`?
```mysql
SELECT * FROM articulo WHERE nombre LIKE '%-%'
```

<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md#funciones-de-agrupamiento)   


</div>
