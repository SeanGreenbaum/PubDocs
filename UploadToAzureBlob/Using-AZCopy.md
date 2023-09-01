# <span style="color:#548dd4;">**Uploading data using AzCopy**</span>
---

> <span style="color: red">**Important**:</span> You will need to have AzCopy downloaded and extracted. AzCopy is a command line program used to transfer data to and from Azure storage.
Details and download links can be downloaded [here](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10).

Copy AzCopy.exe to a local path that you can access from the command prompt.

![](/.attachments/figure1.PNG)

Place the files you want to upload into a specific folder. In this case, I'll copy my files to a subfolder called "Files to Upload"

![](/.attachments/figure2.PNG)

Next you will need to get the URI for the Azure location you will be uploading the files to. The owner of the Azure Storage account will need to generate a SAS token for you to use. 
> <span style="color: red">**Note**:</span> These SAS tokens look like web URLs. They are not. Attempting to use one in your web browser will not work. These URIs are intended to be used in applications like AzCopy or Azure Storage Explorer; not Chrome, Edge or Firefox. 

An Example SAS token URI will look like this:
https://seandemo.blob.core.windows.net/demouploads?sv=2019-02-02&st=2020-05-22T18%3A22%3A38Z&se=2020-05-23T18%3A22%3A38Z&sr=c&sp=racwl&sig=4zWpJ591w%2BPrKGp7Pl8Qre4ZUdexG3JSdyX58ht1uFk%3D

The AzCopy command to upload a single file to an Azure Storage blob is:
```
AzCopy cp "myfile.txt" "https://destination-azure-storage-URI"
```
![](/.attachments/figure3.PNG)

The AzCopy command to upload a bunch of files to an Azure Storage blob is:
```
AzCopy cp "*.zip" "https://destination-azure-storage-URI"
```
![](/.attachments/figure4.PNG)
