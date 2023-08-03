[`Introducción a Bases de Datos`](../../README.md) > [`Sesión 04`](../Readme.md) > Reto 1

## Reto 1: Realizando operaciones con tablas

### 1. Objetivos :dart:
- Realizar operaciones SQL para administrar tablas
- Crear tablas acorde a los datos

### 2. Requisitos :clipboard:
- Servidor __MySQL__ instalado

### 3. Desarrollo :rocket:

1. Definir los campos y tipos de datos para la tabla `movies` haciendo uso de los archivos `movies.dat` y `README`.

1. Crear la tabla `movies` (recuerda usar el mismo nombre del archivo sin la extensión para vincular nombres de tablas con archivos).

1. Definir los campos y tipos de datos para la tabla `ratings` haciendo uso de los archivos `ratings.dat` y `README`.

1. Crear la tabla ratings (recuerda usar el mismo nombre del archivo sin la extensión para vincular nombres de tablas con archivos)

```mysql
CREATE TABLE IF NOT EXISTS users (
   user_id INT PRIMARY KEY,
   gender VARCHAR(13),
   age INT,
   occupation INT,
   zip_code VARCHAR(20)
);
CREATE TABLE IF NOT EXISTS movies (
   movie_id INT PRIMARY KEY,
   title VARCHAR(200),
   genres VARCHAR(100)
);
CREATE TABLE IF NOT EXISTS ratings (
   rating_id INT PRIMARY KEY,
   user_id INT,
   movie_id INT,
   rating FLOAT,
   timestamp INT,
   FOREIGN KEY (user_id) REFERENCES users(user_id),
   FOREIGN KEY (movie_id) REFERENCES movies(movie_id)
);
```
---

> **Nota:** *Observa que la tabla `ratings` requiere llaves foráneas. Revisa esta referencia o pregunta a tu experta(o): https://www.w3schools.com/sql/sql_foreignkey.asp*

> *Parte de tu formación como Data Scientist consiste en que aprendas a consultar documentación.* :nerd: Google es tu amigo. :heart:

---

<br/>

[`Anterior`](../Ejemplo-02/Readme.md) | [`Siguiente`](../Readme.md#importando-datos-a-una-tabla-en-formato-csv)   
