[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 02`](../Readme.md) > `Reto 2`
	
## Reto 2: Funciones de agrupamiento

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Escribir consultas que permitan responder a algunas preguntas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, escribe consultas que permitan responder las siguientes preguntas.

- ¿Cuál es el promedio de salario de los puestos?
```mysql
SELECT AVG(salario) FROM puesto
```
- ¿Cuántos artículos incluyen la palabra `Pasta` en su nombre?
```mysql
SELECT COUNT(*) FROM articulo WHERE nombre LIKE '%pasta%'
```
- ¿Cuál es el salario mínimo y máximo?
```mysql
SELECT MIN(salario) AS salario_minimo, MAX(salario) AS salario_maximo FROM puesto
```
- ¿Cuál es la suma del salario de los últimos cinco puestos agregados?
```mysql
SELECT SUM(salario) FROM (SELECT salario FROM puesto ORDER BY id_puesto DESC LIMIT 5) x
```

<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)      

</div> 
