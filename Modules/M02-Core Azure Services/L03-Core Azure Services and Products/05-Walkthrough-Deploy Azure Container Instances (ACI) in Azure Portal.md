In this walkthrough, you create, configure, and deploy a Docker container to *Azure Container Instances* (ACI) in Azure Portal. The container is created from an image template called `microsoft/aci-helloworld`. The image packages a small web application, written in Node.js, and serves a static HTML page.

Finish this walkthrough by completing the steps that follow, or by reading through them.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-01-welcome.png" alt="Screenshot of the ACI welcome message shown in a web browser."></p>

### Prerequisites

An active Azure subscription is required. If you do not have an Azure subscription, create a <a href="https://azure.microsoft.com/free/" target="_blank"><span style="color: #0066cc;">free Azure account</span></a> before you begin.

### Steps

1. Select the **Deploy to Azure** button below to create a new Azure Container Instance in Azure Portal. When prompted, sign into Azure Portal.

	![](../../Linked_Image_Files/deploybutton.png)[Deploy to Azure](https://portal.azure.com/#create/microsoft.containerinstances)
	
	![](../../Linked_Image_Files/visualizebutton.png)[Visualize](http://armviz.io/#/?load=https%3A%2F%2Fportal.azure.com%2F%23create%2Fmicrosoft.containerinstances)

2. Provide the following basic details for the new container instance.

	- **Container name**: `mycontainer`
	- **Container image type**: `Public`
	- **Container image**: `microsoft/aci-helloworld`
	- **Subscription**: Choose your subscription.
	- **Resource group**: Select **Create new**, then type `myResourceGroup`, and select **OK**.
	- **Location**: Use the dropdown to choose the Azure region that is closest to you.
	- Press the **OK** button.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-02-basic.png" alt="Screenshot of the basic configuration pane of the create container instances blade, in Azure portal, with basic details entered."></p>

3. Configure the new container instance as follows.

	- **DNS name label**: Specify a DNS name label for your container. The DNS name label you specify must be unique within the Azure region where you create the container instance. Your container will be publicly reachable at `http://<dns-name-label>.<region>.azurecontainer.io`. If you receive a **DNS name label not available** error message, specify a different DNS name label.
	- Leave all other settings in the **Configuration** pane at their default values.
	- Select **OK** to start the automatic validation process.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-03-configure.png" alt="Screenshot of the configuration pane of the create container instances blade, in Azure portal, with the DNS name label entered."></p>

4. When the validation process has passed, review the configuration summary, and select the **OK** button to begin deploying the container.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-04-summary.png" alt="Screenshot of the summary pane of the create container instances blade, in Azure portal, with an overview of the container details."></p>

5. When the deployment starts, a notification appears in Azure Portal indicating the deployment is in progress. Another notification is displayed when the container deployment has completed successfully. Wait for the deployment succeeded notification *before* going to Step 6.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-05-notifications.png" alt="Screenshot of the deployment in progress and the deployment succeeded notifications in Azure portal."></p>

6. Obtain the Fully Qualified Domain Name (FQDN), in Azure Portal, by opening the **Overview** pane for the container group and navigating to **Resource Groups** > **myResourceGroup** > **mycontainer**. Make a note of the **FQDN** of the container instance, as well its **Status**.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-06-fqdn.png" alt="Screenshot of the overview pane for the newly created container in Azure portal, with the FQDN highlighted."></p>

7. When the **Status** value of the container instance is `Running`, navigate to the container's FQDN in a web browser.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l03-aci-01-welcome.png" alt="Screenshot of the ACI welcome message shown in a web browser."></p>

> **Note**: You can also navigate to the container's IP address in your browser. You can obtain the IP address by following Step 6, and making a note of the **IP address** instead of the **FQDN**.

Congratulations! You have used Azure Portal to deploy an application to a container in Azure Container Instances successfully.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.