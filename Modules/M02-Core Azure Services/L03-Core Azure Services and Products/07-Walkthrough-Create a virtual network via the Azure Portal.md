
In this walkthrough task we will create a virtual network, deploy two virtual machines onto that virtual network and then configure them to allow one virtual machine to ping the other over that virtual network.

You can complete this walkthrough task by completing the steps outlined below, or you can simply read through them, depending on your available time.

### Prerequisites
- You require need an Azure subscription to perform these steps. If you don't have one you can create one by following the steps outlined on the <a href="https://azure.microsoft.com/en-us/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio" target="_blank"><span style="color: #0066cc;" color="#0066cc">Create your Azure free account today</span></a> webpage.


### Steps

1. Sign in to the Azure portal at <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://portal.azure.com</span></a>
2. Choose **Create a resource** in the upper left-hand corner of the Azure portal, then select **Networking**  > **Virtual network**

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal1.png" alt="Screenshot of the Marketplace pane search blade Networkign selected and the  Virtual network highlighted."></p>


3. In the **Create virtual network** pane  above the list of Azure Marketplace resources, search for and select **Windows Server 2016 Datacenter**, then choose **Create**.

   | Setting | Value | 
   | --- | --- |
   | Name | **vnet1** |
   | Address space |**10.1.0.0/16** |
   | Subscription | < Select your subscription > |
   | Resource group | Select **Create new**, enter **vnet1-rg1**, then select **OK**. |
   | Location | **East US** |
   | Subnet - Name | **subnet1** |
   | Subnet Address range | **10.1.0.0/24** |

   Leave the rest of the settings at their default values and select **Create**.


   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal2.png" alt="Screenshot of the Create virtual network pane with fields and settings filled in and the create button highlighted."></p>

4. Verify the creation of the virtual network by going to the newly created resource group and viewing the virtual network is present, you can click on the virtual network and view its properties if you wish.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal3.png" alt="Screenshot of the resource group just created containing the virtual network that has just been created."></p>

5. Create a virtual machine by going to the the upper-left side of the Azure Portal and selecting **Create a resource** > **Compute** > **Windows Server 2016 Datacenter**

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal1a.png" alt="Screenshot of the Marketplace pane search blade with windows server 2016 datacenter entered,  returned in a list of matches and highlighted."></p>

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal1b.png" alt="Screenshot of the Windows Server 2016 datadenter resource object blade and the button create highlighted."></p>

6. In Create a **virtual machine** - **Basics** tab, enter or select this information:

   | Setting | Value | 
   | --- | --- |
   | Subscription | < Select your subscription >  |
   | Resource group | The resource group you created it in the last section, i.e. **vnet1-rg1** |
   | Virtual machine name | **vm1**|
   | Region | **East US** |
   | Availability options | Leave the default **No infrastructure redundancy required** |
   | Image | Leave the default **Windows Server 2016 Datacenter** |
   | Size | Leave the default **Standard DS1 v2** |
   | Username| **azureuser** |
   | Password| enter a password that meets the complexity requirements. |
   | Public inbound ports| Select **Allow selected ports**  |
   | Selected inbound ports| Select **HTTP**, **HTTPS**, **SSH** and **RDP** |

7. Select **Next** : **Disks**, leave the default values.

8. Select **Next** : **Networking**, complete the following details

   | Setting | Value | 
   | --- | --- |
   | Virtual network | Leave the default **vnet1** |
   | Subnet | Leave the default **subnet1 (10.1.0.0/24)** |
   | Public IP | Leave the default (new) **vm1-ip** |
   | NIC network security group | accept the default **Basic**|
   | Public inbound ports| Select **Allow selected ports**  |
   | Select inbound ports  |  Select **HTTP**, **HTTPS**, **SSH** and **RDP** |

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal6.png" alt="Screenshot of the create a virtual machine pane on the Network Interface section with fields filled in as per the table in the steps."></p>

9. Select **Next** : **Management**, accept all the defaut values except for the below settings:

   | Setting | Value | 
   | --- | --- |
   | Boot diagnostics | accept the default value i.e. **On** |
   | Diagnostic storage account | accept the default value i.e. **vnet1rgdiag** |

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal7.png" alt="Screenshot of the create a virtual machine pane on the Management tab with fields filled in as per the table in the steps."></p>

