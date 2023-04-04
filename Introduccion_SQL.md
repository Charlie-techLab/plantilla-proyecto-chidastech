[Página anterior](README.md)  

# SQL

## Definición: 

SQL significa lenguaje de consulta estructurada, por sus siglas en inglés (Structured Query Language). Es decir, SQL es un lenguaje de programación para el almacenamiento de la información y 
su procesamiento en una base de datos relacional. En una base de datos relacional, la información se almacena en forma de tabla, con filas y columnas que representan los atributos de los 
datos y las diferentes relaciones entre los valores de estos datos. Las instrucciones SQL se usan para almacenar, actualizar, eliminar, buscar y recuperar información de la base de datos.
También SQL se usa para mantener y optimizar el rendimiento de una base de datos.

## ¿Por qué es importante SQL?

El lenguaje SQL se usa frecuentemente en todo tipo de aplicaciones ya que se integra bien con los diferentes lenguajes de programación. Por ejemplo, se pueden incrustar consultas SQL con el
lenguaje de programación Java para crear aplicaciones de procesamiento de datos de alto rendimiento con los principales sistemas de bases de datos SQL, como Oracle o MS SQL Server. Además, 
SQL es muy fácil de aprender, ya que en sus instrucciones se utilizan palabras clave comunes en inglés. 

## Historia de SQL

SQL se inventó en la década de 1970 con base en el modelo de datos relacional. Al inicio se conocía como el lenguaje de consultas estructuradas en inglés (SEQUEL). Más tarde, el término se 
abrevió a SQL. Oracle, antes conocido como Relational Software, se convirtió en el primer proveedor en ofrecer un sistema comercial de administración de bases de datos relacionales SQL.

## ¿Cuáles son los componentes de un sistema SQL?

Los sistemas de administración de bases de datos relacionales utilizan un lenguaje de consulta estructurada (SQL) para almacenar y administrar datos. El sistema almacena varias tablas de bases
de datos que se relacionan entre sí. MS SQL Server, MySQL o MS Access son ejemplos de sistemas de administración de bases de datos relacionales. Los siguientes son los componentes de un 
sistema de este tipo. 

## Tabla SQL

Una tabla SQL es el elemento básico de una base de datos relacional. La tabla de la base de datos SQL se compone de filas y columnas. Los ingenieros de bases de datos crean relaciones entre 
varias tablas de bases de datos para optimizar el espacio de almacenamiento de datos.

Por ejemplo, el ingeniero de bases de datos crea una tabla SQL para los productos de una tienda: 

ID de producto

Nombre del producto

ID del color

0001 Colchón Color 1

0002 Almohada Color 2

A continuación, el ingeniero de bases de datos vincula la tabla de productos a la tabla de colores con el ID de color

ID del color

Nombre del color

Color 1 Azul

Color 2 Rojo

## ¿Qué es una clave primaria?

La clave primaria de una tabla es la columna cuyos valores son diferentes en cada fila. Puesto que son diferentes, convierten cada fila en exclusiva. Si no existe ninguna columna de este tipo,
la clave primaria es una composición de dos o más columnas cuyos valores, combinados, son distintos en cada fila. 

Cada tabla del modelo debe tener una clave primaria. Esta norma se deriva automáticamente de la norma que indica que todas las filas deben ser exclusivas. Si es necesario, la clave primaria 
se compone de todas las columnas combinadas. No utilice series de caracteres largas como claves primarias.

Para eficacia, la clave primaria debe ser uno de los siguientes tipos:
Numérico (INT o SMALLINT)
Serie (BIGSERIAL, SERIAL o SERIAL8)
Una serie de caracteres corta (como la que se utiliza para códigos).
Nunca se permiten valores NULL en una columna de clave primaria. Los valores NULL no se pueden comparar; es decir, no se puede decir si son parecidos o diferentes. Por lo tanto, no pueden 
hacer que una fila sea exclusiva, en comparación con las demás. Si una columna permite valores NULL, no puede formar parte de una clave primaria. Al definir una restricción PRIMARY KEY, el 
servidor de bases de datos también crea silenciosamente una restricción NOT NULL en la misma columna, o en el mismo conjunto de columnas que componen la clave primaria.

Algunas entidades tienen claves primarias ya preparadas, como códigos de catálogos o números de identidad, que se definen fuera del modelo. A veces se puede utilizar más de una columna o 
grupo de columnas como clave primaria. Todas las columnas o grupos que están cualificados para ser claves primarias se denominan claves candidatas. Todas las claves candidatas se deben tener
en cuenta porque su propiedad de exclusividad las convierte en previsibles en una operación SELECT.

### Referencias:

1. **https://aws.amazon.com/es/what-is/sql/**
2. **https://www.ibm.com/docs/es/informix-servers/12.10?topic=ssgu8g-12-1-0-com-ibm-ddi-doc-ids-ddi-182-htm**

[Página siguiente](Modelado_BD.md)  
