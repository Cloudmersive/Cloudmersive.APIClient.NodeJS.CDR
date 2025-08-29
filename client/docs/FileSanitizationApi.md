# CloudmersiveCdrApiClient.FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**file**](FileSanitizationApi.md#file) | **POST** /cdr/sanitization/file | Complete Content Disarm and Reconstruction on an Input File, and output in same file format
[**fileToPdf**](FileSanitizationApi.md#fileToPdf) | **POST** /cdr/sanitization/file/to/pdf | Complete Content Disarm and Reconstruction on an Input File with PDF/A Output


<a name="file"></a>
# **file**
> file(opts)

Complete Content Disarm and Reconstruction on an Input File, and output in same file format

Processes the input file via CDR to produce a secured output file.  Input content is parsed, disarmed, and then reconstructed into a new output file with the same file format as the input.

### Example
```javascript
var CloudmersiveCdrApiClient = require('cloudmersive-cdr-api-client');
var defaultClient = CloudmersiveCdrApiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveCdrApiClient.FileSanitizationApi();

var opts = { 
  'inputFile': "/path/to/file.txt" // File | Input document, or photos of a document, to extract data from
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.file(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

null (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

<a name="fileToPdf"></a>
# **fileToPdf**
> fileToPdf(opts)

Complete Content Disarm and Reconstruction on an Input File with PDF/A Output

Processes the input file via CDR to produce a secured PDF/A output file.  Input content is parsed, disarmed, and then reconstructed into a new PDF/A output file.

### Example
```javascript
var CloudmersiveCdrApiClient = require('cloudmersive-cdr-api-client');
var defaultClient = CloudmersiveCdrApiClient.ApiClient.instance;

// Configure API key authorization: Apikey
var Apikey = defaultClient.authentications['Apikey'];
Apikey.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Apikey.apiKeyPrefix = 'Token';

var apiInstance = new CloudmersiveCdrApiClient.FileSanitizationApi();

var opts = { 
  'inputFile': "/path/to/file.txt" // File | Input document, or photos of a document, to extract data from
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
apiInstance.fileToPdf(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

null (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined

