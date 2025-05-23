# Azure ARM Templates

The templates in this folder allow you to quickly create all of the necessary Azure resources to use the majority of TypeAgent features. Please follow [these instructions](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-portal) to deploy these ARM templates.

## Quickstart

To deploy these resources in your Azure subscription into a resource group called _typeagent_demo_ run the following command either in the cloud shell or from an AzureCLI:

`az deployment group create --resource-group typeagent_demo --template-file template.json`

## Features Not Covered

The following TypeAgent features/components are not automatically created or configured by these ARM templates:

- Demo Tenant for [Calendar](../ts/packages/agents/calendar) & [Email](../ts/packages/agents/email/) agents
- Permissions Assignment
- Identity Management
- Populating Key values in KeyVault (see [getKeys](../ts/tools/scripts/getKeys.mjs) script)
- [Docker](../ts/Dockerfile) endpoint app service
