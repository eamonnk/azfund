<h1><strong><span style="color: #0000CD;">Factors affecting costs</span></strong></h1>

The following sections describe the main factors that affect Azure costs, including resource type, services, and the user's location.

### Resource type

Costs are resource-specific, so the usage that a meter tracks and the number of meters associated with a resource depend on the resource type.

> **Note**: Each meter tracks a *particular kind of usage*.  For example, a meter might track bandwidth usage (ingress or egress network traffic in bits-per-second), number of operations, size (storage capacity in bytes), or similar items.

The usage that a meter tracks correlates to a quantity of billable units. Those are charged to your account for each billing period, and the rate per billable unit depends on the resource type you are using.

### Services

Azure usage rates and billing periods can differ between Enterprise, Web Direct, and Cloud Solution Provider (CSP) customers. Some subscription types also include usage allowances, which affect costs.

The Azure team develops and offers first-party products and services, while products and services from third-party vendors are available in the <a href="https://azuremarketplace.microsoft.com" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Azure marketplace</span></a>.  Different billing structures apply to each of these categories.

<p style="text-align:center;">
<img src="../Linked_Image_Files/0403-billing-period-graphic.png" width="300" height="250" alt="Depicts a billing period, with a calendar, computer, and meter linked to illustrate correlation between the three">
</p>

### Location

The Azure infrastructure is globally distributed, and usage costs might vary between locations that offer particular Azure products, services, and resources.

For example, you might want to build your Azure solution by provisioning resources in locations that offer the lowest prices, but this would require transferring data between locations, if dependent resources and their users are located in different parts of the world. If there are meters tracking the volume of data that transfers between the resources you provision, any potential savings you make from choosing the cheapest location could be offset by the additional cost of transferring data between those resources.

> **Note**: For more information about Azure usage charges, refer to <a href="https://docs.microsoft.com/en-us/azure/billing/billing-understand-your-invoice" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Understand terms on your Microsoft Azure invoice</span></a>.