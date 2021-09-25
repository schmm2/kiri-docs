# Update
kiri has a front and backend component.  
The frontend is running inside the Azure App Service *YOURSITENAME*.  
The backend code is running inside the Azure Function App *YOURSITENAME-backend*  

Both code bases can be updated independently. I highly advice you to update both at the same time. The frontend might fail to execute several functions if they are not yet implementen on the backend. 

## Update Frontend

1. Go to the Azure Portal, change the Resource Group kiri was deployed to and select the App Service *YOURSITENAME*.

2. Select **Deployment Center**
<img width=200px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/update_appservice_deploymentcenter.jpg?raw=true">

3. Click on **Sync**. This will check if there is a new realse on Github. If so it will start the download and deploy process.
<img width=500px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/update_appservice_sync.jpg?raw=true">

4. Accept the message. Click on **OK**.

5. Click on **Logs** to check the status of the deployment.
<img width=500px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/update_appservice_log.jpg?raw=true">

6. If the status switches to success the new version has been deployed.

## Update Backend

1. Select the App Service *YOURSITENAME-backend*.

2. Select **Deployment Center**
<img width=200px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/update_functionapp_deploymentcenter.jpg?raw=true">

3. Follow the same steps as in Updating the Frontend. It's basically the same process.