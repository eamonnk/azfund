

You can configure and manage Azure using a broad range of tools and platforms. There are tools available for the command line, language-specific Software Development Kits (SDKs), developer tools, tools for migration, and many others. Tools that are commonly used for day-to-day management and interaction include: *Azure Portal*, for interacting with Azure via a Graphical User Interface (GUI); *Azure PowerShell*, *Azure Command-Line Interface* (CLI), and *Azure Cloud Shell*, for command line and automation-based interactions with Azure.

Creating administration scripts and using automation tools is a powerful way to optimize your work flow. You can automate common repetitive tasks, and once a script has been verified it will run consistently, thereby reducing errors.


### **Azure Portal**
Azure Portal is a website that you can access with a web browser, by going to the URL <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://portal.azure.com</span></a>. From here you can interact manually with all the Azure services. You can identify a service you are looking for, obtain links for help and more learning on particular topics, and deploy, manage and delete resources. It also guides you through complex administrative tasks by providing wizards and tooltips.

The dashboard view provides high-level details about your Azure environment. You can customize the portal view as you need by moving and resizing tiles, displaying just particular services of interest, accessing links for help and support, and providing feedback.

The portal does not provide any way to automate repetitive tasks. For example, to set up multiple VMs, you would need to create them one at a time by completing the wizard for each VM. This can be time-consuming and error-prone for complex tasks. 

<p style="text-align:center;"><img src="../Linked_Image_Files/azureportal.png" alt="Screenshot of the Azure portal landing page."></p>


### **Azure PowerShell**
Azure PowerShell is a module that you add to Windows PowerShell or PowerShell Core that enables you to connect to your Azure subscription and manage resources. Azure PowerShell requires Windows PowerShell to function. PowerShell provides services such as the shell window and command parsing. Azure PowerShell then adds the Azure-specific commands.

For example, Azure PowerShell provides the **New-AzureRmVM** command that creates a virtual machine for you inside your Azure subscription. To use it, you would launch PowerShell, sign in to your Azure account using the command `Connect-AzureRMAccount`, and then issue a command such as:


```powershell
New-AzureRmVm `
    -ResourceGroupName "TesResourceGroup" `
    -Name "Testvm" `
    -Image "UbuntuLTS"
    ...
```


<p style="text-align:center;"><img src="../Linked_Image_Files/powershell1.png" alt="a powershell console window with the powershell command New-AzureRmVm     -ResourceGroupName TesResourceGroup  -Name Testvm -Image UbuntuLTS command having been successfully run and created a virtual machine."></p>


> **Note**: *PowerShell Core* is a cross-platform version of PowerShell that runs on Windows Linux or macOS. Details are available from the page <a href="https://docs.microsoft.com/en-us/powershell/scripting/whats-new/what-s-new-in-powershell-core-60?view=powershell-6" target="_blank"><span style="color: #0066cc;" color="#0066cc"> What's New in PowerShell Core 6.1</span></a> which is now also available.

### **Azure CLI**
Azure CLI is a cross-platform command-line program that connects to Azure and executes administrative commands on Azure resources. *Cross platform* means that it can be run on Windows, Linux, or macOS. For example, to create a VM, you would open a command prompt window, sign in to Azure using the command `az login`, create a resource group, then use a command such as:

```azurecli
az vm create \
  --resource-group Testrg1 \
  --name Testvm \
  --image UbuntuLTS
  --generate-ssh-keys
  ...
```

<p style="text-align:center;"><img src="../Linked_Image_Files/azclivmcreate.png" alt="Screenshot of a command prompt window with the az cli command having been run az vm create --resource group Testrg1 --name Testvm --image UbuntuLTS having been successfully run, and created a virtual machine."></p>



### **Azure Cloud Shell**
Azure Cloud Shell is a browser-based scripting environment in your portal. It provides the flexibility of choosing the shell experience that best suits the way you work. Linux users can opt for a Bash experience, while Windows users can opt for PowerShell.

A storage account is required to use the cloud shell and you will be prompted to create one when accessing the Azure cloud shell.


> **Note**: You can access Azure Cloud Shell by going to <a href="https://shell.azure.com/" target="_blank"><span style="color: #0066cc;" color="#0066cc"> https://shell.azure.com/</span></a>.




> **Note**: There are also <b>Azure SDKs</b> in a range of languages, as well as <b>REST APIs</b> through which you can configure Azure. For a full list of tools available, see the <a href="https://azure.microsoft.com/en-us/downloads/" target="_blank"><span style="color: #0066cc;" color="#0066cc">Downloads</span></a> page.
