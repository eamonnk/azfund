
In this walkthrough task we will create a SQL database in Azure and then query the data in that database.

You can complete this walkthrough task by completing the steps outlined below, or you can simply read through them, depending on your available time.

### Prerequisites
- You require need an Azure subscription to perform these steps. If you don't have one you can create one by following the steps outlined on the <a href="https://azure.microsoft.com/en-us/free/?ref=microsoft.com&utm_source=microsoft.com&utm_medium=docs&utm_campaign=visualstudio" target="_blank"><span style="color: #0066cc;" color="#0066cc">Create your Azure free account today</span></a> webpage.


### Steps

1. Sign in to the Azure portal at <a href="https://portal.azure.com" target="_blank"><span style="color: #0066cc;" color="#0066cc">https://portal.azure.com</span></a>

2. Select **Create a resource** on the upper left hand side of the Azure Portal. Select **Databases** > **SQL Databases** and in the **SQL Database** pane fill in the fields as per the below table, and then click **Server**


    | Setting | Value | 
    | --- | --- |
    | Database name| **db1** | 
    | Subscription | < Select your subscription > |
    | Resource group | Select **Create new**, enter **sqldb1-rg1**, then select **OK**. |
    | Select source | Select **Sample AdventureWorksLT** |

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb1.png" alt="Screenshot of the Create virtual network pane with fields and settings filled in and the create button highlighted."></p>

3. In the **Server** pane, choose **Create a new server** and complete the New server pane using below details and click **Select** when finished.

    | Setting | Value | 
    | --- | --- |
    | Server name | < this needs to be a unique name > | 
    | Server admin login | **azureuser** |
    | Password | Enter a password that meets the complexity requirements. |
    | Location | **East US** |


   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb2.png" alt="Screenshot of the Server pane and the New Server pane with fields fille din as per the table and the Select button highlighted."></p>

4. On the **Storage Accounts** window that appears, if there are no storage accounts present you can select **Create storage account**, or if there are already storage accounts present, this option will nt be present and you can choose the option **+ Add**.

   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb2.png" alt="Screenshot of the Create virtual network pane with fields and settings filled in and the create button highlighted."></p>


5. On the **SQL Database** pane , select **Pricing tier**. Explore the amount of *DTUs* and *storage* available for each service tier.


   <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb3.png" alt="Screenshot of the database pricing tier configuration pane."></p>


> **Note**: This database uses the DTU-based purchasing model, but there is another, the vCore-based purchasing model, which is also available.  

6. Select the **Standard** service tier, and then use the slider to select **10 DTUs** (S0) and **1 GB** of storage and select **Apply**. 
   
    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb4.png" alt="Screenshot of the Pricing Tier configuration pane."></p>

7. Click **Create** to deploy and provision the resource group, server, and database. It can take approx 2 to 5 minutes to deploy.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb5.png" alt="Screenshot of the Create virtual network pane with fields and settings filled in and the create button highlighted and the Create button highlighted."></p>

8. Once complete verify the successful deployment by going to the resource group you just created in the Azure Portal and verifying the presence of the server and database. 

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb6.png" alt="Screenshot of the sql database and server that have just been deployed."></p>

9. Open the SQL database you crated **db1**, go to the  **Query Editor (preview)** in the left hand pane, and enter the login details and password. then click **OK**


    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb7.png" alt="Screenshot of the database db1 on the Query Editor pane and login and password details displaying with the OK button Highlighted."></p>

10. Once you log in successfully the query pane appears, enter the following query into the editor pane

    ```SQL
    SELECT TOP 20 pc.Name as CategoryName, p.name as ProductName
    FROM SalesLT.ProductCategory pc
    JOIN SalesLT.Product p
    ON pc.productcategoryid = p.productcategoryid;
    ```

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb8.png" alt="Screenshot of the database query editor in Azure portal with the above SQl code entered into the query editor."></p>

11. Select *Run**, and then review the query results in the **Results** pane. The query should run successfully.

    <p style="text-align:center;"><img src="../Linked_Image_Files/walkthrough-createdb9.png" alt="Screenshot of the database Query Editor pane with the SQl code having been rnu successfully and the output visible in the results pane."></p>

Congratulations! You have created a SQL database in Azure and successfully queried the data in that database.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.