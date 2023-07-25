[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 01`](../Readme.md) > `Reto 1`
	
## Reto 1: Estructura de una tabla

<div style="text-align: justify;">

### 1. Objetivos :dart:

- Consultar la estructura de algunas tablas.

### 2. Requisitos :clipboard:

1. MySQL Workbench instalado.

### 3. Desarrollo :rocket:

Usando la base de datos `tienda`, muestra la descripción de las tablas `articulo`, `puesto` y `venta`. Por cada tipo de dato que encuentres llena la siguiente tabla (a mano, puedes dibujarla en un cuaderno o dónde tú prefieras). Usa la [Documentación de MySQL](https://dev.mysql.com/doc/refman/8.0/en/data-types.html) como referencia si no recuerdas cómo se usa un comando, o por supuesto, preguntarle al experto.

```mysql
DESCRIBE articulo;
```
```mysql
DESCRIBE puesto;
```
```mysql
DESCRIBE venta;
```
| Tipo   | Descripción |
|---|---|
|int   |Permite números desde -2147483648 hasta 2147483647. Si se define como *UNSIGNED* (sin signo) permite números desde 0 hasta 4294967295   |
|double   |Permite almacenar números decimales de punto flotante grandes, por lo que sus cálculos son aproximados.   |
|varchar   |Permite almacenar una cadena de datos (caracteres, números y caracteres especiales) con longitud variable. No reserva el espacio de la longitud máxima definida, ya que ocupa espacio del tamaño real de los datos. La longitud máxima es de 255.   |
|timestamp   |Permite almacenar fecha y hora con el formato YYYY-MM-DD HH:MM:SS (4 dígitos para el año, 2 dígitos para el mes, 2 dígitos para el día, 2 dígitos para las horas, 2 dígitos para los minutos y 2 dígitos para los segundos). El rango soportado es de '1970-01-01 00:00:01' UTC a '2038-01-19 03:14:07' UTC.   |

<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md)

</div>
