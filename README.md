# Azure Blob Storage Quickstart:
This repository demonstrates how to interact with Azure Blob Storage using C# and the Azure SDK. The code in this example performs basic operations, including creating a blob container, uploading and downloading blobs, and listing blobs in a container. It also demonstrates authentication with Azure using the DefaultAzureCredential class, allowing for secure, passwordless access to Azure resources.

Prerequisites:
.NET SDK (v6.0 or later)
Azure Storage Account with Blob Storage enabled
Azure CLI for account setup and resource management (optional)
Azure Identity Setup: Ensure you have appropriate permissions on the Azure Storage Account for passwordless authentication.

Clone the repository:
git clone https://github.com/Wolverine3369/Blob-Passwordless.git
cd yourrepository

Install Dependencies: This project relies on the Azure.Storage.Blobs and Azure.Identity packages. Run the following commands in the project directory:
dotnet add package Azure.Storage.Blobs
dotnet add package Azure.Identity

Update Configuration:
Replace <storage-account-name> in the code with your actual storage account name.
Ensure you have configured your Azure environment to support DefaultAzureCredential. This could be through an Azure service principal or user account with access to the storage account.

The sample code performs the following steps:
Authenticate using DefaultAzureCredential, which allows for flexible authentication in various environments (e.g., Azure VM, local development, or Azure Function).
Create a Blob Container dynamically with a unique name.
Upload a Text File to the container.
List Blobs in the container.
Download the Blob to a local file.
Clean Up resources by deleting the container and local files.

Run the Application: Execute the application with:
dotnet run

Expected Output: The application will:
Create and upload a blob to Azure Blob Storage.
List the blob in the console output.
Download the blob back to a local file.
Delete the created container and files after execution.

Customize: You can modify containerName, fileName, or the file contents in localFilePath to explore additional use cases.

Notes:
Ensure that your Azure account and Storage Account have proper permissions set for DefaultAzureCredential to work.
The code includes clean-up steps to delete created resources after execution. To keep the uploaded blobs, comment out the cleanup section at the end of the code.

References:
Azure SDK for .NET Documentation
Azure Storage Blobs Documentation

License:
This project is licensed under the MIT License. See LICENSE for details.
