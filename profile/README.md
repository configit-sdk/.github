# Welcome to the Configit SDK :wave:

Welcome to the Configit SDK, home of libraries and sample code for Configit partners.

> **Getting access**: The Configit SDK repositories and NuGet/npm packages are private.<br/> To request access, mail configit-sdk-req@configit.com.

The following libraries are available for Configit Ace.

### Ace Model Client for .NET

A helper library for the Ace Model API, letting you read or write Ace Model data.

- NuGet package — [`Configit.Ace.Model.Client`](https://github.com/configit-sdk/ace-model-samples/packages/1459862)
- Sample application — [Ace Model Client sample](https://github.com/configit-sdk/ace-model-samples/tree/main/ModelApi/ApiClientSampleModel)

### Ace Model Import Client for .NET

A library for generating XML import files for Ace Model. This client is intended for bulk creation of data entities.

- NuGet package — [`Configit.Ace.Model.Import.Client`](https://github.com/configit-sdk/ace-model-samples/packages/1467389)
- Sample application — [Ace Model Import Client sample](https://github.com/configit-sdk/ace-model-samples/tree/main/XmlClientSampleModel)

### Ace Platform Client for .NET

A helper library for calling the Packages API, Configuration API, Solution Space API, and Storage API. Use this client to build
interactive configurators, inspect products, and query a package for its individual resources.

- NuGet package — [`Configit.Ace.Platform.Client`](https://github.com/configit-sdk/ace-configure-samples/packages/1123127)
- Sample application — [CLI Configurator](https://github.com/configit-sdk/ace-configure-samples/tree/master/cli-configurator)

### Ace Platform Offline Client for .NET

An offline implementation of the Configuration API. Use this client to build configurators (intended for a single users) that run locally
against packages downloaded from Ace Platform.

- NuGet package — [`Configit.Ace.Platform.Client.Offline`](https://github.com/configit-sdk/ace-configure-samples/packages/1370338)
- Sample application —
  [CLI Offline Configurator](https://github.com/configit-sdk/ace-configure-samples/tree/master/cli-offline-configurator)

### Ace Platform Client for TypeScript

For building interactive web configurators in TypeScript. This client wraps the Configuration API and Packages API.

The client consists of two npm packages:

- [`ace-platform-client`](https://github.com/configit-sdk/ace-configure-samples/packages/1325398), the main library.
- [`ace-platform-client-react`](https://github.com/configit-sdk/ace-configure-samples/packages/1325400), an optional companion library for React development.
