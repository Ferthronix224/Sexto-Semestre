---
layout: post
title: Topicos de Bases de Datos
subtitle: Mejorando el estudio
cover-img: /assets/img/bases.jpg
thumbnail-img: /assets/img/data.png
share-img: /assets/img/bases.jpg
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

## Temas de la materia


- [CRUD](#crud)
- [DML (Data Manipulation Languaje)](#data)
- [Create](#create)
- [Insert](#insert)
- [Update](#update)
- [Delete](#delete)
- [Select](#select)
- [DDL (Data Definition Languaje)](#ddl)
- [Drop](#drop)
- [DCL (Data Control Languaje)](#dcl)
- [Grant](#grant)
- [Revoke](#revoke)

## CRUD

CRUD (Create, Read, Update, Delete) es un acrónimo para las maneras en las que se puede operar sobre información almacenada. Es un nemónico para las cuatro funciones del almacenamiento persistente. CRUD usualmente se refiere a operaciones llevadas a cabo en una base de datos o un almácen de datos, pero también pude aplicar a funciones de un nivel superior de una aplicación como soft deletes donde la información no es realmente eliminada, sino es marcada como eliminada a tráves de un estatus.
## DML (Data Manipulation Languaje)

DML es el conjunto de comandos de SQL que permite ingresar, modificar y consultar los datos guardados en la base de datos en las tablas principalmente. DML entonces guarda la informacion en las estructuras creadas con los comandos DDL (Data Definition Languaje). Básicamente consta de los siguientes comandos:
- Insert: Añade registros.  
- Update: Modifica registros.  
- Delete: Elimina registros.  
- Select: Consulta o extrae información de la base de datos.  
## Create 
## Insert

Es el comando utilizado para añadir registros en una tabla o en una vista. En su forma más simple añade un registro a una tabla, pero pueden añadirse más de un registro si se proporcionan los datos necesarios para varios regustros o se anida la salida de una consulta de una tabla como entrada del comando INSERT para añadir varios registros a la vez.

Al momento de realizar la inserción del nuevo registro, la base de datos verifica si los datos cumolen con todas las restricciones de la base de datos y si cumple con la integridad referencial impuesta en la estructura de la base de datos.
**Sintaxis**
{% highlight sql linenos %}
INSERT INTO table_name VALUES(p1, p2, p3)
INSERT INTO table_name(c1, c2) VALUES(p1, p3)
INSERT INTO Alumnos(nombre, edad) VALUES('chinito',23)
{% endhighlight %}

## Update

Update
Es el comando que permite modificar la información en uno o más registros de una tabla. Es capaz de modificar varios registros y varios campos a la vez.

Al igual que con los demas comandos de DML, la base de datos al querer hacer una modificacion a los datos, verifica que la integridad referencial se mantenga y que todas las restricciones establecidas se sigan cumpliendo.
**Sintaxis**
{% highlight sql linenos %}
UPDATE Prueba
   SET nombre = 'Smith'
 WHERE id = 2
 
 UPDATE Prueba
   SET nombre = 'Smith', telefono = 7341285599, edad = 24
 WHERE id = 2
{% endhighlight %}
## Delete
Comando que se utiliza cuando es necesario eliminar permamentemente  uno o mas registros de una tabla. Si bien en ocasiones, no es recomendable eliminar fisicamente los registros (sino lógicamente) el comando DELETE permite hacer la eliminación física (siempre y cuando esto no contradiga las restricciones o integridad de la base de datos).

**Sintaxis**
{% highlight sql linenos %}
DELETE FROM Prueba

DELETE FROM Prueba Where id = 6
{% endhighlight %}
## Select
Es quizá el comando más conocido de SQL ya que se utiliza para extraer o consultarla información contenida en la base datos. Es por mucho, el comando más complejo por las variedades de uso y pòr tanto por las multiples variaciones que puede tener. En un comando SELECT se pueden:

- Consultar una o varias tablas.
- Consultar una o varias vistas.
- Ejecutar funciones creadas por el usuario y de llas interconstruidas en la base de datos.
- Extraer informacion de otras bases de datos.
- Filtrar registros o columnas.
- Agrupar registros.
- Ser entrada para otros comandos.
- Unir diversos comandos SELECT.

La lista puede seguir, pero esos son sólo algunas funcionalidades que se pueden realizar con el comando SELECT.

**Sintaxis**
{% highlight sql linenos %}
SELECT * FROM Prueba

SELECT nombre, edad FROM Prueba
{% endhighlight %}
## DDL (Data Definition Languaje)

Un lenguaje de definición de datos (Data Definition Language, DDL por sus siglas en inglés) es un lenguaje proporcionado por el sistema de gestión de base de datos que permite a los usuarios de la misma llevar a cabo las tareas de definición de las estructuras que almacenarán los datos así como de los procedimientos o funciones que permitan consultarlos.

Las principales funcionalidades de SQL como lenguaje de definición (DDL) son la creación, modificación y borrado de las tablas que componen la base de datos, así como de los índices, vistas, sinónimos, permisos, etc. que pudieran definirse sobre las mismas. Este documento introduce los comandos para el trabajo básico con tablas.

- CREATE TABLE: Crear una tabla  
- SHOW TABLES: mostrar tablas  
- DROP TABLE<nombre de tabla>: Borrar tabla  
- DESCRIBE <nombre de tabla> Mostrar estructura de una tabla  
## Drop
## DCL (Data Control Languaje)
## Grant
## Revoke
