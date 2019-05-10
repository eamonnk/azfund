
## About review questions ##
End-of-module review questions are for practice only and are not included in your grade for the course.  The final assessment at the end of the course is graded.  

---
##Checkbox##

<<display_name:Review Question 1; partial_credit="EDC"; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>What terms from the below list are valid core architectural components of Microsoft Azure?<<

(choose four)

[x] Region  
[x] Availability zone
[ ] Server group
[x] Resource group
[x] Availability set


[explanation]   
Region, availability zone, resource group, and availability set are the correct answers, as they are all core architectural components of Azure. 


Server Groups are not a core architectural component of Microsoft Azure.
[explanation]
---
##Multiple Choice##

<<display_name:Review Question 2; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Every resource created in Azure must exist in one and only one what?<<

( ) Availability set
( ) Availability zone
(x) Resource group
( ) Azure Resource Manager

[explanation]   
Resource group is the correct answer. Each resource must exist in one, and only one, resource group.

All other answers are incorrect, as a resource does not need to exist in an availability set or an availability zone, and Azure Resource Manager is a management layer that creates resources, but a resource cannot exist in this layer. 
[explanation]
---
##DropDown##

<<display_name:Review Question 3; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>As a best practice, all resources that are part of an application and share the same life cycle exist in the same what?<<

[[      
Geography
(Resource group)
Region  
Availability set     
]]

[explanation]    
Resource group is the correct answer. Resources that are part of an application and share its life cycle should be placed in the same resource group for ease of management. 

It is not a recommended best practice for resources to be placed in the same geography, region, or availability set.
[explanation]
---
##Checkbox##

<<display_name:Review Question 4; partial_credit="EDC"; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>You want to deploy an application in a container, and may need to run it at scale on some occasions. You want to deploy the containers directly to Azure without having to first deploy virtual machines. Which services are available for you to use to deploy containers directly to Azure?<<

(choose two)
 
[X] Azure Kubernetes Service (AKS)
[ ] Azure Functions
[ ] VMs
[X] Azure Container Instances

[explanation]
AKS and Azure Container Instances are the correct answers. Azure Container Instances allows you to deploy containers directly to Azure; and Azure Kubernetes Service is a container orchestrator, which allows you run containers at scale without having to manage underlying VMs.

Azure Functions is not the correct answer as Functions is involved in serverless computing and does not run containers directly. 

VMs is not the correct answer either, because although you could run containers in an IaaS virtual machine, you would have to manage the virtual machine to do so. 
[explanation]
---
##Multiple Choice##

<<display_name:Review Question 5; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>You need to deploy a legacy application in Azure that has some customizations that are needed to ensure it runs successfully. The application will run on a Windows VM. Which Azure service from the below list would you recommend to run the virtual machine in?<<

( ) Azure App Service
( ) Azure Event Grid
(X) Azure Virtual Machines
( ) Azure Container Instances

[explanation]
Azure Virtual Machines is the correct answer, because it is an IaaS service and as such you are responsible for configuring and managing the virtual machine on which the application will run. This enables you to customize it as needed in this case.

Azure App Service is a PaaS service, and as such you will not be able to customize the underlying virtual machine in which the application runs. 

Azure Event Grid is a messaging service in Azure that triggers other events. It allows you to connect serverless logic to events coming from multiple Azure services, and it connects to events from external sources, all as part of a serverless computing model. However, it does not run virtual machines.

Azure Container Instances will not run virtual machines; it will only run containers, and is a PaaS service.


[explanation]
---

##Multiple Choice##

<<display_name:Review Question 6; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>True or false: Resource Manager templates are JSON files.<<

(X) True 
( ) False


[explanation]
Resource Manager templates are JSON files that define the resources you need to deploy for your solution. You can then use the template to easily re-create multiple versions of your infrastructure, such as staging and production.

[explanation]
---

##Multiple choice##

<<display_name:Review Question 7; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which of the following services are part of Core Networking services in Azure?<<

( ) Azure App Services
( ) Azure Blob Storage
( ) Azure Cosmos DB
(x) Azure VPN Gateway

[explanation]
Azure VPN Gateway is the correct answer, because it allows you to connect securely from your on-premises environment to Azure. It is also referred to as a Virtual Network Gateway.

Azure App Services is a PaaS service for running different types of apps, such as web apps, mobile apps, and others.

Azure Blob Storage is part of storage services, and Azure Cosmos DB is part of data services.
[explanation]

---

##Multiple choice##

<<display_name:Review Question 8; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>> Which of the following services are part of Core IoT services in Azure?<<

(x) IoT Central
( ) Application Gateway
( ) Azure DevOps
( ) Azure PowerShell


[explanation]
IoT Central is the correct answer, because it is an SaaS for IoT that allows you to connect, monitor, and manage your IoT assets at scale.

Application Gateway is a gateway service to allow your application connect internally or externally and is part of the Networking suite of services.

Azure DevOps is part of the DevOps suite of services and allows you build continuous integration and delivery pipelines.

Azure PowerShell is a scripting language that allows you manage and configure Azure.

[explanation]

---

##Multiple choice##

<<display_name:Review Question 9; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>> Which of the following services are part of the Artificial Intelligence service in Azure?<<

( ) HDInsight
(x) Azure Machine Learning service
( ) Azure DevTest Labs
( ) Azure Advisor

[explanation]

Azure Machine Learning service is the correct answer. Machine Learning service provides a cloud-based environment that you can use to develop, train, test, deploy, manage, and track machine learning models. 

HDInsight is a fully managed, open-source analytics service for enterprises, and is part of the big data and analytics category of services.

Azure DevTest Labs is a service that helps developers and testers quickly create environments in Azure while minimizing waste and controlling cost. It is part of the DevOps suite of services.

Azure Advisor is a free service built into Azure that provides recommendations on high availability, security, performance, and cost. It is part of the management suite of tools and services.

[explanation]
