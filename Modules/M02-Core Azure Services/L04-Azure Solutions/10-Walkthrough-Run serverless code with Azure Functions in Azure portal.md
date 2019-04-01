In this walkthrough you write and run serverless code inside an *Azure Function App* in Azure portal.

Finish this walkthrough by completing the steps that follow, or by reading through them.

### Prerequisites

An active Azure subscription is required. If you do not have an Azure subscription, create a <a href="https://azure.microsoft.com/free/" target="_blank"><span style="color: #0066cc;">free Azure account</span></a> before you begin.

### Steps

1. To create a new Azure Function App, select the **Deploy to Azure** button. Sign into Azure Portal, when prompted.

    <a href="https://portal.azure.com/#create/Microsoft.FunctionApp" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>
    <a href="http://armviz.io/#/?load=https%3A%2F%2Fportal.azure.com%2F%23create%2FMicrosoft.FunctionApp" target="_blank"><img src="http://armviz.io/visualizebutton.png"/></a>

2. Fill in the Azure Function App settings fields with the following details.

    - **App name**: Provide a unique name that identifies your new Function App.
    - **Subscription**: Select an Azure subscription for your Function App.
    - **Resource Group**: Choose **Create new**. Provide a unique name for your new Resource Group, if Azure has not provided a name automatically.
    - **OS**: Select `Windows`. For Linux hosting, see <a href="https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-first-azure-function-azure-cli-linux" target="_blank"><span style="color: #0066cc;">Create your first function running on Linux using the Azure CLI</span></a>.
    - **Hosting plan**: Choose `Consumption plan`. With Azure serverless hosting, you only pay for the time that your functions run. Using the default **Consumption Plan** means that resources are added dynamically as required by your functions.
    - **Location**: Choose the Azure region that is closest to your location.
    - **Runtime stack**: Select `.NET` (this is suitable for running C# and F# functions).
    - **Storage**: Choose **Create new**. Provide a unique name for your new storage account, if Azure has not provided a name automatically.
    - **Application Insights**: Leave this set to the default value, provided by Azure automatically.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-02-app-create.png" alt="Screenshot of the create function app blade in Azure portal. Sample settings are provided in the function app settings fields. The settings fields and create button are highlighted to illustrate how to complete the create function app process."></p>

3. Select the **Create** button to begin provisioning and deploying your new Azure Function App.

> **Note**: When the deployment starts, a notification appears in Azure Portal indicating the deployment is in progress. Another notification is displayed when the deployment has completed successfully.

4. When the deployment has completed, choose **Go to resource** from the notification area to view your new Azure Function App. You can also select **All resources** from the main Azure menu, then choose your Azure Function App from the list of resources.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-04-notify.png" alt="Screenshot of the deployment in progress and deployment succeeded notifications in Azure portal. The go to resource button is highlighted to illustrate how to access the newly created function app from the deployment succeeded notification."></p>

5. To create an *HTTP Triggered Function*, use the down arrow icon to expand your Azure Function App. Select the "**+**" button next to **Functions**. Choose **In-portal**, and select **Continue**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-05-choose-portal.png" alt="Screenshot of the choose a development environment step in the azure functions for dot net getting started pane inside Azure portal. The display elements for creating a new in-portal function are highlighted. The highlighted elements are expand the function app, add new function, in-portal, and the continue button."></p>

6. Choose **WebHook + API**, and then select **Create**.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-06-add-webhook.png" alt="Screenshot of the create a function step in the azure functions for dot net getting started pane inside Azure portal. The webhook + api button and create button are highlighted to illustrate the display elements used to add a new webhook to an Azure function."></p>

7. Select **</> Get function URL** from the within the function editor. Set the **Key** value to `default (Function key)` using the dropdown. Then, select **Copy** to copy the function URL.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-07-test-function.png" alt="Screenshot of the get function URL pane inside the function editor in Azure portal. The display elements get function URL button, set key dropdown, and copy URL button are highlighted to indicate how to obtain and copy the function URL from the function editor."></p>

8. Paste the copied function URL into your web browser's address bar. Append `&name=<yourname>` to the end of the URL. **Note**: Here, `<yourname>` refers to your given name. Navigate to the URL to see the "Hello" message, followed by the name you provided, displayed in your browser.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-08-browser-function.png" alt="Screenshot of a highlighted function URL and an appended example user name in the address bar of a web browser. The hello message and user name are also highlighted to illustrate the output of the function in the main browser window."></p>

9. When your function runs, trace information is written to log files in Azure. To view the logs in Azure portal, return to the function editor, and select the **Logs** button.

    <p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-functions-09-view-logs.png" alt="Screenshot of a trace information log resulting from running the function inside the function editor in Azure portal. The logs button for accessing the trace information and some of the log content are highlighted to indicate how to access and read a trace information log from the function editor."></p>

Congratulations! You have written and run serverless code inside an Azure Function App, in Azure portal, successfully.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.