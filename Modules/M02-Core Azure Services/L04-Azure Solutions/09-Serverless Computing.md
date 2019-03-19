<h1><strong><span style="color: #0000CD;">Serverless computing</span></strong></h1>

*Serverless computing* is a cloud-hosted execution environment that runs your code but abstracts the underlying hosting environment. You create an instance of the service and you add your code. No infrastructure configuration or maintenance is required, or even allowed. 

You configure your serverless apps to respond to events. An event could be a REST endpoint, a periodic timer, or even a message received from another Azure service. The serverless app runs only when it's triggered by an event.

Scaling and performance are handled automatically, and you are billed only for the exact resources you use. You don't even need to reserve resources.

Some of the most common serverless service types in Azure are Azure Functions, Azure Logic Apps, and Azure Event Grid.


### **Azure Functions**

<p style="text-align:left;"><img src="../Linked_Image_Files/functions.png" width="100" height="100" alt="Image representing Azure Functions"></p>

*Azure Functions* are ideal when you're only concerned with the code running your service and not the underlying platform or infrastructure. Azure Functions are commonly used when you need to perform work in response to an event—often via a REST request, timer, or message from another Azure service—and when that work can be completed quickly, within seconds or less. 

Azure Functions scale automatically and charges accrue only when a function is triggered, so they're a solid choice when demand is variable. For example, you may be receiving messages from an IoT solution that monitors a fleet of delivery vehicles. You'll likely have more data arriving during business hours. Azure Functions can scale out to accommodate these busier times.

Furthermore, Azure Functions are stateless; they behave as if they're restarted every time they respond to an event. This is ideal for processing incoming data. And if state is required, they can be connected to an Azure storage service. See <a href="https://azure.microsoft.com/en-us/services/functions/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Functions</span></a> for more details.



### **Azure Logic Apps**

<p style="text-align:left;"><img src="../Linked_Image_Files/logicapps.png" width="100" height="100" alt="Image representing Logic Apps"></p>

*Azure Logic Apps* is a cloud service that helps you automate and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across enterprises or organizations. Logic Apps simplifies how you design and build scalable solutions—whether in the cloud, on premises, or both—for app integration, data integration, system integration, enterprise application integration (EAI), and business-to-business (B2B) integration.

Logic Apps are designed in a web-based designer and can execute logic triggered by Azure services without writing any code. To build enterprise integration solutions with Azure Logic Apps, you can choose from a growing gallery of over 200 connectors. These include services such as Salesforce, SAP, Oracle DB, and file shares. See <a href="https://azure.microsoft.com/en-us/services/logic-apps/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Logic Apps</span></a> for more details.




### **Azure Event Grid**

<p style="text-align:left;"><img src="../Linked_Image_Files/eventgrid.png" width="100" height="100" alt="Image representing Azure Event Grid"></p>

*Azure Event Grid* allows you to easily build applications with event-based architectures. It's a fully-managed, intelligent event routing service that uses a publish-subscribe model for uniform event consumption. Event Grid has built-in support for events coming from Azure services, such as storage blobs and resource groups. 

You can use Event Grid to support your own non-Azure-based events in near-real time, using custom topics. You can use filters to route specific events to different endpoints, and ensure your events are reliably delivered. See <a href="https://azure.microsoft.com/en-us/services/event-grid/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Event Grid</span></a> for more details.



> **Note**: For more details about serverless services available with Azure, see the page <a href="https://azure.microsoft.com/en-us/solutions/serverless/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Serverless in Azure</span></a>.
