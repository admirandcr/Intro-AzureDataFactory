# Lab 1 – Creación del Data Lake
En esta sección del laboratorio vamos a crear nuestro Data Lake en el portal de Azure.

## Herramientas utilizadas en este laboratorio
•	[Azure portal](https://portal.azure.com/signin/index)

## Creando un Data Lake
En esta serie de pasos se requiere que usted cree un nuevo Data Lake empresarial para permita la carga de archivos desde distintas fuentes (Relaciones, No Relaciones, No estructuradas, etc).
Realice los siguientes pasos en su suscripción de Azure. 
1.	Ingrese al Azure Portal.
2.	En el Azure Portal haga click en el menú de la esquina superior izquierda y haga click en **All Services.**

![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/CreateResource.png)
 
3.	En las Categorías, busca Storage y has click en **Storage Accounts.**
4.	Haz click en + Add.

 ![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/2StorageAccount.png)
 
5.	Selecciona la suscripción sobre la cual se va a crear el recurso.
 -	En el Resource Group, crea uno nuevo e ingresa **demodatauniRG**. Puedes utilizar el nombre que gustes mientras cumpla con las reglas de nomenclatura.
 - Storage account name : Ingresa un nombre descriptivo para el nombre de la cuenta.
 - Location: La ubicación más cercana del datacenter en donde te encuentres. Para este ejemplo podemos usar **(US) Central US.**
 - Performance: Selecciona **Standard. **
 - Account Type: **Storage V2.**
 - Replication: **Locally-Redundant Storage (LRS)**
 - Blob access tier (default): **Hot**
 - Click en **Networking.**
 - Los valores se quedan en default. Haz click en **Data protection.**
 - Los valores se quedan en default. Haz click en **Advanced.**
 - En la opción **Data Lake Storage Gen2**, activar **Hierarchical namespace.** Haz click en **Tags.**
 - Incluir un tag. Ejemplo: Name – Analytics, Value – Produccion. Haz click en **Review + Create.**
 - Valide lo que está por crearse y haga click en **Create.**
 
  ![Alt Text](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/img/3Review.png)
  
6.	Listo, haz creado tu primer Data Lake. 

Ahora continuemos a nuestro siguiente laboratorio.

[Siguiente >](https://github.com/admirandcr/Intro-AzureDataFactory/blob/master/Docs/Lab2-CreateSQLDatabase.md)
