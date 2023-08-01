[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 03`](../Readme.md) > `Reto 1`
	
## Reto 1: Agrupamientos y subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el nombre de los empleados que realizaron cada venta?
```mysql
SELECT e.nombre, e.apellido_paterno, v.id_venta
FROM empleado e
JOIN venta v ON e.id_empleado = v.id_empleado
```
- ¿Cuál es el nombre de los artículos que se han vendido?
```mysql
SELECT v.id_venta, a.nombre FROM venta v
JOIN articulo a ON v.id_articulo = a.id_articulo
```
- ¿Cuál es el total de cada venta?
```mysql
SELECT  v.id_venta, (a.precio + a.iva) * cantidad as totalVenta
FROM venta v
JOIN articulo a ON a.id_articulo = v.id_articulo
```
<br/>

[`Anterior`](../Ejemplo-01/Readme.md) | [`Siguiente`](../Readme.md)

</div>
