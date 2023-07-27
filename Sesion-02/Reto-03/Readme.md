[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 3`
	
## Reto 3: Agrupamientos

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuántos registros hay por cada uno de los puestos?
```mysql
SELECT nombre, count(*) AS cuenta FROM puesto GROUP BY nombre
```
- ¿Cuánto dinero se paga en total por puesto?
```mysql
SELECT nombre, sum(salario) AS salario_total FROM puesto GROUP BY nombre
```
- ¿Cuál es el número total de ventas por vendedor?
```mysql
SELECT id_empleado, count(*) AS venta_total FROM venta GROUP BY id_empleado
```
- ¿Cuál es el número total de ventas por artículo?
```mysql
SELECT id_articulo, count(*) AS venta_total FROM venta GROUP BY id_articulo
```
<br/>

[`Anterior`](../Ejemplo-03/Readme.md) | [`Siguiente`](../Readme.md)         

</div>
