[Página anterior](README.md)
# SQL

## Definición: 

SQL significa lenguaje de consulta estructurada, por sus siglas en inglés (Structured Query Language). Es decir, SQL es un lenguaje de programación para el almacenamiento de la información y 
su procesamiento en una base de datos relacional. En una base de datos relacional, la información se almacena en forma de tabla, con filas y columnas que representan los atributos de los 
datos y las diferentes relaciones entre los valores de estos datos. Las instrucciones SQL se usan para almacenar, actualizar, eliminar, buscar y recuperar información de la base de datos.
También SQL se usa para mantener y optimizar el rendimiento de una base de datos.

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





