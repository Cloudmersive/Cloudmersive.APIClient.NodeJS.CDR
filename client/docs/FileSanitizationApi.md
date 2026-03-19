# CloudmersiveCdrApiClient.FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**file**](FileSanitizationApi.md#file) | **POST** /cdr/sanitization/file | Content Disarm and Reconstruction on a File
[**fileAdvanced**](FileSanitizationApi.md#fileAdvanced) | **POST** /cdr/sanitization/file/advanced | Advanced Content Disarm and Reconstruction on a File
[**fileToPdf**](FileSanitizationApi.md#fileToPdf) | **POST** /cdr/sanitization/file/to/pdf | Content Disarm and Reconstruction on a File with PDFA Output
[**fileToPdfAdvanced**](FileSanitizationApi.md#fileToPdfAdvanced) | **POST** /cdr/sanitization/file/to/pdf/advanced | Advanced Content Disarm and Reconstruction on a File with PDFA Output


<a name="file"></a>
# **file**
> 'Blob' file(opts)

Content Disarm and Reconstruction on a File

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
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.file(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

**'Blob'**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

<a name="fileAdvanced"></a>
# **fileAdvanced**
> 'Blob' fileAdvanced(opts)

Advanced Content Disarm and Reconstruction on a File

Processes the input file via CDR to produce a secured output file with advanced scan options and response headers containing scan metadata.

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
  'allowExecutables': true, // Boolean | Set to false to block executable files (EXE, DLL, etc.)
  'allowInvalidFiles': true, // Boolean | Set to false to block files that are not valid for their detected type
  'allowScripts': true, // Boolean | Set to false to block script files. PDF and Office macro sanitization still runs regardless.
  'allowPasswordProtectedFiles': true, // Boolean | Set to false to block password-protected files
  'allowMacros': true, // Boolean | Set to false to block files containing macros. Office macro removal still runs regardless.
  'allowXmlExternalEntities': true, // Boolean | Set to false to block XML files with external entity references (XXE)
  'allowInsecureDeserialization': true, // Boolean | Set to false to block files with insecure deserialization patterns
  'allowHtml': true, // Boolean | Set to false to block HTML files
  'allowUnsafeArchives': true, // Boolean | Set to false to block archive files flagged as unsafe (e.g., zip bombs)
  'allowOleEmbeddedObject': true, // Boolean | Set to false to block files with embedded OLE objects
  'allowUnwantedAction': true, // Boolean | Set to false to block files with unwanted actions
  'restrictFileTypes': "restrictFileTypes_example", // String | Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked.
  'inputFile': "/path/to/file.txt" // File | Input document to CDR process
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.fileAdvanced(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowExecutables** | **Boolean**| Set to false to block executable files (EXE, DLL, etc.) | [optional] 
 **allowInvalidFiles** | **Boolean**| Set to false to block files that are not valid for their detected type | [optional] 
 **allowScripts** | **Boolean**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | [optional] 
 **allowPasswordProtectedFiles** | **Boolean**| Set to false to block password-protected files | [optional] 
 **allowMacros** | **Boolean**| Set to false to block files containing macros. Office macro removal still runs regardless. | [optional] 
 **allowXmlExternalEntities** | **Boolean**| Set to false to block XML files with external entity references (XXE) | [optional] 
 **allowInsecureDeserialization** | **Boolean**| Set to false to block files with insecure deserialization patterns | [optional] 
 **allowHtml** | **Boolean**| Set to false to block HTML files | [optional] 
 **allowUnsafeArchives** | **Boolean**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | [optional] 
 **allowOleEmbeddedObject** | **Boolean**| Set to false to block files with embedded OLE objects | [optional] 
 **allowUnwantedAction** | **Boolean**| Set to false to block files with unwanted actions | [optional] 
 **restrictFileTypes** | **String**| Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked. | [optional] 
 **inputFile** | **File**| Input document to CDR process | [optional] 

### Return type

**'Blob'**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

<a name="fileToPdf"></a>
# **fileToPdf**
> 'Blob' fileToPdf(opts)

Content Disarm and Reconstruction on a File with PDFA Output

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
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.fileToPdf(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inputFile** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

**'Blob'**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

<a name="fileToPdfAdvanced"></a>
# **fileToPdfAdvanced**
> 'Blob' fileToPdfAdvanced(opts)

Advanced Content Disarm and Reconstruction on a File with PDFA Output

Processes the input file via CDR to produce a secured PDF/A output file with advanced scan options and response headers containing scan metadata.

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
  'allowExecutables': true, // Boolean | Set to false to block executable files (EXE, DLL, etc.)
  'allowInvalidFiles': true, // Boolean | Set to false to block files that are not valid for their detected type
  'allowScripts': true, // Boolean | Set to false to block script files. PDF and Office macro sanitization still runs regardless.
  'allowPasswordProtectedFiles': true, // Boolean | Set to false to block password-protected files
  'allowMacros': true, // Boolean | Set to false to block files containing macros. Office macro removal still runs regardless.
  'allowXmlExternalEntities': true, // Boolean | Set to false to block XML files with external entity references (XXE)
  'allowInsecureDeserialization': true, // Boolean | Set to false to block files with insecure deserialization patterns
  'allowHtml': true, // Boolean | Set to false to block HTML files
  'allowUnsafeArchives': true, // Boolean | Set to false to block archive files flagged as unsafe (e.g., zip bombs)
  'allowOleEmbeddedObject': true, // Boolean | Set to false to block files with embedded OLE objects
  'allowUnwantedAction': true, // Boolean | Set to false to block files with unwanted actions
  'restrictFileTypes': "restrictFileTypes_example", // String | Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked.
  'inputFile': "/path/to/file.txt" // File | Input document to CDR process
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.fileToPdfAdvanced(opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allowExecutables** | **Boolean**| Set to false to block executable files (EXE, DLL, etc.) | [optional] 
 **allowInvalidFiles** | **Boolean**| Set to false to block files that are not valid for their detected type | [optional] 
 **allowScripts** | **Boolean**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | [optional] 
 **allowPasswordProtectedFiles** | **Boolean**| Set to false to block password-protected files | [optional] 
 **allowMacros** | **Boolean**| Set to false to block files containing macros. Office macro removal still runs regardless. | [optional] 
 **allowXmlExternalEntities** | **Boolean**| Set to false to block XML files with external entity references (XXE) | [optional] 
 **allowInsecureDeserialization** | **Boolean**| Set to false to block files with insecure deserialization patterns | [optional] 
 **allowHtml** | **Boolean**| Set to false to block HTML files | [optional] 
 **allowUnsafeArchives** | **Boolean**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | [optional] 
 **allowOleEmbeddedObject** | **Boolean**| Set to false to block files with embedded OLE objects | [optional] 
 **allowUnwantedAction** | **Boolean**| Set to false to block files with unwanted actions | [optional] 
 **restrictFileTypes** | **String**| Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked. | [optional] 
 **inputFile** | **File**| Input document to CDR process | [optional] 

### Return type

**'Blob'**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream

