[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 03`](../Readme.md) > `Reto 2`
	
## Reto 2: Definición de vistas

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Definir vistas sobre algunas consultas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

---

<img src="../../imagenes/tabla.gif" align="right" height="170" width="200"> 

:warning: <ins>**IMPORTANTE**</ins>

_Para este reto necesitarás un identificador único. Tu identificador serán los últimos tres dígitos de tu número de celular. Por ejemplo, si tu número es: 5512345678 tu identificador debe ser 678. <ins>¡No lo olvides!</ins>_   

_**Te pedimos esto para que todos puedan realizar los ejemplos y retos.**_


_Si no sigues las instruciones..._   

---

Usando la base de datos `tienda`, define las siguientes vistas que permitan obtener la siguiente información.

**AÑADE A TODOS LOS NOMBRES DE TUS VISTAS EL SUFIJO `_<tu identificador>`.** Por ejemplo `mi_vista_hermosa_123`.

- Obtener el puesto de un empleado.
```mysql
CREATE VIEW R02E01_619 AS (
SELECT p.nombre puesto, CONCAT_WS(" ", e.nombre, e.apellido_paterno, e.apellido_materno) AS empleado
FROM empleado e
JOIN puest p ON e.id_puesto = p.id_puesto
)
```
- Saber qué artículos ha vendido cada empleado.
```mysql
CREATE VIEW R02E02_619 AS (
SELECT v.clave, e.nombre empleado, a.nombre articulo
FROM venta v
JOIN empleado e ON v.id_empleado = v.id_empleado
JOIN articulo a ON v.id_articulo = a.id_articulo
)
```
- Saber qué puesto ha tenido más ventas.
```mysql
CREATE VIEW R02E03_619 AS (
SELECT v.clave, e.nombre empleado, p.nombre puesto
FROM venta v
JOIN emplead e ON v.id_empleado = e.id_empleado
JOIN puesto p ON p.id_puesto = e.id_puesto
)
```
<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)

</div>
