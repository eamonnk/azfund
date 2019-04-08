In this walkthrough, you create and save a personalized recommendations report with Azure Advisor. You deploy a Virtual Machine (VM) and network resources, which Azure Advisor analyzes, to get recommendations and generate the report.

Finish this walkthrough by completing the steps that follow, or by reading through them.

### Prerequisites

An active Azure subscription is required. If you do not have an Azure subscription, create a <a href="https://azure.microsoft.com/free/" target="_blank"><span style="color: #0066cc;">free Azure account</span></a> before you begin.

### Steps

1. Select the **Deploy to Azure** button to begin deploying a new VM to Azure from a template. Sign into Azure Portal, when prompted.

	[![Deploy to Azure button icon](../Linked_Image_Files/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F101-vm-simple-linux%2Fazuredeploy.json)

	[![Arm visualizer button icon](../Linked_Image_Files/visualizebutton.png)](http://armviz.io/#/?load=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F101-vm-simple-linux%2Fazuredeploy.json)

2. Enter the following details for the new VM.

	- **Subscription**: Select your Azure subscription.
	- **Resource group**: Choose **Create new**, and enter a name for the new resource group. Select the **ok** button.
	- **Location**: Choose the Azure location that is closest to you. For example, `Australia SouthEast`.
	- **Admin Username**: Enter a name for the VM administrator.
	- **Authentication Type**: Select `password`.
	- **Admin Password Or Key**: Enter a password for the VM administrator.
	- **DNS Label Prefix**: Enter a DNS label prefix. For example, `mydnsprefix`
	- **Ubuntu OS Version**: Leave this at the default setting. For example, `16.04.0LTS`
	- **Location**: Leave this at the default setting `[resourceGroup().location]`
	- Check the box to agree to the terms and conditions.
	- Select the **Purchase** button.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-02-createvm.png" alt="Screenshot of the deploy vm from a template pane in Azure portal. The highlighted configuration settings fields, agree to terms and conditions checkbox, and purchase button, illustrate how to configure a vm for deployment to Azure from a template."></p>

> **Note**: When the deployment starts, a notification appears in Azure Portal indicating the deployment is in progress. Another notification is displayed when the deployment has completed successfully.

3. When the deployment has completed, choose **Go to resource group** from the notification area to open the Azure resource group **Overview** blade. You can also select **Resource groups** from the main Azure menu, then choose your resource group from the list.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-03-notifications.png" alt="Screenshot of the deployment in progress and deployment succeeded notifications in Azure portal. The go to resource group button is highlighted to illustrate how to access the newly created resource group from the deployment succeeded notification."></p>

4. Verify that the new VM and associated network resources are present in the Azure resource group **Overview** pane.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-04-verify-resources.png" alt="Screenshot of the resource group overview pane in Azure portal. A list of highlighted resources indicates how to verify that the vm and network resources are present under a specific resource group."></p>

5. Open **Advisor** from the main Azure menu. The **Recommendations** tile under **Overview**, and panels, allow you to filter the recommendations identified by Azure Advisor. For example, for an overview of Security Center recommendations, select the **Security** panel.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-05-run-advisor.png" alt="Screenshot of the recommendations overview pane in Azure advisor. A highlighted advisor menu item illustrates how to open Azure advisor from the main menu in Azure portal. A highlighted security recommendations panel indicates how to access the security center recommendations overview pane from within Azure advisor."></p>

> **Note**: Azure Advisor recommendations are unique to your Azure configuration and usage history. More or less recommendations may be available, in accordance with your Azure resource configurations and usage telemetry.

6. Choose **Follow Security Center Recommendations** to see a list of security center recommendations applicable to your subscription.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-06-follow-recommendations.png" alt="Screenshot of the security center recommendations overview pane in Azure advisor. The highlighted follow security center recommendations message indicates how to access a detailed list of security center recommendations from the overview pane."></p>

7. Select a recommendation from the list for more information. The following example shows how to access information about applying disk encryption to VMs. Explore the other recommendations to learn about Azure Advisor.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-07a-disk-encryption.png" alt="Screenshot of a detailed list of security center recommendations in Azure advisor. Results from the Azure advisor security analyzes are visualized as graphs, charts and icons. One security center recommendation is highlighted within the list to indicate how to access detailed information about applying disk encryption to virtual machines in Azure."></p>

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-07b-disk-encryption-info.png" alt="Screenshot of a security center recommendation which shows textual information that describes the security benefits of applying disk encryption to virtual machines in Azure."></p>

8. To download an Azure Advisor recommendations report, return to the **Azure Advisor Overview**. Select **Download recommendations** as PDF or CSV, and save the report file.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-advisor-08-save-report.png" alt="Screenshot of the recommendations overview pane in Azure advisor. Two highlighted download recommendations links indicate how to download an Azure Advisor recommendations report in pdf and csv format from within in Azure advisor."></p>

Congratulations! You created and saved a personalized recommendations report with Azure Advisor.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.
