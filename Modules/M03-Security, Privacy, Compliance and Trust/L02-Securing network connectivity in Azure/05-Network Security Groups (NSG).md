<h1><strong><span style="color: #0000CD;">Network Security Groups</span></strong></h1>



*Network Security Groups* (NSGs) allow you to filter network traffic to and from Azure resources in an Azure virtual network. An NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port, and protocol.


<p style="text-align:left;"><img src="../Linked_Image_Files/nsg.png" width="100" height="100" alt="Image representing Network Security Groups"></p>


#### Network security rule properties
A network security group can contain as many rules as you  need, within Azure subscription limits. Each rule specifies the following properties:

| Property| Explanation| 
| --- | --- |
| Name |Unique name of the NSG. |
| Priority | A number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers. |
| Source or Destination| Individual IP address or IP address range, service tag, or application security group. |
| Protocol | TCP, UDP, or Any.|
| Direction| Whether the rule applies to inbound or outbound traffic. |
| Port Range | An individual port or range of ports. |
| Action | Allow or Deny. |



When you create a network security group, Azure creates a series of default rules to provide a baseline level of security. You cannot remove the default rules, but you can override them by creating new rules with higher priorities.




> **Note**: You can read more about NSGs on the <a href="https://docs.microsoft.com/en-us/azure/virtual-network/security-overview#network-security-groups" target="_blank"><span style="color: #0066cc;" color="#0066cc">Security groups</span></a> page.
