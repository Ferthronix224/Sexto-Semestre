---
layout: post
title: Topicos de Bases de Datos
subtitle: Mejorando el estudio
cover-img: /assets/img/bases.jpg
thumbnail-img: /assets/img/datos.jpg
share-img: /assets/img/bases.jpg
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

Alch con todo

- [CRUD](#crud)
- [DML (Data Manipulation Languaje)](#data)
- [Insert](#insert)
- [Update](#update)
- [Delete](#delete)
- [Select](#select)
- [DDL (Data Definition Languaje)](#ddl)
- [Create](#create)
- [Drop](#drop)
- [DCL (Data Control Languaje)](#dcl)
- [Grant](#grant)
- [Revoke](#revoke)

**Here is some bold text**

## Here is a secondary heading

Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

It can also be centered!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.

# CRUD

CRUD (Create, Read, Update, Delete) es un acrónimo para las maneras en las que se puede operar sobre información almacenada. Es un nemónico para las cuatro funciones del almacenamiento persistente. CRUD usualmente se refiere a operaciones llevadas a cabo en una base de datos o un almácen de datos, pero también pude aplicar a funciones de un nivel superior de una aplicación como soft deletes donde la información no es realmente eliminada, sino es marcada como eliminada a tráves de un estatus.
# DML (Data Manipulation Languaje)
# Insert

{% highlight javascript linenos %}

**Sintaxis**

INSERT INTO table_name VALUES(p1, p2, p3)
INSERT INTO table_name(c1, c2) VALUES(p1, p3)
INSERT INTO Alumnos(nombre, edad) VALUES('chinito',23)
{% endhighlight %}

# Update
# Delete
# Select
# DDL (Data Definition Languaje)
# Create
# Drop
# DCL (Data Control Languaje)
# Grant
# Revoke
