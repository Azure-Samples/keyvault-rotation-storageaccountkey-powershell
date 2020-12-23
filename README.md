# KeyVault-Rotation-StorageAccountKey-PowerShell

Functions regenerate individual key (alternating key1 and key2) in Storage Account and add regenerated key to Key Vault as new version of the same secret.

## Features

This project framework provides the following features:

* Rotation function for storage account key triggered by Event Grid (AKVStorageRotation)

* Rotation function for storage account key triggered by HTTP call (AKVStorageRotationHttp)

* ARM template for function deployment

* ARM template for adding storage account key to existing function

## Getting Started

### Installation

There are 3 ARM templates available
- [Initial Setup (Demo)](https://github.com/Azure-Samples/KeyVault-Rotation-StorageAccountKey-PowerShell/tree/master/ARM-Templates#inital-setup)- Creates Key Vault and Storage Account if needed. Existing Key Vault and Storage Account can be used instead
- [Rotation Azure Function - Setup](https://github.com/Azure-Samples/KeyVault-Rotation-StorageAccountKey-PowerShell/tree/master/ARM-Templates#storage-account-key-rotation-functions) - It creates and deploys function app and function code, creates necessary permissions, and Key 
Vault event subscription for Near Expiry Event for individual secret (secret name can be provided as parameter)
- [Add storage accounts for management to existing Azure Function](https://github.com/Azure-Samples/KeyVault-Rotation-StorageAccountKey-PowerShell/tree/master/ARM-Templates#add-event-subscription-to-existing-functions) - single function can be used for multiple storage accounts. This template adding new event subscription for secret and necessary permissions to access storage account

## Demo

You can find all steps in tutorial below:
[Automate the rotation of a secret for resources that have two sets of authentication credentials](https://docs.microsoft.com/azure/key-vault/secrets/tutorial-rotation-dual)

