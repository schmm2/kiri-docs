# Installation

This site will guide you through the process of installing kiri in your environment.

1. Let's start with the prerequisites. You will need:

    - Microsoft Azure Subscription  
    - A Global Administrator Account

2. Click on the button below  

   This will open a new tab and present you with the Azure custom deplyoment page.

   <a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fschmm2%2Fkiri-deploy%2Fmaster%2Fdeployment%2Fazuredeploy.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2Fschmm2%2Fkiri-deploy%2Fmaster%2Fdeployment%2FuiDefinition.json" target="_blank"><img src="https://aka.ms/deploytoazurebutton"/></a>

3. Go ahead an login to the Azure portal

4. Basics  

   First you have to select an existing resource group or create a new one. Give a name to your deyploment.
   This name will determined the URL of the webpage of your kiri deployment. For example if you set the name to **kiritest** the final URL will be <https://kiritest.azurewebsites.net>. Remember this URL. You will need it later to access kiri.

   > This step might change a bit in the future. The idea is to give you more flexibility to name your ressources.
   
   <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy1.jpg?raw=true">

5. Service Principal Worker

   A service principal is needed to authenticate to the managed tenants.  
   The script you will need will be automatically created a new Azure Application Registration with th correct settings.  
   The sitename has automatically been set correctly.

      <img width=400px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy_code.jpg?raw=true">

    1. Open Cloud Shell. You can find it in the top right corner of the portal.

       <img width=300px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy_cloudshell.jpg?raw=true"> 

    2. Copy and paste the code. Grap the created **Application Id** und **Secret** and paste them to the fields in the portal. Click Next.

       <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/azdeploy_output.jpg?raw=true"> 

6. Service Principal App
  
   A service principal is needed so you can control witch user will be able to login to the kiri webapp. Same as before the script is automatically created. Copy and paste the script to Cloudshell. Copy the App ID Output to the form and hit Next.

7. Tags  

   Add Tags if needed

8. Review

   Review your Settings and then click on create. Let the magic happen. Sit back and relax this stept will take some time up to 15min in my experience.

9. The only thing you must do manually (because I do not yet know how to automate this step) is to allow requests to the backend via Frontend Access Token. Sounds complicated... its actually pretty easy to setup. Follow these steps:

   1. Go to the [Azure Portal](https://portal.azure.com)

   2. Go to Application Registration and search **svc-kiriapp**. Select the App.

       <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/permissionimpersonation1.PNG?raw=true">

   3. Select API Permissions and then **Add a permission**

      <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/permissionimpersonation2.PNG?raw=true">

   4. Select organization api, search for **svc-kiriapi**

      <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/permissionimpersonation3.PNG?raw=true">

   5. Select **user_impersonation**

      <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/permissionimpersonation4.PNG?raw=true">

   6. Select **Grant for yourdomain**

      <img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/permissionimpersonation6.PNG?raw=true">

10. You can now Access kiri via the URL in a Webbrowser.

## Installation issues

There have been some installation issues and you don't know how to proceed? First of all "Don't panic". Im pretty sure we can figure this out. If the issue hasen't been documented yet, feel free to reach out to me directly.

### Source Control step failed

I haven't figured out why this is happening but from time to time the installation process fails at the step *sourcecontrol*. If this is the only action that failed, please follow the update guide. Yes you read that one right. If you trigger the update process descriped here [Update](update.md) Azure will redeploy the ressources.