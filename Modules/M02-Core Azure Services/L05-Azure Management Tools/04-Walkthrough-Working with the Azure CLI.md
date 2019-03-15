In this walkthrough task we will install the Azure CLI on our local machine, then create a virtual machine using the Azure CLI and an Azure Resource Manager template, then verified that deployment using the Azure CLI in the Azure Cloud Shell.

You can complete this walkthrough task by completing the steps outlined below, or you can simply read through them, depending on your available time.

### Prerequisites
- You require need an Azure subscription to perform these steps. If you don't have one you can create one by following the steps outlined on the <a href="https://azure.microsoft.com/en-us/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio" target="_blank"><span style="color: #0066cc;" color="#0066cc">Create your Azure free account today</span></a> webpage.
- A local environment is also needed such as a Windows, Linux or MacOS

> **Note**: The following steps are based on a Windows installation, however they could equally be applicable to a mac or linux environment. However there are specific installation steps for each environment. To see the installation steps for your particular environment see the 
<a href="https://docs.microsoft.com/cli/azure/install-azure-cli" target="_blank"><span style="color: #0066cc;" color="#0066cc">Install the Azure CLI</span></a> page.


### Steps

We will install Azure CLI on the Windows operating system using the MSI installer:

1. To download the Azure CLI msi, click on the URL <a href="https://aka.ms/installazurecliwindows" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://aka.ms/installazurecliwindows</span></a>, and in the browser, select to **Run**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli1.png" alt="Screenshot of create a virtual machine pane on the basics tab entering details for subscription and resource group."></p>

2. In the installation wizard, accept the license terms, and then click **Install**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli2.png" alt="Screenshot of Azure CLI installation wizard with the checkbox to accept the EULA terms checked and the Install button highlighted."></p>

3. In the **User Account Control** dialog, select **Yes**.

4. Once successfully installed, the Azure CLI is run by opening a Bash shell for Linux or macOS, or from the command prompt or PowerShell for Windows. Open a command prompt as administrator.

5. Login to your Azure subscription by runnning the below command and following the prompts

```azurecli
az login
```

6. Verify your installation by running the version check command and ensuring it runs successfully:

    ```azurecli
    az --version
    ```

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli3.png" alt="Screenshot of command prompt with the az --version command having been run and the output present."></p>

> **Note**: Running Azure CLI from PowerShell has some advantages over running Azure CLI from the Windows command prompt. PowerShell provides more tab completion features than the command prompt.



7. Create a resource group to deploy your resources to, by running the following command:

    ```azurecli
    az group create --name < resource group name > --location < your nearest datacenter >
    ```

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli4.png" alt="Screenshot of command prompt with the  az group create --name azcli-rg1 --location eastus command having been run and the output present."></p>


8. We will now deploy a virtual machine and configure it using an Azure Resource Manager template. The template is available on GitHub at the location <a href="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/101-vm-simple-windows/azuredeploy.json" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/101-vm-simple-windows/azuredeploy.json</span></a>, and we will call the script using an Azure CLI command and some other parameters. 

9. Before deploying we will validate the template and command by running the following Azure CLI command, substituting the values with your own, specifying a username and password and a unique name for the virtual machine DNS label prefix value. The command should run successfully without error, identify what is causing the error, modify it and run the command again until it does validate successfully.

 
    ```azurecli
    az group deployment validate \
      --resource-group < resource group created earlier > \
      --template-uri https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/101-vm-simple-windows/azuredeploy.json \
      --parameters adminUsername=$USERNAME \
      --parameters adminPassword=$PASSWORD \
      --parameters dnsLabelPrefix=$DNS_LABEL_PREFIX
    ```
   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli5.png" alt="Screenshot of command prompt with the az group deployment validate command displaying and its output."></p>


10. Deploy the resource by running the following command, substituting the same values as earlier:

    ```azurecli
    az group deployment create \
      --name MyDeployment \
      --resource-group <rgn>[sandbox resource group name]</rgn> \
      --template-uri https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/101-vm-simple-windows/azuredeploy.json  \
      --parameters adminUsername=$USERNAME \
      --parameters adminPassword=$PASSWORD \
      --parameters dnsLabelPrefix=$DNS_LABEL_PREFIX
    ```
   
    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli6.png" alt="Screenshot of command prompt with the az group deployment create command displaying and an output message of running."></p>

11. Verify the deployment by signing into the Azure portal at <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://portal.azure.com</span></a>

12. Go to the resource group you created and verify the virtual machine and resources are present, note the name of the virtual machine is *SimpleWinVM*

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli7.png" alt="Screenshot of resource group in the Azure portal containing deployed resources."></p>

13. It is also possible to use the Azure CLI with the **Azure Cloud Shell**. The **Azure Cloud Shell** has the Azure CLI already installed. Open the **Azure Cloud Shell** by clicking on the *Azure Cloud Shell icon* in the top right of the Azure Portal.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli8.png" alt="Screenshot of Azure Portal Azure Cloud Shell icon."></p>

14. The browser becomes split and the Azure cloud Shell opens in the bottom half of your existing browser and you are prompted to select between **Bash** or **PowerShell**, select **Bash**

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli9.png" alt="Screenshot of Azure Portal Azure Cloud Shell icon."></p>

15. You are prompted to create storage, select **Create storage**, and allow the Azure Cloud Shell to initialize. You do not need to sign into the Azure Clod Shell, it does this automatically for you.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli10.png" alt="Screenshot of Azure Portal Azure Cloud Shell icon."></p>

16. Obtain a list of the virtual machines present in your subscription, and display only the resource group and virtual machine name by running the command:

    ```azurecli
    az vm list --query [].[resourceGroup,name] --out tsv
    ```
    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-azcli11.png" alt="Screenshot of Azure Cloud Shell with the Azure CLI command having been run to query the resource group and virtual machine name, listed in the output."></p>

Congratulations! You have installed the Azure CLI on your local machine, created a virtual machine using the Azure CLI and an Azure Resource Manager template, then verified that deployment using the Azure CLI in the Azure Cloud Shell.

> **Note**: Don't forget to delete any resources you deployed to avoid incurring additional costs from them.


