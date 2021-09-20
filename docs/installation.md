# Installation

This site will guide you through the process of installing kiri in your environment.

1. Let's start with the prerequisites. You will need:
    - Microsoft Azure Subscription 
    - A Global Administrator Account

2. Go ahead an login to the [Azure portal](https://portal.azure.com)

3. Click on the button below\
This will open a new tab and present you with the Azure custom deplyoment page.\
\
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fschmm2%2Fkiri-deploy%2Fmaster%2Fdeployment%2Fazuredeploy.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2Fschmm2%2Fkiri-deploy%2Fmaster%2Fdeployment%2FuiDefinition.json" target="_blank"><img src="https://aka.ms/deploytoazurebutton"/></a>

4. First you have to select an existing resource group or create a new one. Give a name to your deyploment.
This name will determined the URL of the webpage of your kiri deployment. For exaple you you set the name to kiritest the final URL will be https://kiritest.azurewebsites.net.
<img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy1.PNG?raw=true">  

5. Test