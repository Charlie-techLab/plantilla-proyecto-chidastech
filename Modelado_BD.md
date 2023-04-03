[Página anterior](Introduccion_SQL.md)

# Modelado de bases de datos
Un modelo, una representación gráfica, de bases de datos muestra la estructura lógica de la base, las relaciones entre tablas y las limitaciones que determinan cómo se almacenan los datos y cómo se accede a ellos.[1](#Referencia1)  

## Tipos de modelados de bases de datos

- [Modelo jerárquico](#mod1)
- [Modelo relacional](#mod2)
- [Modelo de red](#mod3)
- [Modelo orientado a objetos](#mod4)
- [Modelo entidad-relación](#mod5)
- [Modelo de documentos](#mod6)
- [Modelo entidad-atributo-valor](#mod7)

### Modelo jerárquico<a name="mod1"></a>  

Organiza los datos en una estructura de árbol, en la que cada registro tiene un único elemento raíz. Los registros del mínimo nivel se clasifican en un orden específico el cual se usa para almacenar la base de datos. Este modelo ayuda a describir muchas relaciones del mundo real.  

<img src="/img/hierarchical-model.png" width="500" >

### Modelo relacional<a name="mod2"></a>  

Ordena los datos en tablas, relaciones, cada una de las cuales se compone de columnas y filas. Cada columna enumera un atributo de la entidad en cuestión. Se hace uso de un atributo o varios para las llamadas llaves primarias y foráneas para hacer referencia en otras tablas. Cada fila, tupla, incluye datos sobre una instancia específica de la entidad en cuestión. Las relaciones pueden ser uno a uno, uno a muchos y muchos a muchos.  

<img src="/img/relational-model.png" width="500" >  

### Modelo de red<a name="mod3"></a>  
Se basa en el modelo jerárquico, cuya diferencia es que permite relaciones de muchos a muchos, que permite conjuntos con relaciones más complejas.  

<img src="/img/network-model.png" width="500" >  

### Modelo orientado a objetos<a name="mod4"></a>  
Con este modelo se define una base de datos como si fueran clases y objetos. Este modelo se utiliza principalmente en bases de datos no relacionales ya que permite la incorportación de datos multimedia y de hipertexto.   

<img src="/img/object-oriented-model.png" width="500" >  

### Modelo entidad-relación<a name="mod5"></a>  
Este tipo de modelo es el que se emplea principalmente en base de datos SQL. Se le conoce como entidad a las personas, lugares, cosas, etc. Se representa las relaciones y la cardinalidad.  

<img src="/img/er-diagram.png" width="500" >  

### Modelo de documentos<a name="mod6"></a>  
Es un modelo empleado para bases de datos no SQL el cual se diseña para almacenar y administrar documentos o datos semiestructurados.  

<img src="https://www.diegocalvo.es/wp-content/uploads/2017/11/base_de_datos_orientada_a_documentos.png" width="500" >  

### Modelo entidad-atributo-valor<a name="mod7"></a>  
Similar al modelo entidad-relación con la diferencia en que agregan los atributos de las entidades y los posibles valores.  

## Referencias:
[1] <a name="Referencia1"></a> https://www.lucidchart.com/pages/es/que-es-un-modelo-de-base-de-datos 

[Página siguiente](Consultas_SQL.md)