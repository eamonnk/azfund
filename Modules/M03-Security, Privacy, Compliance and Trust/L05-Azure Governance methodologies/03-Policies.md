
The journey of creating and implementing a policy in Azure Policy begins with creating a policy definition. Every policy definition has conditions under which it is enforced. And, it has an accompanying effect that takes place if the conditions are met.

The process of applying a policy to your resources consist of the following steps:

1. Create a policy definition.
2. Assign a definition to a scope of resources.
3. View policy evaluation results.


### Policy definition

A *policy definition* expresses what to evaluate and what action to take. For example, you could prevent VMs from being deployed if they are exposed to a public IP address. You also could prevent a particular hard disk from being used when deploying VMs to control costs.

The following list contains example policy definitions:

- *Allowed Storage Account SKUs*. This policy definition has a set of conditions/rules that determine whether a storage account that is being deployed is within a set of SKU sizes. Its effect is to deny all storage accounts that do not adhere to the set of defined SKU sizes.
- *Allowed Resource Type*. This policy definition has a set of conditions/rules to specify the resource types that your organization can deploy. Its effect is to deny all resources that are not part of this defined list.
- *Allowed Locations*. This policy enables you to restrict the locations that your organization can specify when deploying resources. Its effect is used to enforce your geographic compliance requirements.
- *Allowed Virtual Machine SKUs*. This policy enables you to specify a set of VM SKUs that your organization can deploy.

A List of sample policies is available on the <a href="https://docs.microsoft.com/en-us/azure/governance/policy/samples/
" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Policy Samples</span></a> page.

### Policy assignment
To implement these policy definitions, whether custom or built-in, you will need to assign them. A *policy assignment* is a policy definition that has been assigned to take place within a specific scope. This scope could range from a management group to a resource group. Policy assignments are inherited by all child resources. This means that if a policy is applied to a resource group, it is applied to all the resources within that resource group. However, you can exclude a subscope from the policy assignment.





> **Note**: You can read more about Azure Policy on the <a href="https://azure.microsoft.com/en-us/services/azure-policy/
" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Policy</span></a> webpage.
