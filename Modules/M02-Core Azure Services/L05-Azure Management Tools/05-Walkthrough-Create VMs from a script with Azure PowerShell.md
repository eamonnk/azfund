In this walkthrough you write and run a local PowerShell script. The PowerShell script uses the *Azure PowerShell* module to create three virtual machines (VMs) in Azure from a Linux Ubuntu image.

Finish this walkthrough by completing the steps that follow, or by reading through them.

> **Note**: The screenshots throughout this walkthrough are Windows specific, but the PowerShell commands will run on any suitable Operating System platform within Azure PowerShell.

### Prerequisites

- An active Azure subscription is required. If you do not have an Azure subscription, create a <a href="https://azure.microsoft.com/free/" target="_blank"><span style="color: #0066cc;">free Azure account</span></a> before you begin.
- The Azure PowerShell module requires *Windows PowerShell* 5.1 or higher on Windows, or *PowerShell Core* 6.0 on Windows, Linux, macOS and ARM. Follow these instructions for <a href="https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell?view=powershell-6" target="_blank"><span style="color: #0066cc;">Installing various versions of PowerShell</span></a> on your local machine.
- You must have a text editor installed to write a new PowerShell script.

### Steps

1. Open a text editor. Make a new file, and add the following code into the new file. The comments explain each of the commands within the script file.

    ```PowerShell
    # capture the input parameter in a variable
    param([string]$resourceGroup)

    # prompt for a username and password for the VMs admin account
    # and capture the result in a variable
    $adminCredential = Get-Credential -Message "Enter a username and password for the VM administrator."

    # Add a loop that executes three times to create a new VM for each loop iteration
    For ($i = 1; $i -le 3; $i++)
    {
        # create a name for each VM, store it in a variable and output it to the console
        $vmName = "AzDemo" + $i
        Write-Host "Creating VM: " $vmName

        # create a VM using the $vmName variable
        New-AzVm -ResourceGroupName $resourceGroup -Name $vmName -Credential $adminCredential -Image UbuntuLTS
    }
    ```

2. Save the new file as `azdemo.ps1`. Make a note of the directory location where you save the script file, you will be required to recall the directory location in Step 6.

3. Open a new PowerShell session with *elevated* privileges.

    - **Windows**: Select the **Start** icon from the task bar. Type **PowerShell**. Right select the **Windows PowerShell Desktop App** icon. Choose **Run as administrator**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-03-win-open-powershell.png" alt="Screenshot of the windows task bar and start menu. The start icon, text entry search field, windows powershell icon, and run as administrator menu option are highlighted to demonstrate how to open a powershell session with administrator privileges."></p>

    - **Linux and macOS**: In a terminal, launch PowerShell Core with elevated privileges using the following command.

        ```bash
        sudo pwsh
        ```

4. At the PowerShell prompt, install the Azure PowerShell module (`Az`) by running the following command.

    ```PowerShell
    Install-Module Az -AllowClobber
    ```

    Answer **Yes** or **Yes to All**, if prompted, to trust the `Az` module.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-04-az-install.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to install the Azure powershell module has run successfully. The option to install modules from the powershell gallery has been affirmed."></p>

> **Note**: Windows users should agree to install the *NuGet* provider, and agree to install modules from the *PowerShell Gallery* (PSGallery), if prompted. If you receive script execution failures, run `Set-ExecutionPolicy RemoteSigned` in an elevated PowerShell session. Running the command will unrestricted your execution policy, and allow you to install and run modules from the PSGallery.

5. Update the Az module by running the following command.

    ```PowerShell
    Update-Module -Name Az
    ```

    Answer **Yes** or **Yes to All**, if prompted, to trust updates to the Az module. If you already have the latest version of the Az module installed, the prompt will be returned automatically.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-05-az-update.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to update the Azure powershell module has returned the prompt automatically, indicating that the latest version of the Azure powershell module is installed already."></p>

