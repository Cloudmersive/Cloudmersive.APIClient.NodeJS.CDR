# cloudmersive-cdr-api-client

CloudmersiveCdrApiClient - JavaScript client for cloudmersive-cdr-api-client
Use the Content Disarm and Reconstruction API to remove security risks from documents by tearing them down, removing unsafe content and rebuilding them.
[Cloudmersive CDR API](https://www.cloudmersive.com/cdr-api) provides advanced document sanitization capabilities.

- API version: v1
- Package version: 1.0.0


## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install cloudmersive-cdr-api-client --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your cloudmersive-cdr-api-client from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('cloudmersive-cdr-api-client')` in javascript files from the directory you ran the last 
command above from.

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
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var CloudmersiveCdrApiClient = require('cloudmersive-cdr-api-client');

var defaultClient = CloudmersiveCdrApiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix['Apikey'] = "Token"

var api = new CloudmersiveCdrApiClient.FileSanitizationApi()

var opts = { 
  'inputFile': "/path/to/file.txt" // {File} Input document, or photos of a document, to extract data from
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.file(opts, callback);

```

## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CloudmersiveCdrApiClient.FileSanitizationApi* | [**file**](docs/FileSanitizationApi.md#file) | **POST** /cdr/sanitization/file | Complete Content Disarm and Reconstruction on an Input File, and output in same file format
*CloudmersiveCdrApiClient.FileSanitizationApi* | [**fileToPdf**](docs/FileSanitizationApi.md#fileToPdf) | **POST** /cdr/sanitization/file/to/pdf | Complete Content Disarm and Reconstruction on an Input File with PDF/A Output


## Documentation for Models



## Documentation for Authorization


### Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header

