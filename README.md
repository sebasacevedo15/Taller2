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

![image](https://user-images.githubusercontent.com/109991685/192169320-6409b6e8-e7a6-484d-939a-52c8b8a4fed2.png)

 

Se encuentra que la tienda que más realizó ventas fue Denver con 1549 Transacciones alrededor del 30,98% del total. La tienda que cuenta con menos transacciones es San Diego con 346 equivalente al 6,92%

 ![image](https://user-images.githubusercontent.com/109991685/192169328-d6aa2293-d7a9-4da8-8a12-e5c41d619906.png)

Al analizar el promedio de edad de las personas que realizan compras en las diferentes tiendas no se encuentra una diferencia significativa entre ellas. Para las diferentes tiendas el promedio de edad de sus clientes esta entre 43 y 45 años. Un comportamiento similar se encuentra en el promedio de calificación de satisfacción con un promedio de 3,7 de 5. 

2. Ahora que hemos visto que en términos de satisfacción las tiendas se encuentran bien, debido a que tienen políticas homogéneas de servicios al cliente que se cumplen a cabalidad nos interesa saber un poco más acerca de los clientes por lo cual queremos responder ¿Cómo es el comportamiento por grupos etarios (se decide hacer la distribución entre joven menores a 30 y Adultos mayores a 30) en cuanto a ticket promedio? ¿existe una diferencia marcada?, de esta manera se puede plantear estrategias focalizadas en cada uno de los grupos examinados.
 ![image](https://user-images.githubusercontent.com/109991685/192169332-56fbfa9e-8a1b-4ccd-bc91-9a0b5a4f369e.png)

Al graficar en el plano y por medio de barras el promedio de transacciones para los dos grupos etarios definidos se encuentra que tienen valor cercano, pero tienen comportamientos interesantes en Denver y New York donde en promedio las personas jóvenes tienen un promedio de transacción más alto que los adultos. En las demás tiendas el promedio de transacción de los adultos es mayor. 
 ![image](https://user-images.githubusercontent.com/109991685/192169335-aa724712-0379-4c3d-ade5-9015ca5ef951.png)

3. Con el fin de segmentar el comportamiento de los clientes, se necesita saber cómo fue la dinámica de sus compras por cada uno de los géneros, que canal usan para las compras y debido a que se están posicionando en el mercado la empresa ha optado por dar cupones y necesita saber en relación con el total de las compras que tantos cupones se han usado.
![image](https://user-images.githubusercontent.com/109991685/192169338-f7bab022-d35c-4424-b23c-cf2dcc7e9862.png)

 
Al observar la cantidad de transacciones donde se usaron cupones se encuentra que la transaccionalidad no se ve apalancada por el uso de cupones ya que en general no superan el 15% de las transacciones registradas en las tiendas. 
 ![image](https://user-images.githubusercontent.com/109991685/192169341-0908b453-7f22-42cd-b789-0edcb7ea5a1f.png)

Al analizar la distribución de transacciones por género se encuentra que no hay razón para realizar una segmentación por genero ya que no se encuentra una diferencia importante entre la cantidad de transacciones realizadas por mujeres o por hombres.
 ![image](https://user-images.githubusercontent.com/109991685/192169345-0b3b0654-0ca3-4dc8-9c05-5c9900149bd6.png)

 
Cuando se analiza la participación de compras por los diferentes canales se observa que las transacciones en tienda son las que predominan, aunque las transacciones Online también tienen una participación importante en el total de ventas por lo cual sería importante explorar estrategias que incrementen la cantidad de transacciones Online. 
Nota: Para la creación de gráficos nos apoyamos en la herramienta Tableau y las incorporamos en cada una de las preguntas.
