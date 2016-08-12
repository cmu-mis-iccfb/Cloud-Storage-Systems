# Homework User Story

## User Story
As an instructor, I want to you to implement an image storage using Azure
Storage so you can get experience reading and writing from a cloud storage
system.

## Acceptance Criteria
* I should receive a single email per team
* The email should contain the name of the individuals on your team
* The email should contain a link to your Github repository
* The email should contain a link to your running application
* I should see the image gallery after entering my credentials

# Azure
Azure is Microsoft's cloud service.  Sign up for a free account -

https://azure.microsoft.com/en-us/free/

## Azure Storage
Once you have created an account, sign into the dashboard and setup Azure
Storage

https://portal.azure.com

You can read more about Azure Storage here -

https://azure.microsoft.com/en-us/documentation/articles/storage-introduction/

Once you have setup your storage account, create a container that will contain
the uploaded images.

## Configuring the Image Gallery Application
You will need to add three configuration parameters to you application.  These
parameters must end up in the application.properties file

* cloud.azure.credentials.accountName
    * The name you set when creating the storage account
* cloud.azure.credentials.accountKey
    * Must be kept secret
    * See the "Manage you storage access keys"
        * https://azure.microsoft.com/en-us/documentation/articles/storage-create-storage-account/
* cloud.azure.storage.container
    * The container name that will hold your images


## Implementing the Image Service
Implement an image service that will handle image uploading, listing and reading from Azure.

See the following for more information on the Azure Java API -

https://github.com/Azure/azure-storage-java

https://azure.microsoft.com/en-us/documentation/articles/storage-java-how-to-use-blob-storage/

You can reference the ImageServiceS3Impl when creating the Azure based image service.

Note, you will need to disable the ImageServiceS3Impl by commenting out the @service decorator.
