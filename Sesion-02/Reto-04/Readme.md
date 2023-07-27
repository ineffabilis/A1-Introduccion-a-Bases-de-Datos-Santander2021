[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 4`
	
## Reto 4: Subconsultas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el nombre de los empleados cuyo sueldo es menor a $10,000?
```mysql
SELECT empleado.nombre FROM empleado 
INNER JOIN puesto ON puesto.id_puesto = empleado.id_puesto
WHERE puesto.salario > 10000;
```
- ¿Cuál es la cantidad mínima y máxima de ventas de cada empleado?
```mysql
SELECT min(precio) AS venta_minima, max(precio) AS venta_maxima, CONCAT_WS(" ", empleado.nombre, empleado.apellido_paterno, empleado.apellido_materno) AS nombre_empleado
FROM empleado
INNER JOIN venta ON venta.id_empleado = empleado.id_empleado
INNER JOIN articulo ON articulo.id_articulo = venta.id_articulo
GROUP BY empleado.id_empleado;
```
- ¿Cuál es el nombre del puesto de cada empleado?
```mysql
SELECT empleado.nombre AS nombre_empleado, puesto.nombre AS puesto FROM empleado 
INNER JOIN puesto ON puesto.id_puesto = empleado.id_puesto;
```

<br/>

[`Anterior`](../Ejemplo-04/Readme.md) | [`Siguiente`](../Readme.md)            

</div>
