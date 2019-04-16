In this walkthrough, you will generate and then download a cost estimate for a specific resource configuration in Azure, using the Azure Pricing Calculator. The estimate will outline the costs of running a Virtual Machine (VM) and related network resources in Azure.

Finish this walkthrough by completing the steps that follow, or by reading through them.

<p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-13-offline-estimate.png" alt="Screenshot of an example Azure pricing calculator estimate in Microsoft excel."></p>

>**Note**: To create an Azure Pricing Calculator estimate, this walkthrough provides example configurations for the VM and related resources. Use the example configurations or provide the Azure Pricing Calculator with details of your *actual* resource requirements instead.

### Steps

1. In a browser, navigate to the <a href="https://azure.microsoft.com/en-us/pricing/calculator/" target="_blank"><span style="color: #0066cc;">Azure Pricing Calculator</span></a> webpage.

2. To add details of your VM configuration, select **Virtual Machines** from the **Products** tab. Inside the **Virtual Machines added** message dialog, choose **View**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-02-vm-select.png" alt="Screenshot of the featured products area within the Azure pricing calculator webpage. The highlighted add and view vm tiles indicate how to add and view details of a vm configuration in an Azure pricing calculator estimate."></p>

3. Enter a name for your Azure Pricing Calculator estimate, and a name for your VM configuration. This walkthrough example uses **My Pricing Calculator Estimate** for the estimate, and **Windows VM** for the VM configuration.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-03-vm-name.png" alt="Screenshot of the vm configuration area within the Azure pricing calculator estimate webpage. The highlighted estimate name and vm configuration name indicate how to add an estimate name and a vm configuration name to an Azure pricing calculator estimate."></p>

4. Modify the default VM configuration to match the following VM details.

    |Region|Operating system|Type|
    |------|----------------|----|
    |North Europe|Windows|(OS ony)|

    |Tier|Instance|
    |----|--------|
    |Standard|A2: 2 Core(s), 3.5 GB RAM, 135 GB Temporary storage|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-04-vm-configuration.png" alt="Screenshot of the vm configuration area within the Azure pricing calculator estimate webpage. The highlighted examples of user inputted vm configuration property values indicate how to specify a vm configuration within an Azure pricing calculator estimate."></p>

    > **Note**: The VM instance specifications and pricing may differ from those in this example. Follow this walkthrough by choosing an instance that matches the example as closely as possible. To view details about the different VM product options, choose **Product details** from the **More info** menu on the right.

5. Set the **Billing Option** to **Pay as you go**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-05-vm-billing.png" alt="Screenshot of the vm billing options area within the Azure pricing calculator estimate webpage. The highlighted pay as you go billing option indicates how to specify a billing option for a vm within an Azure pricing calculator estimate."></p>

6. In Azure, a month is defined as 730 hours. If your VM needs to be available 100 per cent of the time each month, you set the hours-per-month value to `730`. This walkthrough example requires one VM to be available 50 per cent of the time each month.

    Leave the number of VMs set at `1`, and change the hours-per-month value to `365`.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-06-vm-hours.png" alt="Screenshot of the vm billing options area within the Azure pricing calculator estimate webpage. The highlighted number of vm instances and hours per month options indicate how to specify the number of instances and hours per month for a vm within an Azure pricing calculator estimate."></p>

7. In the **Managed OS Disks** pane, modify the default VM storage configuration by adding the following details.

    |Tier|Disk size|Number of disks|Snapshot|Storage transactions|
    |----|---------|---------------|--------|--------------------|
    |Standard HDD|S30: 1024 GiB|1|Off|10,000|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-07-vm-storage.png" alt="Screenshot of the managed os disks options area within the Azure pricing calculator estimate webpage. The highlighted tier type, disk size, number of disks, and number of storage transactions, options indicate how to specify a storage configuration for a vm within an Azure pricing calculator estimate."></p>

8. To add networking bandwidth to your estimate, go to the top of the Azure Pricing Calculator webpage. Select **Networking** from the product menu on the left, then choose the **Bandwidth** tile. Inside the **Bandwidth added** message dialog, select **View**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-08-network-add.png" alt="Screenshot of the networking products area within the Azure pricing calculator webpage. The highlighted networking, add bandwidth, and view bandwidth, tiles indicate how to add and view details of a networking bandwidth configuration in an Azure pricing calculator estimate."></p>

9. Add a name for your VM bandwidth configuration. This walkthrough example uses the name **Bandwidth: Windows VM**. Modify the default bandwidth configuration by adding the following details.

    |Region|Zone 1 Outbound Data Transferer Amount|
    |------|--------------------------------------|
    |North Europe|50 GB|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-09-network-config.png" alt="Screenshot of the network bandwidth configuration area within the Azure pricing calculator estimate webpage. The highlighted examples of user inputted bandwidth property values indicate how to specify a bandwidth configuration for a vm within an Azure pricing calculator estimate."></p>

10. To add an Application Gateway, return to the top of the Azure Pricing Calculator webpage. From within the **Networking** product menu, choose the **Application Gateway** tile. Inside the **Application Gateway** message dialog, select **View**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-10-appgateway-add.png" alt="Screenshot of the networking products area within the Azure pricing calculator webpage. The highlighted networking, add application gateway, and view application gateway, tiles indicate how to add and view details of an application gateway configuration in an Azure pricing calculator estimate."></p>

11. Add a name for your Application Gateway configuration. This walkthrough uses the name **App Gateway: Windows VM**. Modify the default Application Gateway configuration by adding the following details.

    |Region|Tier|Size|
    |------|----|----|
    |North Europe|Basic|Small|

    |Instances|Hours|
    |-------|-------|
    |1|365|

    |Data processed|
    |--------------|
    |25 GB|

    |Zone 1: North America, Europe|
    |-----------------------------|
    |50 GB|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-11-appgateway-config.png" alt="Screenshot of the application gateway configuration area within the Azure pricing calculator estimate webpage. The highlighted examples of user inputted application gateway property values indicate how to specify an application gateway configuration for a vm within an Azure pricing calculator estimate."></p>

12. Go to the bottom of the Azure Pricing Calculator webpage to view your total **Estimated monthly cost**.

    > **Note**: Explore the various options available within the Azure Pricing Calculator. For example, this walkthrough requires you to update the currency to Euro.

    Change the currency to Euro, then select **Export** to download a copy of the estimate for offline viewing in Microsoft Excel (`.xlsx`) format.

<p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-pricing-12-save-estimate.png" alt="Screenshot of the total estimated monthly costs within the Azure pricing calculator estimate webpage. The highlighted euro currency option indicates how to modify the currency used in an Azure pricing calculator estimate. The highlighted export option illustrates how to download a copy of an estimate for offline viewing."></p>

Congratulations! You downloaded an estimate from the Azure Pricing Calculator.
