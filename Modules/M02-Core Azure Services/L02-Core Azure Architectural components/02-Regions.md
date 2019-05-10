

Microsoft Azure is made up of datacenters located around the globe. These datacenters are organized and made available to end users by region.

A *region* is a geographical area on the planet containing at least one, but potentially multiple datacenters that are in close proximity and networked together with a low-latency network.

For most Azure services, when you deploy a resource in Azure, you choose the region where you want your resource to be deployed. A few examples of regions are *West US*, *Canada Central*, *West Europe*, *Australia East*, and *Japan West*.

Azure has more global regions than any other cloud provider. This provides customers the flexibility and scale needed to bring applications closer to users around the world, preserving data residency and offering comprehensive compliance and resiliency options for customer. At the time of writing this, Azure is generally available in 42 regions around the world, with plans announced for 12 additional regions.


<p style="text-align:center;"><img src="../Linked_Image_Files/azureregions.png" alt="A map of the earth has all of the current Microsoft Azure regions marked."></p>


> **Note**: A list of regions and their locations is available on the page<a href="https://azure.microsoft.com/en-us/global-infrastructure/regions/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Azure Regions</span></a>

### Special Azure regions
Azure also has some special regions that you might want to use when building out your applications for compliance or legal purposes. These special regions include:

- *US DoD Central*, *US Gov Virginia*, *US Gov Iowa* and more: These are  physical and logical network-isolated instances of Azure for US government agencies and partners. They are operated by screened US persons. Includes additional compliance certifications.

- *China East*, *China North* and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft does not directly maintain the datacenters.

- *Germany Central* and *Germany Northeast*: 
These regions are available through a data trustee model whereby customer data remains in Germany under control of T-Systems, a Deutsche Telekom company, acting as the German data trustee. Any user or enterprise who needs their data to reside in Germany can use this service.

### Region pairs
Each Azure region is paired with another region within the same geography (such as US, Europe, or Asia). This approach allows for the replication of resources (such as virtual machine storage) across a geography that helps reduce the likelihood of interruptions due to events such as natural disasters, civil unrest, power outages, or physical network outages affecting both regions at once. Additional advantages of region pairs include:

- In the event of a wider Azure outage, one region out of every pair is prioritized to help reduce the time it takes to restore them for applications. 

- Planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage.

- Data continues to reside within the same geography as its pair (except for Brazil South) for tax and law enforcement jurisdiction purposes.

Examples of region pairs would be West US paired with East US, and SouthEast Asia paired with East Asia.


> **Note**: A full list of region pairs is avalable <a href="https://docs.microsoft.com/en-us/azure/best-practices-availability-paired-regions#what-are-paired-regions" target="_blank"><span style="color: #0066cc;" color="#0066cc">here</span></a>. 

### Feature availability

Finally, some services or virtual machine features are only available in certain regions, such as specific virtual machine sizes or storage types. There are also some global Azure services that do not require you to select a particular region, such as Microsoft Azure Active Directory, Microsoft Azure Traffic Manager, or Azure DNS. 