# Architecture

## Azure

On the following diagram are all components which will be deployed to Azure. Those components are all needed for kiri to function. 

<img width=700px src="https://github.com/schmm2/kiri-docs/raw/main/docs/img/kiri-architecture.jpg?raw=true">  

## Application Registrations

During the setup, 3 App Registrations will be created.

- svc-kiriapp: Manages the login to kiri

- svc-kiriapi: Grants Access to backend API

- svc-kiriworker: App which is used to interact with tenants for example query configs

## Code

The kiri project codebase is separated into several repositories.  
The Git repositories are stored on Github.

- Frontend Application [kiri-app](https://github.com/schmm2/kiri-app)
- Backend Function App [kiri-backend](https://github.com/schmm2/kiri-backend)
- Arm Template for deployment [kiri-deploy](https://github.com/schmm2/kiri-deploy)
- Docs page [kiri-docs](https://github.com/schmm2/kiri-docs)
- Kiri Project Webpage [kiri-web](https://github.com/schmm2/kiri-web)

<!-- end of the list -->

All code is open-source. I am very happy for reported issues and pull requests.