10. Select **Review** + **create**. Azure will validate the configuration. When you see that Validation passed, select **Create**. Deployment times can vary but it can generally take between three to six minutes to deploy.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal8.png" alt="Screenshot of create a virtual machine pane on the validation passed blade with the validation passed message highlighted and the Create button highlighted."></p>

11. Create a second Virtual machine by repeating steps **5 to 9** above, using the same values above above ensuring the below settings are set:

   | Setting | Value |
   | --- | --- |
   | Virtual machine name |  **vm2** |
   | Public IP | Leave the default (new) **vm2-ip** |
   | Diagnostic storage account | Leave the default value i.e. **vnet1rg1diag** |

12. When finished filling in the details, validate the configuration by clicking **Review + create** and once successfully validated click **Create**

13. When both virtual machine have completed deployment connect to the first virtual machine, **vm1**, by going to the resource group you placed the virtual machine in, **vnet-rg1** and open up the virtual machine, then click the **Connect** button on the virtual machine properties page.


   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal9.png" alt="Screenshot of the virtual machine properties with the resource groups, vm name and Connect button highlighted."></p>


> **Note**: The following directions tell you how to connect to your VM from a Windows computer. On a Mac, you need an RDP client such as this Remote Desktop Client from the Mac App Store and on Linux virtual machine you could connect directly from a bash shell using `ssh`.

14. In the **Connect to virtual machine** page, keep the default options to connect by DNS name over port 3389 and click **Download RDP File**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal7.png" alt="Screenshot of the Connect to virtual machine pane with the download rdp file button highlighted"></p>

15. Open the downloaded RDP file and click **Connect** when prompted. 

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal8.png" alt="Screenshot of the virtual machine properties with the Connect button highlighted"></p>

16. In the **Windows Security** window, select **More choices** and then **Use a different account**. Type the username as localhost\username, (you could also type **.\azureuser**) enter password you created for the virtual machine, and then click **OK**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal9.png" alt="Screenshot of the Windows security dialogue with use a different account selected and th username azure user entered and a password."></p>


17. You may receive a certificate warning during the sign-in process. Click **Yes** or to create the connection and connect to your deployed VM. You should connect successfully.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal10.png" alt="Screenshot of the Certificate warning dialogue informign the user of an untrusted certificate, with the Yes button highlighted."></p>

18. Open up a PowerShell command prompt on the virtual machine, by clicking the **Start** button, typing **PowerShell** right clicking **Windows PowerShell** in the menu and selecting **Run as administrator**

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvmportal11.png" alt="Screenshot of the virtual machine desktop with the start button clicked and powershell selected with run as an administrator highlighted."></p>
19. Run the command

   ```PowerShell
   ping vm2
   ```
   You receive an error, saying request timed out.  The `ping` fails, because `ping` uses the **Internet Control Message Protocol (ICMP)**. By default, ICMP isn't allowed through the Windows firewall.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal10.png" alt="Screenshot of PowerShell command prompt with the command ping vm2 after been run and the output indicating the command wasn't successful."></p>

20. To allow *vm2* to ping *vm1* enter the  below command. This command allows ICMP inbound through the Windows firewall:

   ```PowerShell
   New-NetFirewallRule –DisplayName “Allow ICMPv4-In” –Protocol ICMPv4
   ```
   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal11.png" alt="Screenshot of PowerShell command prompt with the command New-NetFirewallRule –DisplayName “Allow ICMPv4-In” –Protocol ICMPv4 after been run and the output indicating the command was successful."></p>

21. Connect to *VM2* as has been done for *VM1*, using rdp. i.e. open **vm2** properties and click the **Connect** button to download and then connect vis RDP

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal12.png" alt="Screenshot of the virtual machine VM2 properties with the Connect button highlighted."></p>

22. Open up a PowerShell command prompt on the virtual machine, VM2, and run the command:

   ```PowerShell
   ping vm1
   ```
   You should now be able to ping the vm1 virtual machine successfully, because ICMP has been configured to be allowed through the Windows firewall on the *vm1* virtual machine in an earlier step.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createvnetportal13.png" alt="Screenshot of PowerShell command prompt with the command ping vm1 after been run and the output indicating the command was successful."></p>

Congratualations! This ping is being done using the *virtual network* you created and deployed the two virtual machines into. The two virtual machines are communicating over this *virtual network* that was created.

> **Note**: Remember to delete the resources you have just deployed if you are no longer using them to ensure you do not incur costs for running resources. You can delete all deployed resources by deleting the resource group in which they all reside.