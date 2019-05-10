

A *Firewall* is a service that grants server access based on the originating IP address of each request. You create firewall rules that specify ranges of IP addresses. Only clients from these granted IP addresses will be allowed to access the server. Firewall rules, generally speaking, also include specific network protocol and port information.

<p style="text-align:left;"><img src="../Linked_Image_Files/firewall.png" width="130" height="100" alt="Image representing Azure Firewall"></p>

*Azure Firewall* is a managed, cloud-based, network security service that protects your Azure Virtual Network resources. It is a fully stateful firewall as a service with built-in high availability and unrestricted cloud scalability.

You can create, enforce, and log, application and network connectivity policies across subscriptions, and virtual networks, centrally. Azure Firewall uses a static public IP address for your virtual network resources, which allows outside firewalls to identify traffic originating from your virtual network. The service is fully integrated with Azure Monitor for logging and analytics.

Azure Firewall provides many features, including:

- Built-in high availability.
- Unrestricted cloud scalability.
- Inbound and outbound filtering rules.
- Azure Monitor logging.


**Common Usage Scenarios**

You typically deploy Azure Firewall on a central virtual network to control general network access. With Azure Firewall you can configure:

- Application rules that define fully qualified domain names (FQDNs) that can be accessed from a subnet.
- Network rules that define source address, protocol, destination port, and destination address.




*Azure Application Gateway* also provides a firewall, called the *Web Application Firewall* (WAF). However, WAF is different to Azure Firewall. WAF provides centralized, inbound protection for your web applications against common exploits and vulnerabilities. While in contrast, Azure Firewall provides outbound, network-level protection for all ports and protocols, and application-level protection for outbound HTTP/S. In addition, Azure Firewall provides inbound protection for non-HTTP/S protocols. Examples of non-HTTP/S protocols include: Remote Desktop Protocol (RDP), Secure Shell (SSH), and File Transfer Protocol (FTP). Azure Firewall's extended functionality make it suitable for different uses.




> **Note**: For more details, see the <a href="https://azure.microsoft.com/en-us/services/azure-firewall/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Azure Firewall</span></a> page.


