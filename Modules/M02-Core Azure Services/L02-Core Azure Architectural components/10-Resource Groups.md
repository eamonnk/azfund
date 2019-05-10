
A *resource group* is a unit of management for your resources in Azure. You can think of your resource group as a container that allows you to aggregate and manage all the resources required for your application in a single manageable unit. This allows you to manage the application collectively over its life cycle, rather than manage components individually.

You can manage and apply the following resources at resource group level:

- Metering and billing
- Policies
- Monitoring and alerts
- Quotas
- Access control

Remember that when you delete a resource group you delete all resources contained within it.

<p style="text-align:center;"><img src="../Linked_Image_Files/resourcegroup2.png" alt="Conceptual image of a box containing a database, disk, virtual machine, network, and application, representing Azure resources inside a resource group."></p>


### Considerations
When creating and placing resources within resource groups there are a few considerations to take into account:

- Each resource must exist in one, and only one, resource group.

- A resource group can contain resources that reside in different regions.

- You decide how you want to allocate resources to resource groups based on what makes the most sense for your organization.

- You can add or remove a resource to a resource group at any time.

- You can move a resource from one resource group to another.

- Resources for an application do not need to exist in the same resource group. However, it is recommended that you keep them in the same resource group for ease of management.





 






 
