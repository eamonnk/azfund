In this walkthrough, you use *Azure Cloud Shell* to automate the installation of the Windows *Internet Information Services* webserver (IIS) on a new virtual machine (VM). Azure Cloud Shell creates a VM and uses the *Custom Script Extension* to install IIS.

Finish this walkthrough by completing the steps that follow, or by reading through them.

### Prerequisites

An active Azure subscription is required. If you do not have an Azure subscription, create a <a href="https://azure.microsoft.com/free/" target="_blank"><span style="color: #0066cc;">free Azure account</span></a> before you begin.

### Steps

1. To access **Azure Cloud Shell** go to the location <a href="https://shell.azure.com" target="_blank"><span style="color: #0066cc;">https://shell.azure.com</span></a> and sign in with your Azure user login credentials.


	You can also run Azure Cloud Shell from within Azure Portal by using the Cloud Shell icon.

	<p style="text-align:left;"><img src="../Linked_Image_Files/m02-l05-cloudshell-01-portal-icon.png" alt="Screenshot of the quick launch menu in Azure portal. The launch Azure cloud shell icon is highlighted to indicate how to start Azure cloud shell from within Azure portal."></p>

2. If prompted, choose a **Bash** or **PowerShell** environment. This walkthrough uses **PowerShell**.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-02-choose-env.png" alt="Screenshot of the welcome to Azure cloud shell message. The options for choosing a bash or powershell environment are highlighted to illustrate how to choose your preferred environment when Azure cloud shell starts for the first time."></p>

3. First time Azure Cloud Shell users must create and configure Cloud Drive storage, to allow Azure Cloud Shell files to persist. To create and configure storage, select **Show advanced settings**. If you have created and configured storage already, go to Step 5.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-03-choose-storage.png" alt="Screenshot of the no storage mounted message in Azure cloud shell. The message is shown to first time users of Azure cloud shell. The option to show advanced settings is highlighted to illustrate how to access the storage setup advanced settings when Azure cloud shell starts for the first time."></p>

4. Provide the following details to create and configure storage.

	- **Subscription**: Choose your subscription.
	- **Cloud Shell region**: Select the location closest to you. For example, `North Europe`
	- **Resource group**: Choose **Create new**, then provide a unique name for your new resource group.
	- **Storage account**: Select **Create new**, and provide a unique name for your storage account.
	- **File share**: Choose **Create new**, then enter a unique file share name.
	- Select the **Create storage** button

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-04a-set-storage.png" alt="Screenshot of the create and configure storage settings in Azure cloud shell. The required settings fields and create storage button are highlighted to illustrate how to create and configure advanced storage settings in Azure cloud shell."></p>

	Wait for the storage setup to complete. When the storage setup is complete, the **Welcome to Azure Cloud Shell** message is shown in the terminal window.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-04b-competed-storage.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. Highlighted storage properties, such as storage account name and file share name, indicate that storage has been created and configured in Azure cloud shell successfully. A highlighted welcome to Azure cloud shell message indicates that a new powershell session has started in Azure cloud shell."></p>

5. At the Azure Cloud Shell prompt, set a VM administrator username and password with the `Get-Credential` command. The credentials are assigned to the variable `$cred`. The variable is recalled when the new VM is created in the next Step 6.

	```PowerShell
	$cred = Get-Credential
	```

	When prompted, enter a username and password for the VM administrator. For example, 
    - **User**: `myVMAdmin` 
    - **Password**: `pa$$W0rd101`

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-05-admin-credentials.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. The command to set a username and password for the vm administrator is running. A username and password are entered and assigned to a variable."></p>

6. Create a VM with the `New-AzVM` command. The following example creates a VM named `myVM` in the `North Europe` location. If they do not exist, the resource group `myResourceGroup` and supporting network resources are created in Azure. To allow web traffic, the following command also opens port 80. Change these to more suitable settings, if you prefer.

    > **Note**: Ensure you are signed into your Azure subscription. If you have multiple subscriptions, you can get a list of your subscriptions using the command `Get-AzSubscription`. Specify which subscription to use with the command `Select-AzSubscription -Subscription "<Name of your subscription>"`. Substitute the actual name of the subscription you want to use for `<Name of your subscription>`.

	```PowerShell
	New-AzVm `
		-ResourceGroupName "myResourceGroup" `
		-Name "myVM" `
		-Location "North Europe" `
		-VirtualNetworkName "myVnet" `
		-SubnetName "mySubnet" `
		-SecurityGroupName "myNetworkSecurityGroup" `
		-PublicIpAddressName "myPublicIpAddress" `
		-OpenPorts 80 `
		-Credential $cred
	```

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-06a-create-vm-start.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. The command to create a new vm and the required resources is running."></p>

	When the newly created resources and VM are ready, details about the resources and VM will be displayed in the Azure Cloud Shell window. Wait for the resources and VM to be created.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-06b-create-vm-finish.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. Details such as resource group name and vm id are shown which indicates that the command to create a new vm and the required resources has completed successfully."></p>

7. Use the `Set-AzVMExtension` command to install the Custom Script Extension. The Custom Script Extension runs the command `powershell Add-WindowsFeature Web-Server` to install IIS to your new VM.

	```PowerShell
	Set-AzVMExtension -ResourceGroupName "myResourceGroup" `
		-ExtensionName "IIS" `
		-VMName "myVM" `
		-Location "North Europe" `
		-Publisher Microsoft.Compute `
		-ExtensionType CustomScriptExtension `
		-TypeHandlerVersion 1.8 `
		-SettingString '{"commandToExecute":"powershell Add-WindowsFeature Web-Server"}'
	```

	Wait for the Custom Script Extension and IIS to install. When the Custom Script Extension installs IIS successfully, `IsSuccessStatusCode` will return `True` in the Azure Cloud Shell window.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-07-iis-installed.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. A highlighted true value indicates that the commands to install the custom script extension and iis have completed successfully."></p>

8. Obtain the public IP address of your load balancer with the `Get-AzPublicIPAddress` command. The following example obtains the IP address for *myPublicIPAddress* created in Step 4.

	```PowerShell
	Get-AzPublicIPAddress `
		-ResourceGroupName "myResourceGroup" `
		-Name "myPublicIPAddress" | select IpAddress
	```

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-08-obtain-ip.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. The command for obtaining the public IP address of the load balancer has run. An ip address is highlighted which indicates that the command has completed successfully."></p>

9. Use a web browser to navigate to the public IP address. The Windows server **IIS Welcome** page should be displayed in your browser.

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-09-iss-welcome.png" alt="Screenshot of the Windows webserver iis welcome page in a web browser. The page indicates that iis has been installed to the vm successfully."></p>

10. Return to Azure Cloud Shell. Run the following command to remove the resource group `myResourceGroup`, VM, and all related resources. Choose **Yes** to confirm the deletion, when prompted.

	```PowerShell
	Remove-AzResourceGroup -Name myResourceGroup
	```

	<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-cloudshell-10-delete-resourcegroup.png" alt="Screenshot of a powershell session terminal running in Azure cloud shell. The command to delete a resource group is running and a request to confirm the deletion has been affirmed."></p>

Congratulations! You used Azure Cloud Shell to automate the installation of IIS on a new VM.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.
