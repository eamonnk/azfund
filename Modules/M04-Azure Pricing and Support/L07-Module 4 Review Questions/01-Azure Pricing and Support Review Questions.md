
## About review questions ##
End-of-module review questions are for practice only and don't count against your course grade. However, the final assessment at the end of the course is graded. 

---
##Multiple choice##

<<display_name:Review Question 1; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which of the following defines an Azure subscription correctly?<<


( ) Using Azure does not require a subscription
( ) All Azure subscriptions are always free
(x) An Azure subscription is a logical unit of Azure services that is linked to an Azure account
( ) An account cannot have more than one subscription

[explanation]
It's true that an Azure subscription is a logical unit of Azure services that is linked to an Azure account. All other answers are incorrect.

Using Azure requires an Azure subscription. Azure offer free and paid subscription options to suit different customer needs and requirements, and an account can have one or more subscriptions, with different billing models and access-management policies applied to each .  A subscription provides authenticated and authorized access to Azure products and services, and allows you to provision resources.
[explanation]

---
##Multiple choice##

<<display_name:Review Question 2; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>True or false: Azure Management Groups are containers for managing access, policies, and compliance across multiple Azure subscriptions?<<

(x) True
( ) False

[explanation]
True, Azure Management Groups are containers for managing access, policies, and compliance across multiple Azure subscriptions.

Management groups facilitate the hierarchical ordering of Azure resources into collections, at a level of scope above subscriptions. Distinct governance conditions can be applied to each management group, with Azure Policy and Azure RBACs, to manage Azure subscriptions effectively. The resources and subscriptions assigned to a management group automatically inherit the conditions applied to the management group.
[explanation]

---
##Dropdown##

<<display_name:Review Question 3; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Available purchasing and billing options for Azure products and services depend on what?<<

[[
Usage meters
(Customer type)
Cloud Solution Providers
Uptime
]]

[explanation]
It's true that available purchasing options for Azure products and services depend on the type of customer you are. All other answers are incorrect.

Products and services in Azure are arranged by category, with various resources available for provisioning in each category.  You select the Azure products and services that fit your requirements and your account is billed according to Azure's pay-for-what-you-use model.  How you are billed, and which products and services you can choose depends on your customer type.  The three main Azure customer types are  Enterprise,  Web Direct, and Cloud Solution Providers (CSP).
[explanation]

---
##Multiple choice##

<<display_name:Review Question 4; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which of the following are used to determine Azure costs for each billing period?<<


( ) The Azure website
( ) Virtual machines
( ) Microsoft partner companies
(x) Usage meters

[explanation]
Usage meters are used to determine Azure costs for each billing period. The Azure website provides information about, and access to, Azure, while virtual machines are a type of Azure resource.
CSPs typically are Microsoft partner companies who have agreed upon a business arrangement with Microsoft.

When you provision an Azure resource, Azure creates one or more meter instances for that resource.  The meters track the resource's usage. Each meter generates a usage record that Azure uses to calculate your bill. The usage that a meter tracks correlates to a quantity of billable units, which are charged to your account for each billing period.
[explanation]

---
#Checkbox##

<<display_name:Review Question 5; partial_credit="EDC"; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which of the following are factors affecting costs?<<

(choose two)

[ ] Global infrastructure
[x] Resource type
[x] Location
[ ] Availability zone

[explanation]
Resource type and location are factors that affect costs. Global infrastructure refers to a system with architecture that is distributed across many countries, while an availability zone provides failure protection for datacenters.

Azure costs are resource specific. The kind of usage that a meter tracks, and the number of meters associated with a resource, depends on the resource type. The rate of charge per billable unit depends on the resource type. Azure infrastructure is globally distributed. Usage costs between locations offering certain Azure products, services, and resources may vary.
[explanation]
---
##DropDown##

<<display_name:Review Question 6; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Complete the following sentence.  As an Azure customer, Azure Reservations offer discounted prices if you...<<

[[
provision many resources.
(pay in advance).
have a free account.
use Spending Limits.
]]


[explanation]
As an Azure customer, Azure Reservations offer discounted prices if you pay in advance.

There is no requirement to provision many resources to use Azure Reservations, and free accounts can't use Azure Reservations. The Azure Reservations feature is available only for Enterprise or CSP customers, and for those with pay-as-you-go subscriptions.

Spending limits prevent you from exhausting the credit on your account within each billing period. Free-trial customers and some credit-based Azure subscriptions can use the spending limits feature.

Azure Reservations offer discounted prices on certain Azure products and resources. To get a discount, you reserve products and resources by paying in advance.  You can prepay for one or three year's use of certain Azure resources.

[explanation]

---
##Multiple choice##

<<display_name:Review Question 7; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which of the following statements is correct?<<

(x) Paid support plans extend Azure free basic support.
( ) There is no free basic support.
( ) All Azure support is free.

[explanation]
It's true that paid support plans extend Azure free basic support.

There is free basic support for every Azure subscription, which includes access to billing and subscription support, documentation, online self-help, and community-support forums.
Microsoft also offer four paid support plans. including Developer, Standard, Professional Direct, and Premier.

Paid support plans extend Azure free basic support, for Azure customers who require technical and operational support. Providing different Azure support options allows Azure customers to choose a plan that best fits their needs. The support plans you can use, and how you are billed for using support, depends on the type of Azure customer you are and on the Azure subscription you have.
[explanation]

---
##Multiple choice##

<<display_name:Review Question 8; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Complete the following sentence. Performance targets defined within a SLA...?<<

(choose one)

( ) automatically shutdown resources by default.
(x) are specific to each Azure product and service.
( ) typically range from 9.9% to 9.99%.

[explanation]
Performance targets defined within a SLA are specific to each Azure product and service, and they won't automatically shutdown resources by default.

A SLA defines performance targets for an Azure product or service. A typical SLA sets out performance target commitments that range from 99.9 percent (three nines) to 99.99 percent(four nines) for each corresponding Azure product or service. Azure SLAs also describe how Microsoft responds when a product or service fails to perform to its governing SLA's specification.
[explanation]

---
##Multiple choice##

<<display_name:Review Question 9; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>True or false: As you increase availability, you also increase the cost and complexity of your solution?<<

(X) True
( ) False

[explanation]
As you increase availability, you also increase the cost and complexity of your solution.

Availability refers to the proportion of time that a system is functional and working. Maximizing availability requires implementing measures to prevent possible service failures.  Devising preventative measures can be difficult and expensive, and often results in complex solutions. Most providers prefer to maximize the availability of their Azure solutions, by minimizing downtime.

But, it is important to carefully consider the time window against which you measure your application SLA performance targets. The smaller the time window, the tighter the tolerance.  If you define your application SLA in terms of hourly or daily uptime, or availability, you might not always set achievable SLA performance targets.
[explanation]


---
##Dropdown##

<<display_name:Review Question 10; weight:1; max_attempts:2; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>A feature released to all Azure customers is said to have which of the following?<<

[[
Free Availability
High Availability
(General Availability)
Preview Availability
]]

[explanation]
A feature released to all Azure customers is said to have General Availability (GA).

All other answers are incorrect.

Once a feature has been evaluated and tested successfully, it may be released to customers as part of Azure's default product, service, or feature set. A feature released to all Azure customers in this way has GA. In the life cycle of a typical Azure feature, it's common for a feature to move from Azure preview to general availability based on customer evaluation and feedback.
[explanation]