6. Use the `cd` command to change into the directory that contains the PowerShell script file `azdemo.ps1` that you created in Step 1. Replace `<scriptsdir>` with the actual directory where you saved the script file.

    ```PowerShell
    cd C:\<scriptsdir>
    ```

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-06-az-scriptdir.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to change into the az-script directory has run successfully."></p>

7. Sign into Azure by running the following command. When prompted, provide your Azure login credentials and select the **sign in** button.

    ```PowerShell
    Connect-AzAccount
    ```

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-07-az-login.png" alt="Screenshot of the Microsoft account sign in prompt in front of a Windows powershell session terminal running with administrator privileges. A username has been provided. The password entry field and sign in button are highlighted to demonstrate how to complete the sign in process."></p>

> **Note**: The following Step 8 assumes that you have a single Azure subscription associated with your Azure account. If you have multiple subscriptions, you can get a list of your subscriptions using the command `Get-AzSubscription`. Specify which subscription to use with the command `Select-AzSubscription -Subscription "<Name of your subscription>"`. Substitute `<Name of your subscription>` with the actual name of the subscription you want to use.

8. Create a new resource group using the following command.

    ```PowerShell
    New-AzResourceGroup -Name <name> -Location <location>
    ```

    Replace `<name>` with a suitable name for the new resource group. For example, `AzDemo`. Add a value for `<location>` that corresponds to the Azure region closest to you. For example, `northeurope`.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-08-az-resourcegroup.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to create a new resource group with a user specified name and location has run successfully."></p>

9. Execute the `azdemo.ps1` script by running the following command. Substitute `<resource group name>` with the name of the resource group that you created in the previous Step 8.

    ```PowerShell
    .\azdemo.ps1 <resource group name>
    ```

10. When prompted, provide a username and password for the VM administrator, and select **ok**. For example, for the **User name** enter `azdemoadmin` and for the **Password** enter `pa$$W0rd101`.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-10-az-admin-prompt.png" alt="Screenshot of the windows powershell credential request prompt in front of a Windows powershell session terminal running with administrator privileges. The user created script is running and a username and password for the vm administrator has been provided. The username and password entry fields and ok button are highlighted to demonstrate how to provide vm administrator credentials to azure from a powershell session."></p>

11. The script will begin creating the Azure resources required by each VM, and may take several minutes to complete. Wait for the script to finish before you go to Step 12.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-11a-az-runscript.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The user created script is running. A message in the terminal indicates that azure is creating the resources required by the vms."></p>

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-11b-az-script-finish.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The user created script has completed. The properties for each vm, such as vm name and location, are displayed in the terminal and indicate that azure has created the required resources successfully."></p>

12. When the script is finished, verify that it ran successfully by looking at the resources listed in the resource group that you created in Step 8. When you run the following command you should see three VMs, each with a unique name.

    ```PowerShell
    Get-AzResource -ResourceType Microsoft.Compute/virtualMachines
    ```

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-12-az-listvms.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to list resources within a resource group has run successfully. The output from the command shows properties of three vms, such as vm name and location, in the terminal. Each vm has a unique name which indicates that azure has created the vms successfully."></p>

13. Use the following PowerShell command (`cmdlet`) to delete the resource group, and all related resources.

    ```PowerShell
    Remove-AzResourceGroup -Name <Resource group name>
    ```

    Substitute `<resource group name>` with the name of the resource group you created in Step 8. When asked to confirm the deletion, answer **Yes**. The command may take several minutes to complete, and will return **True** when the resource group is deleted successfully.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-13-az-delete-resources.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to delete a resource group from Azure is running and a prompt to confirm the deletion has been affirmed successfully."></p>

14. Run the following command to disconnect the PowerShell session from your Azure account. Then, close the PowerShell terminal window.

    ```PowerShell
    disconnect-AzAccount
    ```

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l05-azpowershell-14-az-disconnect.png" alt="Screenshot of a Windows powershell session terminal running with administrator privileges. The command to disconnect a powershell session from an Azure account has run successfully."></p>

Congratulations! You wrote and ran a local PowerShell script. The PowerShell script used the Azure PowerShell module to create three VMs in Azure from a Linux Ubuntu image.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.
