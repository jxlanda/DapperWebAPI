# .NET 5 WEB API con DAPPER

## ¿Qué es Dapper?

Podríamos definir Dapper como un Micro ORM (o ORM ligero) que se encarga de manejar el acceso a datos, la ejecución de consultas y de operaciones de inserción, actualización y borrado de datos.

Entrando más en detalle podemos ver que Dapper es una clase estática llamada SqlMapper en la que podemos encontrar un conjunto de métodos extensores sobre la interfaz IDbConnection que nos van a permitir la ejecución de consultas genéricas (<T>) y las operaciones de modificación de datos de una forma sencilla. Hacer una extensión de la interfaz IDbConnection va a permitirnos que cualquier clase de conexión a base de datos que implemente dicha interfaz,por ejemplo: SqlConnection (entre otros), disponga de manera automática de todos estos métodos extensores.

Algunas de las cosas que me gustaría destacar dentro de Dapper son:
* Ejecución de consultas parametrizadas: Uno de los principales problemas que podemos encontrarnos al hacer uso de bases de datos dentro de nuestras aplicaciones, es la inyección de SQL que a grosso modo es un problema que permite la ejecución de código no deseado en nuestras consultas a través de la incorrecta utilización de las comillas simples y la no utilización de parámetros en las consultas.
* El automapeo de las consultas a los tipos en las consultas genéricas.
* La ejecución de varias consultas en un único viaje.
