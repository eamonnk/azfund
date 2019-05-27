

Application security groups (ASGs) enable you to configure network security as a natural extension of an application's structure, allowing you to group virtual machines and define network security policies based on those groups.

   <p style="text-align:center;"><img src="../Linked_Image_Files/asg_icon" alt="Application security group icon."></p>

This feature allows you to reuse your security policy at scale without manual maintenance of explicit IP addresses. The platform handles the complexity of explicit IP addresses and multiple rule sets, allowing you to focus on your business logic.

An ASG enables you to group servers with similar port filtering requirements, and group together servers with similar functions, such as web servers. In the below example we have ASGs defined for WebServers, AppServers and DbServers and green and red arrows indicating which network traffic paths are allowable and which are not. 

   <p style="text-align:center;"><img src="../Linked_Image_Files/M3L02T06_asg_1.png" alt="Screenshot of Webservers, Appservers and Dbservers application groups, with green and red arrows showing defined traffic paths that are allowed and denied as per application security group. There is also a table outlining the same information in table format."></p>


In the below example, multiple applications are deployed into the same virtual network. Based on the security rules described, workloads are isolated from each other. If a VM from one of the applications is compromised, lateral exploration is limited, minimizing the potential impact of an attacker. In this example, let’s assume one of the web server VMs from application1 is compromised, the rest of the application will continue to be protected, even access to critical workloads like database servers will still be unreachable. This implementation provides multiple extra layers of security to your network, making this intrusion less harmful and easy to react on such events.

   <p style="text-align:center;"><img src="../Linked_Image_Files/M3L02T06_asg_2.png" alt="Screenshot a network security group with servers divided into application security groups for Webservers, different applications, App1, App2 and App3, and different databases, Database1, Database2, Database3, with green and red arrows indicating which source groups is  able to access which destination group. There is also a table with the same information listed in table format. "></p>

ASGs help simplify how you can filter and control network traffic coming into your organization and how that network traffic is allowed to move. They allows you to isolate multiple workloads and provide additional levels of protection for your virtual network in a more easily manageable way. See <a href="https://docs.microsoft.com/en-us/azure/virtual-network/security-overview#application-security-groups" target="_blank"><span style="color: #0066cc;" color="#0066cc">Application security groups</span></a> for more details.