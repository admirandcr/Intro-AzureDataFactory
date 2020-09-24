# Lab 2 – Creando una base de datos Azure SQL Database
En esta sección del laboratorio vamos a crear nuestra base de datos Plataforma como Servicio (PaaS) en el portal de Azure.

## Herramientas utilizadas en este laboratorio
•	[Azure portal](https://portal.azure.com/)

## Creando una Base de Datos Azure SQL Database
En esta serie de pasos se requiere que usted cree una base de datos Plataforma como Servicio y realice las configuraciones necesarias para realizar la conexión. 
Realice los siguientes pasos en su suscripción de Azure. 

1.  Ingrese al Azure Portal.
2.	En el Azure Portal haga click en el menú de la esquina superior izquierda y haga click en All Services.

![Alt Text](url)
 
3.	En las Categorías, busca Databases y has click en SQL Databases
4.	Haz click en + Add.

 
5.	Selecciona la suscripción sobre la cual se va a crear el recurso.
6.	En el Resource Group, selecciona demodatauniRG o el nombre del RG que hayas creado en el Lab1.
7.	Database Name : Ingresa CloudBiker como nombre de la base de datos.
8.	Server: Haz click en la opción Create new.
a.	En la pantalla siguiente llena los datos de nombre de servidor, para efectos del ejemplo utilizaré srvclouddb01.
b.	Ingresa un usuario y password que van a ser los administradores del equipo.
c.	Recuerda que la localización que estamos utilizando es (US) South Central US.
 
9.	Selecciona No, en SQL Elastic Pool. 
10.	Compute and Storage: Haz click en Configure Database.
11.	En las configuraciones, haz click en Looking for basic, standard, ¿premium?
 
12.	Haz click en Standard y configura la base de datos para que tenga 20 DTUs. Haz click en Apply
13.	Blob access tier (default): Hot
14.	Click en Networking. Seleccionar Public endpoint. En Firewall rules, activar Allow Azure services and resources to access this server y Add current client IP address. Hacer click en Additional Settings. 
15.	Activar Sample en Use existing data. Hacer click en Tags y agrega los que correspondan.  Haz click en Review + Create.
16.	Valide lo que está por crearse y haga click en Create. 

Felicidades, haz creado tu primera Base de Datos Azure SQL Database. 


