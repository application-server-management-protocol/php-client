# ASMP\Client\DefaultApi

All URIs are relative to *https://swagger.asmp.io/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check**](DefaultApi.md#check) | **POST** /check | Check for potential changes
[**request**](DefaultApi.md#request) | **POST** /request | Request a specific change
[**status**](DefaultApi.md#status) | **GET** /status/{id} | Get the current status for a given request ID

# **check**
> check($body)

Check for potential changes

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\Check(); // \ASMP\Client\Model\Check | Check request

try {
    $apiInstance->check($body);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->check: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\ASMP\Client\Model\Check**](../Model/Check.md)| Check request |

### Return type

void (empty response body)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **request**
> request($body)

Request a specific change

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\Request(); // \ASMP\Client\Model\Request | Request request

try {
    $apiInstance->request($body);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->request: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\ASMP\Client\Model\Request**](../Model/Request.md)| Request request |

### Return type

void (empty response body)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **status**
> status($id)

Get the current status for a given request ID

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "38400000-8cf0-11bd-b23e-10b96e4ef00d"; // string | UUID of the request to get the status from

try {
    $apiInstance->status($id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->status: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**string**](../Model/.md)| UUID of the request to get the status from |

### Return type

void (empty response body)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

