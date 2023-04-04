[Página anterior](Modelado_BD.md)  

## Instrucciones SQL

Las instrucciones SQL son instrucciones que se usan para los sistemas de administración de bases de datos. El lenguaje SQL provee elementos que permiten la creación de estas instrucciones 
SQL. Los elementos del lenguaje SQL son componentes como identificadores, variables y condiciones de búsqueda para definir una instrucción SQL de manera correcta.

Por ejemplo, la siguiente instrucción SQL utiliza un comando SQL INSERT para almacenar la Marca del colchón A, con un precio de 499 USD, en una tabla llamada Mattress_table, (Tabla_colchón)
con los nombres de columna brand_name (nombre_marca) y cost (costo):

INSERT INTO Mattress_table (brand_name, cost)
VALUES(‘A’,’499’);

En este caso se usa la sentencia SELECT seguido del nombre del campo del cual se desea obtener un dato específico (en este caso el costo) contenido en el nombre de la tabla indicado después
de la palabra reservada FROM. Luego se establece la condición bajo la cual se quiere realizar la consulta; en este caso, cuando el costo sea menor a 500, indicado de la siguiente manera: 
WHERE cost < 500.

SELECT cost 
FROM Mattress_table 
WHERE cost < 500

En este caso se usa la sentencia UPDATE seguido del nombre de la tabla de la cual se desea actualizar un dato específico (en este caso de la tabla Mattress_table). Luego se establece el 
dato nuevo que se quiere poner, lo que se indica con la palabra reservada SET, seguido del nombre del campo a actualizar y asignándole su respectivo nuevo valor. Finalmente, se indica la 
condición bajo la cual se quiere realizar la actualización; en este caso, cuando el campo brand_name sea igual a A, indicado de la siguiente manera:
WHERE brand_name = 'A'.


UPDATE Mattress_table
SET brand_name = 'C'
WHERE brand_name = 'A'


Para borrar una tabla sencillamente se usa la palabra clave DELETE FROM seguido del nombre de la tabla y la condición del campo a eliminar.

DELETE FROM  Mattress_table WHERE brand_name = 'C';

### Referencias:

https://aws.amazon.com/es/what-is/sql/

[Página siguiente](Optimizacion_BD.md)