<h1><strong><span style="color: #0000CD;">Choosing Azure network security solutions</span></strong></h1>


It's not enough to simply focus on securing the network perimeter, or on network security between services inside a network. A layered approach provides multiple levels of protection so that if an attacker gets through one layer there are further protections in place. A common security concept that is applied to computing systems is *defense in depth*, which is essentially a layered approach to providing security.

<p style="text-align:center;"><img src="../Linked_Image_Files/defense_in_depth_layers_large.png" width="250" height="250" alt="Image representing the defense in depth concept with seven layers, each one on top of the other. From top to bottom: Physical security, Identity and access, perimeter, network, compute, application, and data."></p>

As the image illustrates, there are many layers that you need to consider. However, a broader security discussion on each layer is beyond the scope at this course. Therefore, we will primarily focus on the *Perimeter layer* and the *Networking layer*.


### Perimeter layer
The network perimeter layer is about protecting organizations from network-based attacks against your resources. Identifying these attacks, alerting, and eliminating their impact is important to keep your network secure. To do this:

- Use Azure DDoS Protection to filter large-scale attacks before they can cause a denial of service for end users.
- Use perimeter firewalls with Azure Firewall to identify and alert on malicious attacks against your network.



### Networking layer
At this layer, the focus is on limiting network connectivity across all your resources to only allow what is required. Segment your resources and use network-level controls to restrict communication to only what is needed. By restricting connectivity, you reduce the risk of lateral movement throughout your network from an attack. Use NSGs to create rules about inbound and outbound communication at this layer. As best practices:

- Limit communication between resources through segmenting your network and configuring access controls.
- Deny by default.
- Restrict inbound internet access and limit outbound where appropriate.
- Implement secure connectivity to on-premises networks.


### Combining services
You can also combine multiple Azure networking and security services to manage your network security and provide increased layered protection.  The following are examples of combined services:

- Network security groups and Azure Firewall. Azure Firewall complements network security group functionality. Together, they provide better defense-in-depth network security. Network security groups provide distributed network layer traffic filtering to limit traffic to resources within virtual networks in each subscription. Azure Firewall is a fully stateful, centralized network firewall-as-a-service, which provides network and application-level protection across different subscriptions and virtual networks.


- Application Gateway WAF and Azure Firewall. *WAF* is a feature of Application Gateway that provides your web applications with centralized, inbound protection against common exploits and vulnerabilities. *Azure Firewall* provides inbound protection for non-HTTP/S protocols (for example, RDP, SSH, FTP), outbound network-level protection for all ports and protocols, and application-level protection for outbound HTTP/S. Combining both provides additional layers of protection.



## Shared responsibilities

As computing environments move from customer-controlled datacenters to cloud datacenters, the responsibility for security also shifts. Security is now a concern shared by both cloud providers and customers.

<p style="text-align:center;"><img src="../Linked_Image_Files/shared_responsibilities.png" width="350" height="450" alt="Image representing the sharing of control over security between the cloud provider, Microsoft, and the customer across On-premises, IaaS, PaaS and SaaS."></p>
