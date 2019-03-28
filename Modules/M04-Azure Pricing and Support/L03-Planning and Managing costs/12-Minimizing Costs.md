<h1><strong><span style="color: #0000CD;">Minimizing costs</span></strong></h1>

The following best practice guidelines can help minimize your Azure costs.

### Perform cost analyses

Plan your Azure solution wisely. Carefully consider the products, services, and resources you need, and read the relevant documentation to understand how each of your choices are metered and billed. Additionally, you should calculate your projected costs by using the Azure Pricing and Total Cost of Ownership (TCO) calculators, only adding the products, services, and resources you need.

### Monitor usage with Azure Advisor

<p style="text-align:center;">
<img src="../Linked_Image_Files/0403-monitor-usage-costs.png" alt="Depicts two Azure Advisor monitor results, one for document count and one for storage size">
</p>

In an efficient architecture, provisioned resources match the demand for those resources. The *Azure Advisor* feature identifies unused or under-utilized resources, and you can implement its recommendations by removing unused resources and configuring your resources to match your actual demand.

> **Note**: For more information about Azure Advisor, refer to <a href="https://azure.microsoft.com/en-us/services/advisor/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Azure Advisor</span></a>. </p>


### Use spending limits

Free trial customers and some credit-based Azure subscriptions can use the *Spending Limits* feature. Azure provides the Spending Limits feature to help prevent you from exhausting the credit on your account within each billing period. If you have a credit-based subscription and you reach your configured spending limit, Azure suspends your subscription until a new billing period begins.

The spending limit feature is not available for customers who aren't using credit-based subscriptions, such as Pay-As-You-Go subscribers.


> **Note**: For more information on Azure spending limits, refer to <a href="https://docs.microsoft.com/en-us/azure/billing/billing-spending-limit/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Understand Azure spending limit and how to remove it</span></a>.

> **Note**:  Azure spending limits are not the same as Subscription, Service, or Resource Group limits and quotas. For more information, refer to <a href="https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Azure subscription and service limits, quotas, and constraints</span></a>.</p>


### Use Azure Reservations

*Azure Reservations* offer discounted prices on certain Azure products and resources. To get a discount, you reserve products and resources by paying in advance. You can pre-pay for one year or three years of use of Virtual Machines, SQL Database Compute Capacity, Azure Cosmos Database Throughput, and other Azure resources.

Azure Reservations are only available to Enterprise or CSP customers and for Pay-As-You-Go subscriptions.

> Note: For more information on Azure Reservations, refer to <a href="https://docs.microsoft.com/en-us/azure/billing/billing-save-compute-costs-reservations" target="_blank"><span style="color: #0066cc;" color="#0066cc"> What are Azure Reservations?</span></a>


<p style="text-align:center;">
<img src="../Linked_Image_Files/0403-azure-reservations-savings.png" alt="Depiction of two silos, indicating the 72% cost savings you can realize by using Azure Reservations rather than a Pay-As-You-Go subscription">
</p>

### Choose low-cost locations and regions

The cost of Azure products, services, and resources can vary across locations and regions, and if possible, you should use them in those locations and regions where they cost less.

> **Note**:  Some resources are metered and billed according to how much outgoing network bandwidth they consume (egress).  *You should provision connected resources that are bandwidth metered in the same region* to reduce egress traffic between them.

### Research available cost-saving offers

Keep up-to-date with the latest Azure customer and subscription offers, and switch to offers that provide the greatest cost-saving benefit.

<p>Go to the <a href="https://azure.microsoft.com/en-us/updates/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Updates page</span></a> for information about the latest updates to Azure products, services, and features, as well as product roadmaps and announcements.</p>

### Apply tags to identify cost owners

*Tags* help you manage costs associated with the different groups of Azure products and resources.  You can apply tags to groups of Azure products and resources to organize billing data. For example, if you run several virtual machines for different teams, you can use tags to categorize costs by department, such as Human Resources, Marketing, or Finance, or by environment, such as Production or Test. Tags make it easy to identify groups that generate the biggest Azure costs, so you can adjust your spending accordingly.

> **Note**: For more information about tags, refer to <a href="https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-using-tags" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Use tags to organize your Azure resources</span></a>.
