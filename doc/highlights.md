# Highlights

## Azure Functions

- Azure Functions offers out-of-the-box bindings (aka integration) across the Azure platform for triggers, inputs, and outputs
  - For example, Azure Functions supports HTTP triggers, Azure Event Hub input, Azure Cosmos DB output - which is used in this solution. See [this](https://docs.microsoft.com/en-us/azure/azure-functions/functions-triggers-bindings#supported-bindings) for the complete list of supported Azure Functions bindings

- Azure Functions offers built-in integration with Azure Application Insights to monitor functions. It allows users to query telemetries and logs that are generated by the functions. To learn more, see "[Monitor Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-monitoring)"

- Azure Functions has different service tiers which includes different features. In particular, the [Azure Functions Premium plan](https://docs.microsoft.com/en-us/azure/azure-functions/functions-premium-plan#features) has pre-warmed instances, VNet integration, longer run duration, and other premium features

## Azure Logic App

- Logic App offers [hundreds of ready-to-use connectors](https://docs.microsoft.com/en-us/azure/connectors/apis-list) (which includes Azure Functions, Azure Storage, Azure SQL Database, SAP, Office365, Oracle Database, and more) to simplify integration of apps, data, systems, and services across enterprises or organizations

- You can build logic apps visually with the Logic Apps Designer, which is available in the Azure portal through your browser and in Visual Studio

- Logic app supports [batch processing](https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-batch-process-send-receive-messages) that collects messages into a batch until your specified criteria are met for releasing and processing the batched messages. This pattern requires a "[batch receiver](https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-batch-process-send-receive-messages#batch-receiver)" and a "[batch sender](https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-batch-process-send-receive-messages#create-batch-sender)" logic apps

## GitHub Actions

- [GitHub Actions](https://github.blog/2019-08-08-github-actions-now-supports-ci-cd/) make it possible to create simple yet powerful workflows to enable CI/CD and automation. Defined in YAML files, GitHub Actions allow you to trigger an automated workflow process on any GitHub event, such as code commits, creation of Pull Requests or new GitHub Releases, and more.

- GitHub is powered by the open source communities, so is GitHub Actions. To see complete list of ready-to-use Actions developed by the communities, explore the [GitHub Actions Marketplace](https://github.com/marketplace?type=actions)

## API Management (APIM)

- APIM helps organizations publish APIs to external, partner, and internal developers to unlock the potential of their data and services

- [Products](https://docs.microsoft.com/en-us/azure/api-management/api-management-key-concepts#--products) are grouping of APIs which are surfaced to API consumers. Products in APIM have one or more APIs, and are configured with a title, description, and terms of use

- [Policies](https://docs.microsoft.com/en-us/azure/api-management/api-management-key-concepts#--policies) allow the APIM to change the behavior of the API through configuration. Policies are a collection of statements that are executed sequentially on the request or response of an API. Popular statements include format conversion from XML to JSON and rate limiting to restrict the number of incoming calls from an application. For a complete list of APIM policies, see [Policy reference](https://docs.microsoft.com/en-us/azure/api-management/api-management-policies)

- [Developer portal](https://docs.microsoft.com/en-us/azure/api-management/api-management-key-concepts#--developer-portal) is where developers can learn about your APIs, view and call operations, and subscribe to products. Prospective customers can visit the developer portal, view APIs and operations, and sign up. APIM administrators can customize the look and feel of the developer portal by adding custom content, customizing styles, and adding custom branding
