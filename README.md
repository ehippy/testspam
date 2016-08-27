# bombbomb-nodejs-openapi

BombbombNodejsOpenapi - JavaScript client for bombbomb-nodejs-openapi
We make it easy to use simple video to build relationships
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 2.0
- Package version: 1.0.0
- Build date: 2016-08-27T05:21:50.012Z
- Build package: class io.swagger.codegen.languages.JavascriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install bombbomb-nodejs-openapi --save
```

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/GIT_USER_ID/GIT_REPO_ID
then install it via:

```shell
    npm install GIT_USER_ID/GIT_REPO_ID --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var BombbombNodejsOpenapi = require('bombbomb-nodejs-openapi');

var api = new BombbombNodejsOpenapi.PromptsApi()

var prompt = new BombbombNodejsOpenapi.JerichoConfiguration(); // {JerichoConfiguration} The Video Email Prompt to be created


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.createVideoEmailPrompt(prompt, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://dev.api.bombbomb.com/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BombbombNodejsOpenapi.PromptsApi* | [**createVideoEmailPrompt**](docs/PromptsApi.md#createVideoEmailPrompt) | **POST** /prompt | Prompts user to send a video
*BombbombNodejsOpenapi.PromptsApi* | [**getVideoEmailPrompt**](docs/PromptsApi.md#getVideoEmailPrompt) | **GET** /prompt/{id} | Gets a prompt
*BombbombNodejsOpenapi.PromptsApi* | [**respondToVideoEmailPrompt**](docs/PromptsApi.md#respondToVideoEmailPrompt) | **POST** /prompt/{id}/response | Respond to a prompt
*BombbombNodejsOpenapi.TeamsApi* | [**queueJerichoSend**](docs/TeamsApi.md#queueJerichoSend) | **POST** /team/{teamId}/jericho | Creates a Jericho send.
*BombbombNodejsOpenapi.UtilitiesApi* | [**createOAuthClient**](docs/UtilitiesApi.md#createOAuthClient) | **POST** /oauthclient | Create an OAuth Client
*BombbombNodejsOpenapi.UtilitiesApi* | [**deleteOAuthClient**](docs/UtilitiesApi.md#deleteOAuthClient) | **DELETE** /oauthclient/{id} | Delete an OAuth Client
*BombbombNodejsOpenapi.UtilitiesApi* | [**getOAuthClients**](docs/UtilitiesApi.md#getOAuthClients) | **GET** /oauthclient | Lists OAuth Clients
*BombbombNodejsOpenapi.UtilitiesApi* | [**getSpec**](docs/UtilitiesApi.md#getSpec) | **GET** /spec | Describes this api
*BombbombNodejsOpenapi.WebhooksApi* | [**addWebHook**](docs/WebhooksApi.md#addWebHook) | **POST** /webhook | Add Webhook
*BombbombNodejsOpenapi.WebhooksApi* | [**deleteWebHook**](docs/WebhooksApi.md#deleteWebHook) | **DELETE** /webhook/{hookId} | Deletes Webhook
*BombbombNodejsOpenapi.WebhooksApi* | [**getWebHooks**](docs/WebhooksApi.md#getWebHooks) | **GET** /webhook/ | Lists Webhooks
*BombbombNodejsOpenapi.WebhooksApi* | [**sendWebhookExample**](docs/WebhooksApi.md#sendWebhookExample) | **POST** /webhook/test | Sends test Webhook


## Documentation for Models

 - [BombbombNodejsOpenapi.JerichoConfiguration](docs/JerichoConfiguration.md)
 - [BombbombNodejsOpenapi.ModelString](docs/ModelString.md)
 - [BombbombNodejsOpenapi.Webhook](docs/Webhook.md)


## Documentation for Authorization


### BBOAuth2

- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: https://dev.app.bombbomb.com/auth/authorize
- **Scopes**: 
  - all:manage: Manage All
  - all:read: Read All
  - email:manage: Manage Email
  - email:read: Read Email
  - video:manage: Manage Video
  - video:read: Read Video
  - contact:manage: Manage Contact
  - contact:read: Read Contact
  - automation:manage: Manage Automation
  - automation:read: Read Automation
  - form:manage: Manage Form
  - form:read: Read Form
  - settings:manage: Manage Settings

