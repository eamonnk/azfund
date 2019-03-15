<h1><strong><span style="color: #0000CD;">Management groups</span></strong></h1>

Azure Management Groups are containers for managing access, policies, and compliance across multiple Azure subscriptions. Management groups allow you to order your Azure resources hierarchically into collections, which provides a further level of classification that is above the level of subscriptions.

<p style="text-align:center;">
<img src="../Linked_Image_Files/0402-management-groups-tree.png" alt="Management groups tree image">
</p>

You can manage your Azure subscriptions more effectively by using Azure Policy and Azure role-based access controls (RBACs). These provide distinct governance conditions that you can apply to each management group. The resources and subscriptions you assign to a management group automatically inherit the conditions that you apply to that management group.

> **Note**: For more information about management groups, refer to <a href="https://docs.microsoft.com/en-us/azure/governance/management-groups/create?toc=%2Fazure%2Fbilling%2FTOC.json" target="_blank"><span style="color: #0066cc;" color="#0066cc">Create management groups for resource organization and management</span></a>  and <a href="https://docs.microsoft.com/en-us/azure/governance/management-groups/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Organize your resources with Azure management groups</span></a>.