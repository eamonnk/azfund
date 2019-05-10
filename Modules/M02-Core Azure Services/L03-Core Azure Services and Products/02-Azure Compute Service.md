


*Azure compute* is an on-demand computing service for running cloud-based applications. It provides computing resources such as disks, processors, memory, networking and operating systems. The resources are available on-demand and can typically be made available in minutes or even seconds. You pay only for the resources you use and only for as long as you're using them.

There are two common service types for performing compute in Azure: virtual machines and containers.

## What are virtual machines?

*Virtual machines*, (VMs), are software emulations of physical computers. They include a virtual processor, memory, storage, and networking resources. They host an operating system, and you're able to install and run software just like a physical computer. When using a remote desktop client, you can use and control the virtual machine as if you were sitting in front it.

Azure supports a wide range of computing solutions for development and testing, running applications, and extending your datacenter, including Linux, Windows Server, Microsoft SQL Server, Oracle, IBM, and SAP.

Azure also has many services that can run virtual machines, each providing different options depending on your requirements. Some of the most prominent services are VM Scale Sets, App Services, and Azure Functions.

### **Azure VMs**
<p style="text-align:left;"><img src="../Linked_Image_Files/virtualmachines.png" width="100" height="100" alt="Azure virtual machine icon."></p>

Azure VMs lets you create and use virtual machines in the cloud. It provides infrastructure as a service (IaaS) and can be used in a variety of different ways. When you need total control over an operating system and environment, Azure VMs are an ideal choice. Just like a physical computer, you're able to customize all of the software running on the VM. This is particularly helpful when you are running custom software or custom hosting configurations. See <a href="https://azure.microsoft.com/en-us/services/virtual-machines/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Virtual Machines</span></a> for more details.


### **VM scale sets**

<p style="text-align:left;"><img src="../Linked_Image_Files/vmscalesets.png" width="100" height="100" alt="Azure virtual machines scale sets icon."></p>

Virtual machine scale sets are an Azure compute resource that you can use to deploy and manage a set of identical VMs. With all VMs configured the same, VM scale sets are designed to support true auto-scale—no pre-provisioning of VMs is required—and as such makes it easier to build large-scale services targeting big compute, big data, and containerized workloads. So, as demand goes up more virtual machine instances can be added, and as demand goes down virtual machines instances can be removed. The process can be manual, automated, or a combination of both. See <a href="https://azure.microsoft.com/en-us/services/virtual-machine-scale-sets/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Virtual Machine Scale Sets</span></a> for more details.


### **App services**
<p style="text-align:left;"><img src="../Linked_Image_Files/appservice.png" width="100" height="100" alt="Azure App Services icon"></p>

With App services, you can quickly build, deploy, and scale enterprise-grade web, mobile, and API apps running on any platform. You can meet rigorous performance, scalability, security and compliance requirements while using a fully managed platform to perform infrastructure maintenance. App Services is a platform as a service (PaaS) offering. See <a href="https://azure.microsoft.com/en-us/services/app-service/" target="_blank"><span style="color: #0066cc;" color="#0066cc">App Service</span></a> for more details.



### **Functions**

<p style="text-align:left;"><img src="../Linked_Image_Files/azurefunctions.png" width="100" height="100" alt="Image representing Azure Functions"></p>

When you're concerned only about the code running your service and not the underlying platform or infrastructure, Azure Functions are ideal. They're commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less. See <a href="https://azure.microsoft.com/en-us/services/functions/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Functions</span></a> for more details.



## What are containers?

*Containers* are a virtualization environment. However, unlike virtual machines they do not include an operating system. Instead, they reference the operating system of the host environment that runs the container. 

Containers are meant to be lightweight and are designed to be created, scaled out, and stopped dynamically. This allows you to respond to changes on demand and quickly restart in case of a crash or hardware interruption.

Azure supports Docker containers, and there several ways to manage both Docker and Microsoft-based containers in Azure.


### **Azure Container Instances**

<p style="text-align:left;"><img src="../Linked_Image_Files/containerinstance.png" width="100" height="100" alt="Image representing Azure Container Instances"></p>

Azure Container Instances offers the fastest and simplest way to run a container in Azure without having to manage any virtual machines or adopt any additional services. It is a PaaS offering that allows you to upload your containers, which it will run for you. See  <a href="https://azure.microsoft.com/en-us/services/container-instances/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Container Instances</span></a> for more details.



### **Azure Kubernetes Service**

<p style="text-align:left;"><img src="../Linked_Image_Files/kubernetes.png" width="100" height="100" alt="Image representing Azure Kubernetes Service (AKS)"></p>

The task of automating and managing a large number of containers and how they interact is known as *orchestration*. Azure Kubernetes Service (AKS) is a complete orchestration service for containers with distributed architectures and large volumes of containers. See <a href="https://azure.microsoft.com/en-us/services/kubernetes-service/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Kubernetes Service (AKS)</span></a> for more details.




> **Note**: For a full list of compute services available with Azure and the context on when to use them, see <a href="https://azure.microsoft.com/en-us/product-categories/compute/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Compute</span></a>.