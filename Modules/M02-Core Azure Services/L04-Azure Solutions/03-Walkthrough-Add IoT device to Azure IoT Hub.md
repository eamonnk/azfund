In this walkthrough you set up a new Azure IoT Hub in Azure Portal, and configure the hub to authenticate a connection to an IoT device using the [online Raspberry Pi device simulator](https://azure-samples.github.io/raspberry-pi-web-simulator/#Getstarted). Sensor data and messages are passed from the Raspberry Pi simulator to your Azure IoT Hub, and you view metrics for the messaging activity in Azure Portal.

Finish this walkthrough by completing the steps that follow, or by reading through them.

### Prerequisites

An active Azure subscription is required. If you do not have an Azure subscription, create a <a href="https://azure.microsoft.com/free/" target="_blank"><span style="color: #0066cc;">free Azure account</span></a> before you begin.

### Steps

1. To create a new Azure IoT Hub, select the **Deploy to Azure** button. Sign into Azure Portal, when prompted.

	<a href="https://portal.azure.com/#create/microsoft.iothub" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/></a>
	<a href="http://armviz.io/#/?load=https%3A%2F%2Fportal.azure.com%2F%23create%2Fmicrosoft.iothub" target="_blank"><img src="http://armviz.io/visualizebutton.png"/></a>

2. Fill in the fields with the following details.

	- **Subscription**: Select the subscription to use for your new Azure IoT Hub.
	- **Resource Group**: Choose **Create new** and provide a name for the resource group.
	- **Region**: Select the Azure region that is closest to your location from the dropdown list.
	- **IoT Hub Name**: Put in a name for your Azure IoT Hub. This name must be unique to your chosen region. If the name you enter is available, a green check mark appears.
	- Select the **Next: Size and scale** button to continue.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-02-hub-basics.png" alt="Screenshot of basic tab, within the setup new IoT hub blade, in Azure portal. The required data entry fields are filled in. The data entry fields and next button are highlighted to indicate their position on screen."></p>

3. On the **Size and scale** tab, use the dropdown list to set the **Pricing and scale tier** to `F1 - Free tier`.
	- Leave all other options set to their defaults.
	- Select the **Review + create** button at the bottom.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-03-hub-size.png" alt="Screenshot of the size and scale tab, within the setup new IoT hub blade, in Azure portal. The free tier is selected from the dropdown list and highlighted, together with the review + create button, to indicate their positions on screen."></p>

4. Review your choices on the **Review + create** tab, then select the **Create** button to begin creating your new Azure IoT Hub.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-04-hub-review.png" alt="Screenshot of the review + create tab, within the setup new IoT hub blade, in Azure portal. Details about the new IoT hub are shown. The review + create tab is highlighted to indicate how to access the tab. The highlighted create button indicates its position on screen."></p>

> **Note**: When the deployment starts, a notification appears in Azure Portal indicating the deployment is in progress. Another notification is displayed when the deployment has completed successfully.

5. When the deployment has completed, choose **Go to resource** from the notification area to open the Azure IoT Hub **Overview** blade. You can also select **All resources** from the main menu, then choose your Azure IoT Hub from the list of resources.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-05-notify.png" alt="Screenshot of the deployment in progress and deployment succeeded notifications in Azure portal."></p>

6. To add a a new IoT device, select **IoT Devices** from the **IoT Hub navigation** blade. Then, choose the **+ Add** button.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-06-add-device.png" alt="Screenshot of the IoT devices pane, highlighted within the IoT hub navigation blade, in Azure portal. The add button is highlighted to illustrate how to add a new IoT device identity to IoT hub."></p>

7. Provide a name for your new IoT device, for example `myDeviceId`, and select the **Save** button. This will create a new IoT device identity in your Azure IoT Hub.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-07-create-device.png" alt="Screenshot of the create a device blade, within the IoT devices pane, in Azure portal. The device id text entry field is filled in and highlighted to indicate how to add an id to a new IoT device. The save button is highlighted to indicate how to save the device id."></p>

8. After the new device is created, select the new device from the list of IoT devices in the **IoT devices** pane. Copy the **Connection string---primary key** value. You will use this key in Step 10 to authenticate a connection to a Raspberry Pi device.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-08-copy-string.png" alt="Screenshot of the device details blade, within the IoT devices pane, in Azure portal. The connection string primary key field is highlighted to indicate how to copy the key."></p>

9. In a web browser, open the [online Raspberry Pi simulator](https://azure-samples.github.io/raspberry-pi-web-simulator/#Getstarted). Select "**X**" to close the **Overview of Raspberry Pi Simulator** window or choose **Next** to step through the guide.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-09-pi-sim.png" alt="Screenshot of the online overview of Raspberry Pi simulator window. The close window icon and next button are highlighted to indicate how to close the window or progress through the guide."></p>

10. In the coding area, make sure that you are working on the default, Microsoft sample code. Replace the placeholder code on `Line 15` with the Azure IoT Hub connection string value that you copied from Step 8.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-10-paste-string.png" alt="Screenshot of the coding area within the Raspberry Pi simulator. Line 15 is shown to indicate where to paste the connection string primary key value."></p>

11. Select **Run** or type `npm start` to run the application. The console output should show the sensor data and messages that are sent from the Raspberry Pi simulator to your Azure IoT Hub. Data and messages are sent each time the Raspberry Pi simulator LED flashes. Select **Stop** to stop sending data.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-11-run-app.png" alt="Screenshot of the Raspberry Pi simulator console.  The console output shows sensor data and messages sent from the Raspberry Pi simulator to Azure IoT Hub."></p>

12. To view metrics for the messaging activity in Azure Portal, select **All resources** from the main menu. Choose your Azure IoT Hub from the list of resources. Scroll down to the **IoT Hub Usage** pane of the **IoT Hub Overview** blade. To access these metrics from the **IoT Hub navigation** blade, select **Metrics** from the **Monitoring** section.

<p style="text-align:center;"><img src="../Linked_Image_Files/m02-l04-iot-12-msg-metrics.png" alt="Screenshot of metrics within the IoT hub usage area of Azure portal. Azure navigation menu items are highlighted to indicate how to access the IoT hub usage pane. A highlighted graph, within the metrics pane, illustrates monitored messaging activity between the Raspberry Pi simulator and Azure IoT hub."></p>

Congratulations! You have set up Azure IoT Hub to collect sensor data from an IoT device.

> **Note**: Remember to remove any newly created Azure resources that you no longer use. Removing unused resources ensures you will not incur unexpected costs. Remove unused resources by deleting the Resource Group that the unused resources belong to.