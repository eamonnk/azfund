
In this walkthrough task we will create a storage account, then create a blob storage container within that storage account, then upload a block blob, view and edit the blob file within the blob container in Azure, and then download the block blob file.

You can complete this walkthrough task by completing the steps outlined below, or you can simply read through them, depending on your available time.

### Prerequisites
- You require need an Azure subscription to perform these steps. If you don't have one you can create one by following the steps outlined on the <a href="https://azure.microsoft.com/en-us/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio" target="_blank"><span style="color: #0066cc;" color="#0066cc">Create your Azure free account today</span></a> webpage.


### Steps

1. Sign in to the Azure portal at <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://portal.azure.com</span></a>

2. Select **All services** on the upper left hand side of the Azure Portal. In the **All services** filter box, type **Storage Accounts**. As you begin typing, the list filters based on your input. Select **Storage Accounts**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal1.png" alt="Screenshot of the Create virtual network pane with fields and settings filled in and the create button highlighted."></p>


3. On the **Storage Accounts** window that appears, if there are no storage accounts present you can select **Create storage account**, or if there are already storage accounts present, this option will nt be present and you can choose the option **+ Add**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal2.png" alt="Screenshot of the Storage accounts pane with the + Add option and Create storage account options highlighted."></p>

4. Complete the Create storage account blade with the following details


    | Setting | Value | 
    | --- | --- |
    | Subscription | < Select your subscription > |
    | Resource group | Select **Create new**, enter **strac-rg1**, then select **OK**. |
    | Storage account name | < this must be be between 3-24 characters in length, can be numbers and lowercase only, and must be unique across Azure > |
    | Location | **East US**  |
    | Performance | **Standard** |
    | Account kind | Leave the default value **StorageV2 (general purpose v2)*** |
    | Replication | **Locally redundant storage (LRS)** |
    | Access tier (default) | **Hot** |

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal3.png" alt="Screenshot of the Create storage account pane on the Basics tab with the fields filled in as per the table."></p>

5. Select **Review + Create** to review your storage account settings and allow Azure to validate the configuration. Once validated select **Create**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal4.png" alt="Screenshot of the Create storage account pane after the configuration has been successfulyl validated with the Create button highlighted."></p>

6. Verify its successful creation by going to the resource group just created and locate the storage account.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal5.png" alt="Screenshot of the newly created storage account in the Azure portal ."></p>

7. Open the storage account and scroll in the left menu for the storage account, scroll to the **Blob** service section, select **Blobs** and then select the **+ Container** button.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal6.png" alt="Screenshot of the storage account properties in the blo section with Blobs selected and then the + containers option highlighted."></p>

8. Configure the blob container as belwo and select OK when complete to create the blob container.


    | Setting | Value |
    | --- | --- |
    | Name | i.e. **blob1** The container name must be lowercase, must start with a letter or number, and can include only letters, numbers, and the dash (-) character. |
    | public access level| leave the default value i.e. The default level is **Private (no anonymous access)** |

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal7.png" alt="Screenshot of the new container pane with name and public access slevel fields filled in."></p>

9. The container should be created and available

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal8.png" alt="Screenshot of the newly created blob container in the storage account in the Azure portal."></p>

10. We will upload a block blob to your new container. Select the container to show a list of blobs it contains. Since this container is new, it won't yet contain any blobs


   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal9.png" alt="Screenshot of the newly created blob container with no items uploaded ot it and a message stating no blobs found present."></p>

> **Note**: Block blobs consist of blocks of data assembled to make a blob. Most scenarios using Blob storage employ block blobs. Block blobs are ideal for storing text and binary data in the cloud, like files, images, and videos. 

11. Create a `.txt` file on your local machine, named **blob1.txt**, and enter some text into it, such as `this is a blob file` or something like that.

12. Select the **Upload** button to upload a blob to the container. Browse your local file system to find the file you created in the previous steps to upload as a block blob, Click on the **Advanced** arrow, leave the default values as they are, just note them, and then select **Upload**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal10.png" alt="Screenshot of the Upload blob pane with the blob1.txt file uploaded, the advanced settings expanded and the Upload button highlighted."></p>


 > **Note**: You can upload as many blobs as you like in this way. You'll see that the new blobs are now listed within the container.

13. View the uploaded block blob by right clicking on the blob file that was uploaded and selecting **View/edit blob**

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal11.png" alt="Screenshot of the Uploaded blob with the right click context menu and the items View/edit and Download highlighted."></p>


   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal12.png" alt="Screenshot of the Uploaded blob and the content within it in an edit pane."></p>


14. You can download a block blob by right clicking on the block blob and selecting **Download**. The blob file opens in a browser and is then downloadable by right clicking on the file and selecting save as

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createblobportal13.png" alt="Screenshot of the Uploaded blob opened up in a browser where the content is visible."></p>


Congratulations! You have created a storage account, created a blob storage container within that storage account, then uploaded a block bob, viewed and edited the block blob in the blob container and then downloaded the block blob.

> **Note**: Remember to delete the resources you have just deployed if you are no longer using them to ensure you do not incur costs for running resources. You can delete all deployed resources by deleting the resource group in which they all reside.