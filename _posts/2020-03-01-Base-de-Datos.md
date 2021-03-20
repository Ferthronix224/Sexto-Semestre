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

**Sintaxis**
{% highlight sql linenos %}
INSERT INTO table_name VALUES(p1, p2, p3)
INSERT INTO table_name(c1, c2) VALUES(p1, p3)
INSERT INTO Alumnos(nombre, edad) VALUES('chinito',23)
{% endhighlight %}

## Update
## Delete
## Select
## DDL (Data Definition Languaje)
## Drop
## DCL (Data Control Languaje)
## Grant
## Revoke
