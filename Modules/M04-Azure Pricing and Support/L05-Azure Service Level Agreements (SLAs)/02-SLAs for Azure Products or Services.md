<h1><strong><span style="color: #0000CD;">SLAs for Azure products and services</span></strong></h1>

There are three key characteristics of SLAs for Azure products and services, which the following sections detail.

1. **Performance Targets, Uptime and Connectivity Guarantees**

    A SLA defines performance targets for an Azure product or service.  The performance targets that a SLA defines are specific to each Azure product and service.

    For example, performance targets for some Azure services are expressed in terms of uptime or connectivity rates.

    <p style="text-align:center;"><img src="../Linked_Image_Files/0405-sla-target.png" width="300" height="300" alt="Image depicting data being measured and processed in the cloud"></p>


2. **Performance targets range from 99.9 percent to 99.99 percent**

    A typical SLA specifics performance-target commitments that range from 99.9 percent ("three nines") to 99.99 percent ("four nines"), for each corresponding Azure product or service. These targets can apply to such performance criteria as uptime, or response times for services.

    For example, the SLA for the Azure Database for MySQL service guarantees 99.99 percent uptime.  The Azure Cosmos DB (Database) service SLA offers 99.99 percent uptime, which includes low-latency commitments of less than 10 milliseconds on DB read operations and less than 15 milliseconds on DB write operations.

    <p style="text-align:center;"><img src="../Linked_Image_Files/0405-sla-range.png" width="400" height="300" alt="Image showing a lightbulb representing ideas and cloud data visualized as a pie chart"></p>

3. **Service Credits**

    SLAs also describe how Microsoft will respond if an Azure product or service fails to perform to its governing SLA's specification.

    For example, customers may have a discount applied to their Azure bill, as compensation for an under-performing Azure product or service. The table below explains this example in more detail.

    The first column in the table below shows monthly uptime percentage SLA targets for a single instance Azure Virtual Machine. The second column shows the corresponding service credit amount you receive, if the *actual* uptime is less than the specified SLA target for that month.

    | MONTHLY UPTIME PERCENTAGE | SERVICE CREDIT PERCENTAGE|
    | --- | --- |
    | < 99.9 |10 |
    | < 99 |25 |
    | < 95 |100 |

> **Note**: Azure does not provide SLAs for many services under the *Free* or *Shared* tiers. Also, free products such as Azure Advisor do not typically have a SLA.

> **Note**: For more information about specific Azure SLAs for individual products and services, refer to <a href="https://azure.microsoft.com/en-us/support/legal/sla/summary/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> Service Level Agreements</span></a>.