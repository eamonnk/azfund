
In this walkthrough task we will create a virtual machine in Azure via the Azure Portal, configure it as a web server and connect to the web server over the internet.

You can complete this walkthrough task by completing the steps outlined below, or you can simply read through them, depending on your available time.

### Prerequisites
- You require need an Azure subscription to perform these steps. If you don't have one you can create one by following the steps outlined on the <a href="https://azure.microsoft.com/en-us/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio" target="_blank"><span style="color: #0066cc;" color="#0066cc">Create your Azure free account today</span></a> webpage.


### Steps

1. Sign in to the Azure portal at <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://portal.azure.com</span></a>
2. Choose **Create a resource** in the upper left-hand corner of the Azure portal.
3. In the search box above the list of Azure Marketplace resources, search for and select **Windows Server 2016 Datacenter**, then choose **Create**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal1a.png" alt="Screenshot of the Marketplace pane search blade with windows server 2016 datacenter entered,  returned in a list of matches and highlighted."></p>

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal1b.png" alt="Screenshot of the Windows Server 2016 datadenter resource object blade and the button create highlighted."></p>

4. In the **Basics** tab, under Project details, make sure the correct subscription is selected and then choose to **Create new resource group**. Type *myResourceGroup* for the name. 

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal1.png" alt="Screenshot of create a virtual machine pane on the basics tab entering details for subscription and resource group."></p>


5. Under **Instance details**, type **myVM** for the Virtual machine name and choose **East US** for your Location. Leave the other defaults.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal2.png" alt="Screenshot of create a virtual machine pane on the basics tab and the instance details section , entering details for VM name, regions, availability options , image and size."></p>

6. Under the **Administrator account** section, provide a username, such as **azureuser** and a password. The password must be at least 12 characters long and meet the defined complexity requirements.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal3.png" alt="Screenshot of create a virtual machine pane on the basics tab and the administrator account section entering values for username and password ."></p>

7. Under **Inbound port** rules, choose **Allow selected ports** and then select **RDP (3389)** and **HTTP (80)** from the drop-down. These are to allow us to connect to the virtual machine using RDP over port 3389 and then to see a web page display over HTTP on port 80.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal4.png" alt="Screenshot of create a virtual machine pane on the basics tab and the inbound port rules section, allowing selected ports and enabling ports RDP 3389 and HTTP."></p>

8. Go to the Management tab and under the **Monitoring** section under **Boot diagnostics** select **Off**

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal5a.png" alt="Screenshot of create a virtual machine pane on the review and management tab under the Monitoring section with Boot diagnostics set to off and highlighted."></p>

9. Leave the remaining defaults and then select the **Review + create** button at the bottom of the page.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal5.png" alt="Screenshot of create a virtual machine pane on the review and create pane, with Save money displaying on the pane along with the Review + Create button."></p>


10. Once Validation is passed click the **Create** button. It can take approx three to five minutes to deploy the virtual machine.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal6a.png" alt="Screenshot of create a virtual machine pane on the validation passed blade with the validation passed message highlighted and the Create button highlighted."></p>

11. Once the virtual machine is created, go to the resource group you placed the virtual machine in, and open up the virtual machine, then click the **Connect** button on the virtual machine properties page.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal6b.png" alt="Screenshot of myResourcegroup details pane with the virtual machine myVM highlighted."></p>

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal6.png" alt="Screenshot of the virtual machine properties with the Connect button highlighted."></p>


> **Note**: The following directions tell you how to connect to your VM from a Windows computer. On a Mac, you need an RDP client such as this Remote Desktop Client from the Mac App Store and on Linux virtual machine you could connect directly from a bash shell using `ssh`.

12. In the **Connect to virtual machine** page, keep the default options to connect by DNS name over port 3389 and click **Download RDP File**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal7.png" alt="Screenshot of the Connect to virtual machine pane with the download rdp file button highlighted"></p>

13. Open the downloaded RDP file and click **Connect** when prompted. 

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal8.png" alt="Screenshot of the virtual machine properties with the Connect butotn highlighted"></p>

14. In the **Windows Security** window, select **More choices** and then **Use a different account**. Type the username as localhost\username, (you could also type **.\azureuser**) enter password you created for the virtual machine, and then click **OK**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal9.png" alt="Screenshot of the Windows security dialogue with use a different account selected and th username azure user entered and a password."></p>


15. You may receive a certificate warning during the sign-in process. Click **Yes** or to create the connection and connect to your deployed VM. You should connect successfully.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal10.png" alt="Screenshot of the Certificate warning dialogue informign the user of an untrusted certificate, with the Yes button highlighted."></p>

Congratulations! You have deployed and connected to a Windows Server virtual machine in Azure

If you wish and have time you could also make the deployed server a functioning web server and make a web page available publicly, by continuing with the following steps 

16. Open up a PowerShell command prompt on the virtual machine, by clicking the **Start** button, typing **PowerShell** right clicking **Windows PowerShell** in the menu and selecting **Run as administrator**

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal11.png" alt="Screenshot of the virtual machine desktop with the start button clicked and powershell selected with run as an administrator highlighted."></p>

17. Install the **Web-Server** feature in the virtual machine by running the following command in the PowerShell command prompt:
PowerShell

    ```PowerShell
    Install-WindowsFeature -name Web-Server -IncludeManagementTools
    ```
   
   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal12.png" alt="Screenshot of the windows powershell command prompt with the command Install-WindowsFeature -name Web-Server -IncludeManagementTools present."></p>

18. When completed you should see a prompt stating **Success** with a value **True**, among other items in the output. You do not need to restart the virtual machine to complete the installation. Close the RDP connection to the VM.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal13.png" alt="Screenshot of the windows powershell command prompt with the command Install-WindowsFeature -name Web-Server -IncludeManagementTools successfully completed and output stating it was successful."></p>

19. Back in the portal, select the VM and in the overview pane of the VM, use the **Click to copy** button to the right of the IP address to copy it and paste it into a browser tab.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal14.png" alt="Screenshot of the Azure portal virtual machine property pane with the IP address copied."></p>

20. The default IIS Web Server welcome page will open, and is available to connect to publicly via this IP address, or via the fully qualified domain name.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal15.png" alt="Screenshot of the default IIS web server welcome page being accessed via the public ip address in a web browser."></p>

Congratulations! You have created a web server that can be connected to publicly via this IP address, or via the fully qualified domain name. If you had a web page to host you could deploy those source files to the virtual machine and host them for public access on the deployed virtual machine.


> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.