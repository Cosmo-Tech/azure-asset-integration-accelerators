# azure-asset-integration-accelerators

The Azure Asset Integration Accelerators aim to be an exemple of Data Factory pipelines for Cosmo Tech Asset Simulation Digital Twin. This project demonstrate how to set up a Data Factory pipeline to integrate data into Asset.

You can use this projet to build a data integration pipeline.

## Create Integration Runtimes
The integration runtime objects must be created manually before loading the data factory objects. To do so:
* Go to your Data Factory resource and open it using Azure Data Factory Studio (accessible from the tab overview)
* In the left menu, click on "Manage" (last icon)
* In the menu "Connections", click on "Integration runtimes"
* For each json file in the folder Datafact/integrationRuntime:
  * Create a new resource by clicking the button "+ New"
  * Select Azure, Self-Hosted
  * Select Azure
  * Copy the attribute "Name" of the json file and past it in the field Name of the integration runtime
  * Click on Create

Only the creation of the integration runtime is required, its setting is automatically done with the loading of all the data factory objects. This procedure is detailed in the next section.

## Upload

### Connect to the Git Repository
To upload all the data factory objects, you must connect you data factory with this repository git. To do so, follow the following steps:
* Go to your Data Factory resource and open it using Azure Data Factory Studio (accessible from the tab overview)
* In the left menu, click on "Manage" (last icon)
* In the menu "Source Control", click on "Git configuration"
* Click on the blue button "Configure" in the center of the page to open the configuration menu
* In the configuration menu, select "GitHub"
* DO NOT CHECK the check box "Use GitHub Enterprise Server"
* Enter "Cosmo-Tech" as the GitHub repository owner, then click on "continue"
* Select this repository using the repository name: azure-asset-integration-accelerators
* Select "main" as the collaboration branch
* Enter "/Datafact" as the Root folder
* UNCHECK the check box Import existing resources to repository
* Click on Apply

The data factory is now connected to the git repository

### Load Data Factory Objects
To load all the data factory objects, follow the following steps:
* In the left menu, click on "Author" (second icon)
* Click on the top left menu with the github logo and select the collaboration branch "main"
* All the objects are downloaded in the Studio Editor. To save them, click on "Publish" in the top left menu
