
## About review questions ##
End of module review questions are for practice only and are not included in your grade for the course.  The final assessment at the end of the course is graded.  

---
##Checkbox##

<<display_name:Review Question 1; partial_credit="EDC"; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which descriptions from the following list describes a feature or characteristic of Azure Firewall?<<

(choose three)

[x] Azure Firewall is a stateful firewall service, with built-in high availability and unrestricted cloud scalability.
[ ] You can create and manage access control lists for databases using Azure Firewall.
[ ] You can prevent DDoS attacks on your network using Azure Firewall.
[x] You can centrally create, enforce, and log application and network connectivity policies across subscriptions and virtual networks.
[x] Azure Firewall is fully integrated with Azure Monitor for logging and analytics.


[explanation]   
The following three features and characteristics are correct:
Azure Firewall is a stateful firewall service, with built-in high availability and unrestricted cloud scalability.
You can centrally create, enforce, and log application and network connectivity policies across subscriptions and virtual networks.
Azure Firewall is fully integrated with Azure Monitor for logging and analytics.

You can create and manage access control lists for databases using Azure Firewall is incorrect.
You can prevent DDoS attacks on your network using Azure Firewall is also incorrect, because you need to use DDoS protection to prevent DDoS attacks on your public-facing resources.
S attacks on your network using Azure Firewall is incorrect, you need to use DDoS Protection to prevent DDoS attacks on your public facing resources.

[explanation]
---
##Multiple choice##

<<display_name:Review Question 2; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>There has been an attack on your public-facing website, and the application's resources have been overwhelmed and exhausted, and are now unavailable to users. What service should you use to prevent this type of attack?<<

(X) DDoS protection
( ) Azure Firewall
( ) Network security group
( ) Application Gateway

[explanation]   
DDoS protection is the correct answer, because it will help prevent DDoS attacks.

Azure Firewall is incorrect. It will helps control access to your network, but may not prevent DDoS attacks.

Network security group is incorrect, because while it will help protect access to your virtual network, it may not prevent a DDoS attack.

Application Gateway is incorrect. While it will help make an application available and help protect it, and it also has a built in web application firewall, it may not prevent DDoS-style attacks.
[explanation]
---
##DropDown##

<<display_name:Review Question 3; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>You want to filter inbound and outbound network traffic to and from Azure resources in your Azure virtual network. Which Azure service should you use?<<

[[      
Azure Firewall
VPN Gateway
(Network security group)
Azure AD
]]

[explanation]    
NSG is the correct answer, because it allows you to filter network traffic to and from Azure resources in an Azure virtual network. It can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port, and protocol.

Azure Firewall will control access in and out of your network but will not control inbound and outbound network traffic within a virtual network.

VPN Gateway is a particular gateway type that allows secure connections from on-premises to Azure over the internet.

Azure AD is Azure's cloud-based identity and access management service that will provide authentication capabilities for identities, but will not control network traffic on a virtual network.

[explanation]
---
##Checkbox##

<<display_name:Review Question 4; partial_credit="EDC"; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Azure AD is capable of providing which of the following functions?<<

(choose all that apply)
 
[X] Authentication
[X] SSO
[X] Application management
[X] B2B
[X] B2B identity services
[X] B2C identity services
[X] Device management

[explanation]
Azure AD is capable of delivering all of the services listed, and many more.

[explanation]
---
##Multiple choice##

<<display_name:Review Question 5; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>You want to store certificates in Azure to centrally manage them for your services. Which Azure service should you use?<<

( ) MSIP
( ) Azure AD
( ) Azure ATP
(X) Azure Key Vault

[explanation]
Azure Key Vault is the correct answer, because it is a centralized cloud service for storing application secrets, referred to as a secret store.

All other answers are incorrect.
MSIP is a cloud-based solution that helps an organization classify, and optionally, protect its documents and emails by applying labels.

Azure AD is Microsoft’s cloud-based identity and access management service that helps employees of an organization sign in and access resources.

Azure ATP is a cloud-based security solution that identifies, detects, and helps organizations investigate advanced threats, compromised identities, and malicious insider actions directed at that organization.

[explanation]
---

##Multiple choice##

<<display_name:Review Question 6; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>True or false: You can download published audit reports and other compliance-related information related to Microsoft’s cloud service from the Service Trust Portal.<<

(X) True 
( ) False


[explanation]
True is the correct answer. You can download published audit reports and other compliance-related information related to Microsoft’s cloud service from the Service Trust Portal.

[explanation]
---

##Multiple choice##

<<display_name:Review Question 7; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which of the following services provides up-to-date status information about the health of Azure services?<<

( ) Compliance Manager
( ) Service Trust Portal
( ) Azure Monitor
(x) Azure Service Health

[explanation]
Azure Service Health is the correct answer, because it provides you with a global view of the health of Azure services. With Azure Status, a component of Azure Service Health, you can get up-to-the-minute information on service availability. 

Compliance Manager enables you to track, assign, and verify your organization's regulatory compliance activities related to Microsoft professional services and Microsoft cloud services.

Service Trust Portal provides information about compliance with standards, laws, and regulations, in addition to hosting the Compliance Manager application.

Azure Monitor collects, analyzes, and provides actions on telemetry from your cloud and on-premises environments.
[explanation]

---

##Multiple choice##

<<display_name:Review Question 8; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>> Where can you obtain details about the personal data Microsoft processes, how Microsoft processes it, and for what purposes?<<

(x) Microsoft Privacy Statement
( ) Compliance Manager
( ) Azure Service Health
( ) Azure Government


[explanation]
Microsoft Privacy Statement is the correct answer.

Compliance Manager enables you to track, assign, and verify your organization's regulatory compliance activities related to Microsoft professional services and Microsoft cloud services.

Azure Service Health will provide you with a global view of the health of your Azure services.

Azure Government is a separate instance of the Microsoft Azure service that addresses the security and compliance needs of United States federal agencies, state and local governments, and their solution providers.

[explanation]


