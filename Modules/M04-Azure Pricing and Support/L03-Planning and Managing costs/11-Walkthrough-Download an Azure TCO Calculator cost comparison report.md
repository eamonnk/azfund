In this walkthrough, you download a cost comparison report using the *Total Cost of Ownership* (TCO) *Calculator* in Azure. To create the report, the TCO Calculator uses information that you provide about your on-premises infrastructure and workloads to recommend cost savings that you can make with Azure.

>**Note**: This walkthrough provides example definitions of on-premises infrastructure and workloads for a typical datacenter. To create a TCO Calculator report, use the example definitions or provide details of your *actual* on-premises infrastructure and workloads.

Finish this walkthrough by completing the steps that follow, or by reading through them.

### Steps

1. In a browser, navigate to the <a href="https://azure.microsoft.com/en-us/pricing/tco/calculator/" target="_blank"><span style="color: #0066cc;">Total Cost of Ownership (TCO) Calculator</span></a> webpage.

2. To add details of your on-premises server infrastructure, select **+ Add server workload** in the **Servers** pane.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-02-add-workload.png" alt="Screenshot of the define your workloads pane of the tco calculator in Azure. The highlighted add workload button indicates how to add new on-premises infrastructure and workload definitions to the Azure tco calculator."></p>

3. Provide a name for your server workloads definition. This example uses the name **Servers: Windows VMs**. Enter the following details into the TCO Calculator.

    |Workload|Environment|Operating system|VMS|Virtualization|Core(s)|RAM|Optimize by|
    --------|-----------|----------------|---|--------------|-------|---|-----------|
    |Windows/ Linux server|Virtual machines|Windows|500|VMware|8|16|CPU|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-03-vms-windows.png" alt="Screenshot of the define server workloads pane of the tco calculator in Azure. The highlighted and completed input fields indicate how to provide the Azure tco calculator with an on-premises windows server workload definition."></p>

4. Select **+ Add server workload** to make a row for a new server workloads definition. Provide a name for the server workloads definition. This example uses the name **Servers: Linux VMs**. Enter the following details into the TCO Calculator.

    |Workload|Environment|Operating system|VMS|Virtualization|Core(s)|RAM|Optimize by|
    |--------|-----------|----------------|---|--------------|-------|---|-----------|
    |Windows/ Linux server|Virtual machines|Linux|500|VMware|8|16|CPU|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-04-vms-linux.png" alt="Screenshot of the define server workloads pane of the tco calculator in Azure. The highlighted and completed input fields indicate how to provide the Azure tco calculator with an on-premises linux server workload definition."></p>

5. This example definition does not require a database. Leave the **Databases** pane empty. In the **Storage** pane of the TCO Calculator, provide a name for your storage infrastructure definition. Enter the following details into the TCO Calculator.

    |Storage type|Disk type|Capacity|Backup|Archive|
    |------------|---------|--------|------|-------|
    |Local Disk/ SAN|HDD|60 TB|0 TB|0 TB|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-05-storage.png" alt="Screenshot of the define storage infrastructure pane of the tco calculator in Azure. The highlighted and completed input fields indicate how to provide the Azure tco calculator with an on-premises storage infrastructure definition."></p>

6. In the **Networking** pane of the TCO Calculator, provide a name for your networking infrastructure definition. Enter the following details, then select **Next**.

    |Outbound bandwidth|
    |------------------|
    |15 TB|

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-06-networking.png" alt="Screenshot of the define networking infrastructure pane of the tco calculator in Azure. The highlighted and completed input fields indicate how to provide the tco calculator with an on-premises networking infrastructure definition. The highlighted next button indicates how to proceed to the adjust assumptions pane of the Azure tco calculator."></p>

7. Explore the options and make any adjustments that you require. The currency used in this example is Euros. No other adjustments are required by this example. Select **Next**, at the end of the page.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-07-adjust.png" alt="Screenshot of the adjust assumptions pane of the tco calculator in Azure. The highlighted and completed currency input field indicates how set the currency used by the tco calculator to euros. The highlighted next button indicates how to proceed to the report pane of the Azure tco calculator."></p>

8. Review the Azure cost saving recommendations and visualizations in the TCO calculator report. This example requires you to adjust the **Timeframe** to **3 years**, and the region to **North Europe**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-08-report-view.png" alt="Screenshot of the report pane of the tco calculator in Azure. The highlighted and completed input fields indicates how set the tco calculator timeframe to three years and the region to north europe. A graph shows the cost of on-premises infrastructure and workloads off-set against the reduced cost of using Azure."></p>

9. To modify the information you provided to the TCO calculator, go to the bottom of the page, and select **Back**. To save or print a PDF copy of the report select **Download**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m04-l03-tco-09-report-save.png" alt="Screenshot of the report pane of the tco calculator in Azure. The highlighted back button indicates how to return to the adjust assumptions pane. The highlighted download button indicates how to save or print a pdf copy of the tco calculator report."></p>

Congratulations! You downloaded a cost comparison report from the TCO Calculator in Azure.
