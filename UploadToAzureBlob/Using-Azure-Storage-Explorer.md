# <span style="color:#548dd4;">**Uploading data using Azure Storage Explorer**</span>
---

> <span style="color: red">**Important**:</span> You will need to have Azure Storage Explorer downloaded and installed on your local machine. This may require admin permissions to complete. Azure Storage Explorer is a graphical view of Azure storage you have access to. Azure Storage Explorer documentation and download information can be found [here](https://docs.microsoft.com/en-us/azure/vs-azure-tools-storage-manage-with-storage-explorer?tabs=windows).

> <span style="color: red">**Note**:</span> The owner of the Azure storage will need to generate a SAS token for you. These SAS tokens look like web URLs. They are not. Attempting to use one in your web browser will not work. These URIs are intended to be used in applications like AzCopy or Azure Storage Explorer; not Chrome, Edge or Firefox. 

After installing Azure Storage Explorer, run it from the Start Menu. 
1. Once Azure Storage Explorer opens, on the Left hand side expand "Local & Attached"

 ![image.png](/.attachments/image-45bf7bde-b618-4c46-a6e9-7c09c74b418a.png)

2. Right click on "Storage Accounts" and select "Connect to Azure Storage"

![image.png](/.attachments/image-c75446b6-35e6-4136-ac5a-94fdd645c5a0.png)

3. In the "Connect to Azure Storage" window, select "Blob Container"

![image.png](/.attachments/image-fff23401-a9ab-4128-8e4c-2f444ec8bed8.png)

4. On the Select Connection Method screen, select "Shared access Signature URL (SAS)".

![image.png](/.attachments/image-97e152dc-6548-4f74-9e90-04186089c09a.png)

5. Enter a friendly name for the Display Name. In the Blob container SAS URL field, enter the URL that was provided to you.

![image.png](/.attachments/image-fa22f77f-5e57-4973-a064-d806b7e599c3.png)

6. On the Summary page, review the overview and click Connect.

![image.png](/.attachments/image-f11b2237-fc7c-4032-9228-45c54dc9dedc.png)

Once connected, the Blob container will show in the list, displayed by the Friendly name you selected in step 5.

![image.png](/.attachments/image-a19a22e5-4aeb-4359-9f02-d461978f83dd.png)

From here, you can simply Drag and Drop the files into the container, or use the Upload button on the toolbar to complete the upload.

![image.png](/.attachments/image-df3ac48c-a17a-4957-8e75-624d0fa14532.png)

Once all files are uploaded, and you no longer need the Azure Storage connected, Right click on it and select Detach

![image.png](/.attachments/image-4967619c-af71-4882-93d2-f4199705746f.png)

