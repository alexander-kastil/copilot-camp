# Overview of Custom Search Results app template

## Build a message extension from a new API with Azure Functions

This app template allows Teams to interact directly with third-party data, apps, and services, enhancing its capabilities and broadening its range of capabilities. It allows Teams to:

- Retrieve real-time information, for example, latest news coverage on a product launch.
- Retrieve knowledge-based information, for example, my team’s design files in Figma.

## Get started with the template

> **Prerequisites**
>
> To run this app template in your local dev machine, you will need:
>
> - [Node.js](https://nodejs.org/), supported versions: 16, 18
> - A [Microsoft 365 account for development](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts)
> - [Teams Toolkit Visual Studio Code Extension](https://aka.ms/teams-toolkit) version 5.0.0 and higher or [Teams Toolkit CLI](https://aka.ms/teamsfx-cli)

1. First, select the Teams Toolkit icon on the left in the VS Code toolbar.
2. In the Account section, sign in with your [Microsoft 365 account](https://docs.microsoft.com/microsoftteams/platform/toolkit/accounts) if you haven't already.
3. Select `Debug in Teams (Edge)` or `Debug in Teams (Chrome)` from the launch configuration dropdown.
4. When Teams launches in the browser, you can navigate to a chat message and [trigger your search commands from compose message area](https://learn.microsoft.com/microsoftteams/platform/messaging-extensions/what-are-messaging-extensions?tabs=dotnet#search-commands).

## What's included in the template

| Folder       | Contents                                                                                                    |
| ------------ | ----------------------------------------------------------------------------------------------------------- |
| `.vscode`    | VSCode files for debugging                                                                                  |
| `appPackage` | Templates for the Teams application manifest, the API specification and response template for API responses |
| `env`        | Environment files                                                                                           |
| `infra`      | Templates for provisioning Azure resources                                                                  |
| `repair`     | The source code for the repair API                                                                          |

The following files can be customized and demonstrate an example implementation to get you started.

| File                                          | Contents                                                                     |
| --------------------------------------------- | ---------------------------------------------------------------------------- |
| `repair/function.json`                        | A configuration file that defines the function’s trigger and other settings. |
| `repair/index.ts`                             | The main file of a function in Azure Functions.                              |
| `appPackage/apiSpecificationFiles/repair.yml` | A file that describes the structure and behavior of the repair API.          |
| `appPackage/responseTemplates/repair.json`    | A generated Adaptive Card that used to render API response.                  |
| `repairsData.json`                            | The data source for the repair API                                           |

The following are Teams Toolkit specific project files. You can [visit a complete guide on Github](https://github.com/OfficeDev/TeamsFx/wiki/Teams-Toolkit-Visual-Studio-Code-v5-Guide#overview) to understand how Teams Toolkit works.

| File                 | Contents                                                                                                                                  |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `teamsapp.yml`       | This is the main Teams Toolkit project file. The project file defines two primary things: Properties and configuration Stage definitions. |
| `teamsapp.local.yml` | This overrides `teamsapp.yml` with actions that enable local execution and debugging.                                                     |

## Addition information and references

- [Extend Teams platform with APIs](https://aka.ms/teamsfx-api-plugin)