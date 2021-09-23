# Installation

This site will guide you through the process of installing kiri in your environment.

1. Let's start with the prerequisites. You will need:
    - Microsoft Azure Subscription 
    - A Global Administrator Account

2. Click on the button below\
This will open a new tab and present you with the Azure custom deplyoment page.\
\
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fschmm2%2Fkiri-deploy%2Fmaster%2Fdeployment%2Fazuredeploy.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2Fschmm2%2Fkiri-deploy%2Fmaster%2Fdeployment%2FuiDefinition.json" target="_blank"><img src="https://aka.ms/deploytoazurebutton"/></a>

3. Go ahead an login to the Azure portal

4. Basics\
First you have to select an existing resource group or create a new one. Give a name to your deyploment.
This name will determined the URL of the webpage of your kiri deployment. For exaple you you set the name to kiritest the final URL will be <https://kiritest.azurewebsites.net>.
<img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy1.jpg?raw=true">  

5. Service Principal Worker\
A service principal is needed to authenticate to the managed tenants.\
The script you will need will be automatically created a new Azure Application Registration with th correct settings.\
The sitename has automatically been set correctly.
<img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy_code.jpg?raw=true">  

    1. Open Cloud Shell. You can find it in the top right corner of the portal.
    <img width=200px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy_cloudshell.jpg?raw=true"> 

    2. Copy and paste the code. Grap the created App Id und Secret and paste them to the fields in the portal. Click Next.
    <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy_output.jpg?raw=true"> 

6. Test