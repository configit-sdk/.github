# Welcome to the Configit SDK :wave:

Welcome to the Configit SDK, home of libraries and sample code for Configit partners.

> **Getting access**: The Configit SDK repositories and NuGet/npm packages are private.<br/>To request access, mail configit-sdk-req@configit.com.

## Docker container images

Ace Platform is available as a Docker container image at [ghcr.io/configit-sdk/ace-platform](https://ghcr.io/configit-sdk/ace-platform).

## Libraries

Ace offers several libraries for developing software that integrates with an Ace solution.
Here are some use cases to guide you:

- [Creating packages](#creating-packages)
- [Reading/writing Ace Model data](#readingwriting-ace-model-data)
- [Building a configurator](#building-a-configurator)
- [Accessing a specific web API](#accessing-a-specific-web-api)

### Creating packages

> [!NOTE] 
> This library has Limited Availability.

Use the **Ace Package Builder for .NET** to construct packages
that can be published to Ace Platform.

- NuGet package — [`Configit.Ace.Public`](https://github.com/configit-sdk/ace-packagebuilder-samples/pkgs/nuget/Configit.Ace.Public)
- Sample application — [Ace Package Builder sample](https://github.com/configit-sdk/ace-packagebuilder-samples)

Note that this is a lower-level API that uses concepts such as variables and
values compared to higher-level Ace Model concepts like families and features.

### Reading/writing Ace Model data

If you need to read or write Model data such as product models, features, 
and families, choose from these libraries:

- **Ace Model Import Client for .NET** — For creating Ace Model import XML files.
  This client is intended for bulk creation of data entities.
  - NuGet package — [`Configit.Ace.Model.Import.Client`](https://github.com/configit-sdk/ace-model-samples/packages/1467389)
  - Sample application — [Ace Model Import Client sample](https://github.com/configit-sdk/ace-model-samples/tree/main/XmlClientSampleModel)

- **Ace Model Client for .NET** — Wraps the Model API.
  - NuGet package — [`Configit.Ace.Model.Client`](https://github.com/configit-sdk/ace-model-samples/packages/1459862)
  - Sample application — [Ace Model Client sample](https://github.com/configit-sdk/ace-model-samples/tree/main/ModelApi/ApiClientSampleModel)

### Building a configurator

Choose from the below libraries to develop configurator applications. Though the configurator client names are similar, they differ in API coverage
as described in [Accessing a specific web API](#accessing-a-specific-web-api).

> [!IMPORTANT] 
> Prior to installing npm packages, you must [set up access](#setting-up-access-to-npm-packages).

- **Ace Platform Client for TypeScript** — For building interactive web configurators in TypeScript.
  The client consists of two npm packages:
  - [`ace-platform-client`](https://github.com/configit-sdk/ace-configure-samples/packages/1325398), the main library.
  - [`ace-platform-client-react`](https://github.com/configit-sdk/ace-configure-samples/packages/1325400), an optional companion library for React development.

- **Ace Platform Client for .NET** — For building configurators in C#/.NET.
  - NuGet package — NuGet package — [`Configit.Ace.Public`](https://github.com/configit-sdk/ace-packagebuilder-samples/pkgs/nuget/Configit.Ace.Public)
  - Sample application — [CLI Configurator](https://github.com/configit-sdk/ace-configure-samples/tree/master/cli-configurator)
- **Ace Platform Offline Client for .NET** — For building configurators in C#/.NET that work offline.
  The other clients require continuous access to Ace Platform.
  - NuGet package — NuGet package — [`Configit.Ace.Public`](https://github.com/configit-sdk/ace-packagebuilder-samples/pkgs/nuget/Configit.Ace.Public)
  - Sample application —
  [CLI Offline Configurator](https://github.com/configit-sdk/ace-configure-samples/tree/master/cli-offline-configurator)

### Accessing a specific web API

Ace client libraries are the recommended way for interacting with the
Ace web APIs.  The table below shows the web APIs supported by each client:

|                    | Ace Model Client (.NET) | Ace Platform Client (TypeScript) | Ace Platform Client (.NET) | Ace Platform Offline Client (.NET) |
| ------------------ | ----------------------- | -------------------------------- | -------------------------- | ---------------------------------- |
| Model API          | ☑️                      |                                  |                            |                                    |
| Packages API       |                         | ☑️                               | ☑️                         |                                    |
| Configuration API  |                         | ☑️                               | ☑️                         | ☑️                                 |
| Solution Space API |                         |                                  | ☑️                         |                                    |
| Analyze API        |                         | ☑️                               | ☑️                         |                                    |
| BOM API            |                         | ☑️                               | ☑️                         |                                    |

### Setting up access to npm packages

To get access to the configit-sdk npm packages, set up your environment as follows.

#### Step 1 — Generate a GitHub Personal Access Token

1. Go to your GitHub account settings.
2. Navigate to "Developer settings" > "Personal access tokens".
1. Generate a new token with the permissions `repo` and `read:packages`.

#### Step 2 - Configure npm to use your GitHub token

From the command line, run:

```
npm login --scope=@configit-sdk --registry=https://npm.pkg.github.com --always-auth
```

When prompted, enter your GitHub username, the personal access token as your password, and your GitHub email.

This results in changes to your default `.npmrc` file. To verify the changes, check that your `.npmrc` file contains:

```
@configit-sdk:always-auth = true
@configit-sdk:registry = "https://npm.pkg.github.com/"
//npm.pkg.github.com/:_authToken=YOUR_PERSONAL_ACCESS_TOKEN
```
