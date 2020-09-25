# Lab 2 – Creando una base de datos Azure SQL Database
En esta sección del laboratorio vamos a crear nuestra base de datos Plataforma como Servicio (PaaS) en el portal de Azure.

## Herramientas utilizadas en este laboratorio
•	[Azure portal](https://portal.azure.com/)

## Creando una Base de Datos Azure SQL Database
En esta serie de pasos se requiere que usted cree una base de datos Plataforma como Servicio y realice las configuraciones necesarias para realizar la conexión. 
Realice los siguientes pasos en su suscripción de Azure. 

1.  Ingrese al Azure Portal.
2.	En el Azure Portal haga click en el menú de la esquina superior izquierda y haga click en **All Services.**

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/CreateResource.png)
 
3.	En las Categorías, busca **Databases** y has click en **SQL Databases.**
4.	Haz click en + Add.

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/SQLDatabase.png)
 
5.	Selecciona la suscripción sobre la cual se va a crear el recurso.
6.	En el **Resource Group**, selecciona **demodatauniRG** o el nombre del RG que hayas creado en el Lab1.
7.	Database Name : Ingresa **CloudBiker** como nombre de la base de datos.
8.	Server: Haz click en la opción **Create new.**
  - En la pantalla siguiente llena los datos de nombre de servidor, para efectos del ejemplo utilizaré **srvclouddb01**.
  - Ingresa un usuario y password que van a ser los administradores del equipo.
  - Recuerda que la localización que estamos utilizando es **(US) South Central US**.

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/NewServer.png)
 
9.	Selecciona **No**, en SQL Elastic Pool. 
10.	Compute and Storage: Haz click en **Configure Database**.
11.	En las configuraciones, haz click en **Looking for basic, standard, ¿premium?**

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/BasicPremium.png)
 
12.	Haz click en **Standard** y configura la base de datos para que tenga 20 DTUs. Haz click en Apply
13.	Click en **Networking**. Seleccionar **Public endpoint**. En Firewall rules, activar **Allow Azure services and resources to access this server** y **Add current client IP address**. Hacer click en **Additional Settings**. 
14.	Activar Sample en **Use existing data**. Hacer click en **Tags** y agrega los que correspondan.  Haz click en **Review + Create**.
15.	Valide lo que está por crearse y haga click en **Create**. 

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/DeploymentComplete.PNG)

Felicidades, haz creado tu primera Base de Datos Azure SQL Database. Ahora veamos como conectarnos a la base de datos que recién acabamos de crear.


## Conectarse a la base de datos

Ejecuta los siguientes pasos para conectarte a la base de datos.

1. En el Azure Portal haga click en el menú de la esquina superior izquierda y haga click en **All Services.**

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/CreateResource.png)
 
3.	En las Categorías, busca **Databases** y has click en **SQL Databases.**

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/AllDatabases.PNG)

4. Hacer click sobre la base de datos **CloudBiker**.
5. En el panel de la izquierda, haga click sobre la opción **Query Editor**.

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/Panel.PNG)

6. Ingrese las credenciales de la base de datos que utilizó al crear la base de datos y haga click en **Ok**

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/QueryEditor.PNG)

   En caso de presentarse un mensaje de error como el siguiente.
   
![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/FirewallError.png)

   Debe de agregar la regla del firewall para agregar la dirección ip siguiendo la liga del mensaje. Agregue la dirección IP que despliega el mensaje.
  
![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/FirewallSettings.PNG)

7. Ahora en la pantalla de consultas ingrese la siguiente sentencia SQL.
 <div class="text-blue mb-2">
   **SELECT * FROM SalesLT.Customer**
 </div>
 Haga click en **Run**
   
![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/CustomerTable.PNG)

   La consulta debe de retornar los registros que contiene la tabla.
   
Es importante recalcar que es posible utilizar el [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15) o bien el [SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15) para realizar las consultas sobre la base de datos. Sin embargo para efectos de este laboratorio las consultas las realizaremos desde el portal de Azure.


