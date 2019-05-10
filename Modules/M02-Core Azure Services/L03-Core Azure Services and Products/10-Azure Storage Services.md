

*Azure Storage* is a service that you can use to store files, messages, tables, and other types of information. You can use Azure Storage on its own (for example as a file share), but developers also often use it as a store for working data. Such stores can be used by websites, mobile apps, desktop applications, and many other types of custom solutions. Azure Storage is also used by IaaS virtual machines, and PaaS cloud services. 

You can generally think of Azure Storage in categories.


### **Structured data**
*Structured data* is data that adheres to a schema, so all of the data has the same fields or properties. Structured data can be stored in a database table with rows and columns. Structured data relies on keys to indicate how one row in a table relates to data in another row of another table. Structured data is also referred to as *relational data*, as the data's schema defines the table of data, the fields in the table, and the clear relationship between the two. Structured data is straightforward in that it's easy to enter, query, and analyze. All of the data follows the same format. Examples of structured data include, sensor data or financial data.

### **Semi-structured data**
Semi-structured data is less organized than structured data, and is not stored in a relational format, meaning the fields do not neatly fit into tables, rows, and columns. Semi-structured data contains tags that make the organization and hierarchy of the data apparent. Semi-structured data is also referred to as *non-relational* or *NoSQL* data.

### **Unstructured data**
Unstructured data encompasses data that has no designated structure to it. This also means that there are no restrictions on the kinds of data it can hold. For example, a blob can hold a PDF document, a JPG image, a JSON file, video content, etc. As such, unstructured data is becoming more prominent as businesses try to tap into new data sources.

Some of the most common storage service types in Azure are blob, disk, file, and archive.


### **Blob Storage**

<p style="text-align:left;"><img src="../Linked_Image_Files/blobstorage.png" width="100" height="100" alt="Azure Blob Storage icon"></p>

Azure Blob Storage is *unstructured*, meaning that there are no restrictions on the kinds of data it can hold. Blobs are highly scalable and apps work with blobs in much the same way as they would work with files on a disk, such as reading and writing data. Blob Storage can manage thousands of simultaneous uploads, massive amounts of video data, constantly growing log files, and can be reached from anywhere with an internet connection. 

Blobs aren't limited to common file formats. A blob could contain gigabytes of binary data streamed from a scientific instrument, an encrypted message for another application, or data in a custom format for an app you're developing. See <a href="https://azure.microsoft.com/en-us/services/storage/blobs/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Blob Storage </span></a> for more details.



### **Disk storage**

<p style="text-align:left;"><img src="../Linked_Image_Files/diskstorage.png" width="100" height="100" alt="Azure Disk Storage icon"></p>

Disk storage provides disks for virtual machines, applications, and other services to access and use as they need, similar to how they would in on-premises scenarios. Disk storage allows data to be persistently stored and accessed from an attached virtual hard disk. The disks can be managed or unmanaged by Azure, and therefore managed and configured by the user. Typical scenarios for using disk storage are if you want to lift and shift applications that read and write data to persistent disks, or if you are storing data that is not required to be accessed from outside the virtual machine to which the disk is attached. 

Disks come in many different sizes and performance levels, from solid-state drives (SSDs) to traditional spinning hard disk drives (HDDs), with varying performance abilities. Details on pricing are available on the Managed Disks pricing page.
<a href="https://azure.microsoft.com/en-us/pricing/details/managed-disks/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Managed Disks pricing</span></a> page. Also, see <a href="https://azure.microsoft.com/en-us/services/storage/disks/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Disk Storage</span></a> for more general details.



### **File storage**

<p style="text-align:left;"><img src="../Linked_Image_Files/filestorage.png" width="100" height="100" alt="Azure File Storage icon"></p>

Azure Files offers fully managed file shares in the cloud that are accessible via the industry standard Server Message Block (SMB) protocol. Azure file shares can be mounted concurrently by cloud or on-premises deployments of Windows, Linux, and MacOS. Applications running in Azure virtual machines or cloud services can mount a file storage share to access file data, just as a desktop application would mount a typical SMB share. Any number of Azure virtual machines or roles can mount and access the file storage share simultaneously. Typical usage scenarios would be to share files anywhere in the world, diagnostic data, or application data sharing. See <a href="https://azure.microsoft.com/en-us/services/storage/files/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Files</span></a> for more details.



### **Archive storage**

<p style="text-align:left;"><img src="../Linked_Image_Files/archivestorage.png" width="100" height="100" alt="Image representing Azure Archive Storage"></p>

Archive storage provides a storage facility for data that is rarely accessed. It allows you to archive legacy data at low cost to what it would traditionally have cost to create and maintain archives. Archive storage is available as a tier of Blob Storage, object data in the most cost-effective manner. It is stored offline and offers the lowest storage costs. However, it also has the highest access cost, hence it is suited for archival data that is rarely accessed. Archive storage is intended for data that can tolerate several hours of retrieval latency and will remain archived for at least 180 days. See  <a href="https://azure.microsoft.com/en-us/services/storage/archive/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Azure Archive Storage</span></a> for more details.


> **Note**: For a full list of storage services available with Azure, and context on when you use them, see the page <a href="https://azure.microsoft.com/en-us/product-categories/storage/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Storage</span></a>.

