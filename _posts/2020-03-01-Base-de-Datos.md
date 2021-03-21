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
- [DML (Data Manipulation Languaje)](#dml-data-manipulation-languaje)
- [Create](#create)
- [Insert](#insert)
- [Update](#update)
- [Delete](#delete)
- [Select](#select)
- [DDL (Data Definition Languaje)](#ddl-data-definition-languaje)
- [Drop](#drop)
- [DCL (Data Control Languaje)](#dcl-data-control-languaje)
- [Grant](#grant)
- [Revoke](#revoke)
- [Procedimientos Almacenados](#procedimientos-almacenados)
- [Tareas](#tareas)

## CRUD

CRUD (Create, Read, Update, Delete) es un acrónimo para las maneras en las que se puede operar sobre información almacenada. Es un nemónico para las cuatro funciones del almacenamiento persistente. CRUD usualmente se refiere a operaciones llevadas a cabo en una base de datos o un almácen de datos, pero también pude aplicar a funciones de un nivel superior de una aplicación como soft deletes donde la información no es realmente eliminada, sino es marcada como eliminada a tráves de un estatus.
## DML (Data Manipulation Languaje)

DML es el conjunto de comandos de SQL que permite ingresar, modificar y consultar los datos guardados en la base de datos en las tablas principalmente. DML entonces guarda la informacion en las estructuras creadas con los comandos DDL (Data Definition Languaje). Básicamente consta de los siguientes comandos:
- Insert: Añade registros.  
- Update: Modifica registros.  
- Delete: Elimina registros.  
- Select: Consulta o extrae información de la base de datos.  


## Create 

La sentencia CREATE DATABASE se utiliza para crear bases de datos.
{% highlight sql linenos %}
CREATE DATABASE Ferthronix
{% endhighlight %}

La sentencia CREATE TABLE se utiliza para crear una tabla en una base de datos existente.
{% highlight sql linenos %}
CREATE TABLE numerikis
(
id int,
edad int,
numeros int,
)
{% endhighlight %}
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
   
La sentencia DROP se utiliza para borrar definitivamente un índice, tabla o base de datos.
**Sintaxis**
{% highlight sql linenos %}
DROP TABLE Prueba

DROP DATABASE Ferthronix
{% endhighlight %}
## DCL (Data Control Languaje)

No cualquiera puede acceder a la base de datos, y de los usuarios que pueden ver la base de datos, no todos deberían tener los mismos privilegios para ver o modificar la información. El Lenguaje de COntrol de Datos o DCL aglomera a los comandos que se utilizan en las bases de datos relacionales para otorgar o quitar permisos a los usuarios.

Los permisos que se pueden otorgar a los usuarios son de dos tipos principalmente:

- Permisos de sistema: Incluyen permisos para crear sesiones, crear estructuras (comandos DDL) o incluso ejecutar código contenido dentro de la base de datos.
- Permisos sobre objetos: Son aquellos permisos que dejan a los usuarios ver información  p incluso modificarla.

Las buenas prácticas de seguridad de bases de datos implementadas con ayuda de los administradores de bases de datos o DBAs deben incluir la definición de diversos usuarios, que tengan diversos privilegios, de tal manera que cada usuario solo vea los datos qque requiere y nunca se exponga la información  a usuarios que no sean los permitidos.

Para implementar los permisos o privilegios en la base de datos se utilizan dos comandos, **GRANT** y **REVOKE**. 
## Grant

Es el comando de DCL para otorgar o dar permisos a un usuario de algo en particular (permisos de sistema o sobre objetos). Obviamente, para dar permisos, el usuario que los otorga debe tener, a su vez, permisos para dar permisos. Es por ello que estas actividades están restringidas casi siempre a los DBAs en las organizaciones.
## Revoke

Es el complemento del comando GRANT, ya que el comando REVOKE elimina o quita privilegios al usuario de que se trate en el comando.

Al igual que el comando anterior, para poder quitar permisos a un usuario, el usuario que ejecute REVOKE deberá tener privilegios para hacerlo.

## Procedimientos Almacenados

**Sintaxis de un procedimiento almacenado de Add**
{% highlight sql linenos %}
SET ANSI_NULLS ON
SET QUOTED_IDENTIFIER ON
GO
CREATE PROCEDURE stp_clientes_add
(
@nombre NVARCHAR(50),
@razonSocial NVARCHAR(100),
@telefono NVARCHAR(20),
@descuento DECIMAL(6,2)
)
AS
BEGIN

INSERT INTO [dbo].[Clientes]
           ([nombre]
           ,[razonSocial]
           ,[telefono]
           ,[descuento]
           ,[activo])
     VALUES
           (@nombre,
		    @razonSocial,
		    @telefono,
		    @descuento,
		    1)

END
{% endhighlight %}

**Sintaxis de un procedimiento almacenado de Update**
{% highlight sql linenos %}
SET ANSI_NULLS ON
SET QUOTED_IDENTIFIER ON
GO
CREATE PROCEDURE stp_clientes_update
(
@idCliente INT,
@nombre NVARCHAR(50),
@razonSocial NVARCHAR(100),
@telefono NVARCHAR(20),
@descuento DECIMAL(2,0)
)
AS
BEGIN

UPDATE [dbo].[Clientes]
   SET [nombre] = @nombre
      ,[razonSocial] = @razonSocial
      ,[telefono] = @telefono
      ,[descuento] = @descuento
 WHERE idCliente = @idCliente

END
{% endhighlight %}

**Sintaxis de un procedimiento almacenado de GetById**
{% highlight sql linenos %}
SET ANSI_NULLS ON
SET QUOTED_IDENTIFIER ON
GO
CREATE PROCEDURE stp_clientes_getbyid
(
@idCliente INT
)
AS
BEGIN

SELECT [idCliente]
      ,[nombre]
      ,[razonSocial]
      ,[telefono]
      ,[descuento]
      ,[activo]
  FROM [dbo].[Clientes]
  WHERE idCliente = @idCliente

END
{% endhighlight %}

**Sintaxis de un procedimiento almacenado de GetAll**
{% highlight sql linenos %}
SET ANSI_NULLS ON
SET QUOTED_IDENTIFIER ON
GO
CREATE PROCEDURE stp_clientes_getall
AS
BEGIN

SELECT [idCliente]
      ,[nombre]
      ,[razonSocial]
      ,[telefono]
      ,[descuento]
      ,[activo]
  FROM [dbo].[Clientes]

END
{% endhighlight %}

**Sintaxis de un procedimiento almacenado de Delete**
{% highlight sql linenos %}
SET ANSI_NULLS ON
SET QUOTED_IDENTIFIER ON
GO
CREATE PROCEDURE stp_clientes_delete
(
@idCliente INT
)
AS
BEGIN

UPDATE [dbo].[Clientes]
   SET activo = 0
 WHERE idCliente = @idCliente

END
{% endhighlight %}

## Tareas

{% highlight sql linenos %}
SELECT * FROM Products WHERE UnitsInStock < 30 AND Discontinued = 0 AND ProductName LIKE '%c%'
{% endhighlight %}

{% highlight sql linenos %}
SELECT DISTINCT ShipCity FROM Orders
{% endhighlight %}

{% highlight sql linenos %}
--Actividad 3 Obtener el listado de clientes (nombre), a los cuales se les enviaron productos con descuento 

SELECT DISTINCT CompanyName FROM Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID
INNER JOIN [Order Details] ON Orders.OrderID = [Order Details].OrderID WHERE Discount > 0

--Actividad 4 Obtener el listado de clientes (nombre), a los cuales se les enviaron productos provenientes de canada y que la paqueteria
-- sea "Federal Shipping" 

SELECT DISTINCT Customers.CompanyName FROM Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID INNER JOIN Shippers 
ON Orders.ShipVia = Shippers.ShipperID WHERE ShipCountry = 'Canada' AND ShipVia = 3
{% endhighlight %}

{% highlight sql linenos %}
--ACTIVIDAD CURSORES mostrar en pantalla, el listado de nombres de clientes 
--involucrados en ordenes hechas a Le France en la ventana de Mensajes NO EN RESULTADOS 

DECLARE @cliente AS NVARCHAR(50)
DECLARE @miCursorsito AS CURSOR
SET @miCursorsito = CURSOR FOR
					SELECT DISTINCT ContactName FROM Customers INNER JOIN Orders
					ON Customers.CustomerID = Orders.CustomerID WHERE ShipCountry = 'France'
OPEN @miCursorsito
FETCH NEXT FROM @miCursorsito INTO @cliente
WHILE @@FETCH_STATUS = 0
BEGIN

	PRINT @cliente

	FETCH NEXT FROM @miCursorsito INTO @cliente

END

--SELECT DISTINCT ContactName FROM Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID WHERE ShipCountry = 'France'

--SELECT * FROM Employees
{% endhighlight %}
