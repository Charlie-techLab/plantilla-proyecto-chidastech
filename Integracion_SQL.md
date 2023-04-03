[Página anterior](Optimizacion_BD.md)

# Integración de SQL con otros lenguajes de programación
Como se dijo anteriormente SQL es un lenguaje de programación que permite manipular datos y bases de datos relacionales. Existen sistemas de gestion como MySQL, PostgreSQL y SQL Server los cuales nos permiten modificar la base de datos sin la necesidad de emplear un programa externo.  

## Conexión a la base de datos desde otros lenguajes de programación  
Cuando se instala SQL en un equipo, se genera un servidor SQL que se almacena en localhost. Hay opciones SQL que no estan instaladas en el equipo sino que se accede a travez de la nube pero la conexión es muy similar.  
Para hacer la conexión con las bases de datos cada lenguaje tiene su propia sintaxis pero en general es como conectarse con un servidor usando la ip, el puerto, el usuario y la contraseña del servidor que se crearon en la instalación. Se recomienda no usar el Usuario Raiz (root) para dichas conexiones, sino que se cree un usuario diferente que tenga los permisos para editar las tablas a las que se van a acceder.  

| Data		      | Valor 				  |
|-----------------|-----------------------|
| IP (servidor)   | "localhost"-127.0.0.1 |
| Puerto	      | 3306 (MySQL)		  |
| Usuario	      | User			      |
| Contraseña      | **********			  |

### Java

```
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.SQLException;

public class SQLDatabaseConnection {
    // Connect to your database.
    // Replace server name, username, and password with your credentials
    public static void main(String[] args) {
        String connectionUrl =
                "jdbc:sqlserver://localhost:3306;"
                        + "database=AdventureWorks;"
                        + "user=yourusername@yourserver;"
                        + "password=yourpassword;"
                        + "encrypt=true;"
                        + "trustServerCertificate=false;"
                        + "loginTimeout=30;";

        try (Connection connection = DriverManager.getConnection(connectionUrl);) {
            // Code here.
        }
        // Handle any errors that may have occurred.
        catch (SQLException e) {
            e.printStackTrace();
        }
    }
}

```

### Python

```
import pyodbc
direccion_servidor = '127.0.0.1'
nombre_bd = 'pruebas_parzibyte'
nombre_usuario = 'usuario'
password = 'hunter2'
try:
    conexion = pyodbc.connect('DRIVER={ODBC Driver 17 for SQL Server};SERVER=' +
                              direccion_servidor+';DATABASE='+nombre_bd+';UID='+nombre_usuario+';PWD=' + password)
    # OK! conexión exitosa
except Exception as e:
    # Atrapar error
    print("Ocurrió un error al conectar a SQL Server: ", e)
```

### JS

```
var connection = new ActiveXObject("ADODB.Connection") ;

var connectionstring="Data Source=<server>;Initial Catalog=<catalog>;User ID=<user>;Password=<password>;Provider=SQLOLEDB";

connection.Open(connectionstring);
var rs = new ActiveXObject("ADODB.Recordset");

rs.Open("SELECT * FROM table", connection);
rs.MoveFirst
while(!rs.eof)
{
   document.write(rs.fields(1));
   rs.movenext;
}

```

[Volver al inicio](README.md)