<h1><strong><span style="color: #0000CD;">Azure DDoS protection</span></strong></h1>


*Distributed Denial of Service* (DDoS) attacks attempt to overwhelm and exhaust an application’s resources, making the application slow or unresponsive to legitimate users. DDoS attacks can be targeted at any endpoint that is publicly reachable through the internet. Thus, any resource exposed to the internet, such as a website, is potentially at risk from a DDoS attack.

<p style="text-align:left;"><img src="../Linked_Image_Files/ddosprotection.png" width="100" height="100" alt="Image representing DDoS Protection service"></p>

When you combine *Azure DDoS Protection* with application design best practices, you help provide defense against DDoS attacks. DDoS Protection leverages the scale and elasticity of Microsoft’s global network to bring DDoS mitigation capacity to every Azure region. The Azure DDoS Protection service protects your Azure applications by scrubbing traffic at the Azure network edge before it can impact your service's availability.

#### Azure DDoS protection service tiers

Azure DDoS Protection provides the following service tiers:

- *Basic*. The Basic service tier is automatically enabled as part of the Azure platform. Always-on traffic monitoring and real-time mitigation of common network-level attacks provide the same defenses that Microsoft’s online services use. Azure’s global network is used to distribute and mitigate attack traffic across regions.
- *Standard*. The Standard service tier provides additional mitigation capabilities that are tuned specifically to Microsoft Azure Virtual Network resources. DDoS Protection Standard is simple to enable and requires no application changes. Protection policies are tuned through dedicated traffic monitoring and machine learning algorithms. Policies are applied to public IP addresses which are associated with resources deployed in virtual networks, such as Azure Load Balancer and Application Gateway.


#### DDoS standard protection

DDoS standard protection can mitigate the following types of attacks:

- *Volumetric attacks*. The attack's goal is to flood the network layer with a substantial amount of seemingly legitimate traffic.
- *Protocol attacks*. These attacks render a target inaccessible, by exploiting a weakness in the layer 3 and layer 4 protocol stack.
- *Resource (application) layer attacks*. These attacks target web application packets to disrupt the transmission of data between hosts.



> **Note**: You can read more about Azure DDoS Protection from the page <a href="https://azure.microsoft.com/en-us/services/ddos-protection/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure DDoS Protection</span></a>.
