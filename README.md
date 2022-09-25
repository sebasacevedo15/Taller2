# Taller2
Taller 2. Daniela Rubio, Steven Orozco y Sebastian Acevedo

Subproceso de ETL complementado con su respectiva query de MongoDB y carga a BigQuery 
Se puede detallar todo el proceso que se describe a continuación en el código de Python.
 -Se realiza la conexión a través de Python a MongoDB Atlas
-Se extrae del campo ítems los respectivos precios de cada item comprado por transacción y adicional se operan para obtener el valor total por cada compra realizada.
-Se realizan filtros por rango de fechas que sean importantes para el negocio.
- Es necesario modificar el tipo de dato que se genera en el Json para que en el momento que se tenga que agrupar se puedan realizar operaciones con estos datos.
- Se crea dataset para alojar tablas javeriana-dataprep.GrupoDanielaStevenSebastian
- Las tablas creadas en BigQuery son Taller_tabla1, Taller_tabla2, Taller_tabla3.
Descripción de la colección de datos escogida.
Se eligió la base de datos “sample_supplies.sales”, donde tenemos una cantidad y transacciones y asociada a cada una de estas esta la fecha y hora de la transacción, satisfacción de los clientes en una escala de 1-5, la locación de la tienda, los ítems y precios que fueron comprados en cada transacción, el canal por el cual se realiza la compra y si se hizo uso o no de un cupón al momento de la compra.
 b. Definición de las 3 preguntas de negocio que se quieren responder. 
En aras de ayudar a esta cadena de supermercados a partir de la información disponible de las transacciones (descrita previamente) y lograr mejorar su desempeño en general (facturación, recurrencia entre otros) por cada una de las locaciones en donde están presentes se plantearon las siguientes preguntas:
1.	¿Cómo es el comportamiento actual por cantidad de Transacciones, satisfacción y por edad promedio de los clientes por cada una de las tiendas en el año 2017? Para poder tener una aproximación del estado actual de las tiendas.

![image](https://user-images.githubusercontent.com/109991685/192169294-73024d12-f711-46ab-988c-4b655a93ac8b.png)
