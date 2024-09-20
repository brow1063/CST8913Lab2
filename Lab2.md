Instructions
Scenario: The following application consists of a Web Server written in Flask. A UI front end written in React. A database layer consisting of Postgres.

Describe how this application can be deployed in the cloud using IaaS infrastructure
Describe how this application can be deployed in the cloud using PaaS infrastructure.
For each case, draw a diagram that represents the target architecture and describe each of the chosen cloud components.

Iaas:
For the lift and shift to a Iaas the solution will be the use of 3 VMs within a VNet. The first VM will host the Flask Web Server which will handle external requests. The second VM will host the React Frontend which processes the requests and handle retrieval of data. The third VM will host the Postgres Database which will process the reads and writes as needed. Finally the VMs will run on a VNet that provides security and communications between the VMs.

Paas:
For the lift and shift to a Paas the solutions will utilize Azure functionality including App Services, Static Web Apps and Azure database for PostgreSQL. The Flask backend will be hosted on Azure App Services which will be the first stop of an external request and it will process what is required (database or response). The React Frontend will be hosted on Azure Static Web Apps which will allow users to interact with the webpage. Finally the Database will be hosted on the Azure database for PostgreSQL this will interact this the information stored securely. Through the use of Azure services communication flows both ways through the different services as needed.

![IaaS PaaS Diagram](https://raw.githubusercontent.com/brow1063/CST8913Lab2/main/IaasPaas.png)
