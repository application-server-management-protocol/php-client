# Swagger\Client\CheckApi

All URIs are relative to *https://swagger.asmprotocol.org/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check**](CheckApi.md#check) | **POST** /check | Define a list of desired changes using abstract constraints. Server should process these constraints, check if they can be fulfilled and respond with the possible resolutions.

# **check**
> \Swagger\Client\Model\CheckResponse check($body)

Define a list of desired changes using abstract constraints. Server should process these constraints, check if they can be fulfilled and respond with the possible resolutions.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\CheckApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\CheckRequest(); // \Swagger\Client\Model\CheckRequest | Check request

try {
    $result = $apiInstance->check($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CheckApi->check: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\CheckRequest**](../Model/CheckRequest.md)| Check request |

### Return type

[**\Swagger\Client\Model\CheckResponse**](../Model/CheckResponse.md)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

