This is a simple ETL project.
I have Olympics data that I have put on somewhere from which it got easy to extract. That's why I uploaded it on my github repository.
Now, I setup my Azure account and services that are used in this project implementation. e.g,
1. ResourseGroup : Its nothing but like a container/folder in which all your softwares that often being used, are in their.
2. StorageAccount : Its being used to store data in raw(unstructured) format and also in transformed(structured) format.
3. AzureDataFactory : Its being used to extraxt data from my github repository and load it to my storage db. I used HTTP protocol connection type to connect to my github repository
                      through AzureDataFactory and then sink/load that data to the storage layer (AzureDataLakeStorageGen2) in same format as it is in.
4. AzureDataBricks : Its being used to transform the data and the load that data again in storage layer (AzureDataLakeStorageGen2). To connect AzureDataBricks to AzureDataLakeStorageGen2,
                     you have to mount(give access) your AzureDataLakeStorageGen2 folder to AzureDataBricks.And one more step is that after mount, you also have to allow connection 
                     to AzureDataBricks and you can do this by registering an app and defining your rules in that app to do that.
5. AzureSynapse : Its being used to perform some analytics on top of Olympics data.
