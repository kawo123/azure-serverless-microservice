# Azure Serverless Microservice [WIP]

Azure serverless demo highlighting key functionalities of Azure Functions, API Managements, and Logic App.

## Pre-requisite

- [Postman](https://www.getpostman.com/downloads/)
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
- [VS Code](https://code.visualstudio.com/download)
  - [VS Code: Azure Function Tutorial](https://code.visualstudio.com/tutorials/functions-extension/getting-started)

## Getting Started

- Clone the repository

- Complete authorization of API connections for Logic App workflow
  - For each API connection resource, navigate to the API connection resource -> "Edit API Connection" -> press "Authorize" button and follow authorization flow OR enter necessary information

<!-- - To leverage GitHub Actions to continuous integrate & deploy Azure Functions, you have to add application settings to Azure Functions before deployment
  - Under Azure Functions application settings (navigate to "Azure Function resource" -> "Configuration"), create a new connection string entry with key `CosmosDBConnection`
  -  -->

- To configure GitHub Actions to continuous integrate & deploy to Azure Functions, take the below steps
  - In `.github/workflows/az_func_py_wf.yaml`, replace `app-name: <<TODO>>` (line 53) with `app-name: {Azure Function App Name}`
  - Follow the steps under the section "[Using Publish Profile as Deployment Credential](https://github.com/marketplace/actions/azure-functions-action#using-publish-profile-as-deployment-credential)"

- You can use Postman to test the solution
  - TODO

---

- For local development, use [Azure Functions Core Tools](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=linux) to test Azure Functions locally

- In `functions/`,
  - Run `func extensions install` to install Azure Functions extensions required to run the demo. This may require installation of other dependencies such as `dotnet`

## Considerations

- To use linked template, you can only provide a URI value that includes either http or https ([ref](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/linked-templates#linked-template)). You can't specify a local file or a file that is only available on your local network.

- Although the linked template must be externally available, it doesn't need to be generally available to the public. You can add your template to a private storage account that is accessible to only the storage account owner. Then, you create a shared access signature (SAS) token to enable access during deployment ([ref](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/linked-templates#securing-an-external-template)).

- Use type `securestring` for secrets, keys, and connection strings

- Instead of putting a secure value (like a password) directly in your template or parameter file, you can retrieve the value from an Azure Key Vault during a deployment. You retrieve the value by referencing the key vault and secret in your parameter file. The value is never exposed because you only reference its key vault ID ([ref](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/key-vault-parameter?tabs=azure-cli)).

## References

- [Azure Functions Python developer guide](https://docs.microsoft.com/en-us/azure/azure-functions/functions-reference-python)
- [Azure Functions Python samples](https://github.com/yokawasa/azure-functions-python-samples/blob/master/v2functions/cosmos-trigger-cosmodb-output-binding/__init__.py)
- [Azure Resource Manager (ARM) template best practice](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/template-best-practices)

## Next Steps

- [] document steps to reproduce environment
- [] fix functions ARM template to deploy linux functions
- [] document demo steps
- [] Demo Azure Function in JS
- [] Logic App Integration
- [] Telemetry
- [] Alerts & Notification
- [] DR

---

### PLEASE NOTE FOR THE ENTIRETY OF THIS REPOSITORY AND ALL ASSETS

1. No warranties or guarantees are made or implied.
2. All assets here are provided by me "as is". Use at your own risk. Validate before use.
3. I am not representing my employer with these assets, and my employer assumes no liability whatsoever, and will not provide support, for any use of these assets.
4. Use of the assets in this repo in your Azure environment may or will incur Azure usage and charges. You are completely responsible for monitoring and managing your Azure usage.

---

Unless otherwise noted, all assets here are authored by me. Feel free to examine, learn from, comment, and re-use (subject to the above) as needed and without intellectual property restrictions.

If anything here helps you, attribution and/or a quick note is much appreciated.
