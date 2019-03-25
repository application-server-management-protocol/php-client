# ASMP\Client\ChangeApi

All URIs are relative to *https://swagger.asmprotocol.org/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**change**](ChangeApi.md#change) | **POST** /change | Request a specific change for one or multiple components as previously checked in a /check request
[**check**](ChangeApi.md#check) | **POST** /check | Define a list of desired changes using abstract constraints. Server should process these constraints, check if they can be fulfilled and respond with the possible resolutions.

# **change**
> \ASMP\Client\Model\ChangeResponse change($body)

Request a specific change for one or multiple components as previously checked in a /check request

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\ChangeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\ChangeRequest(); // \ASMP\Client\Model\ChangeRequest | Request a specific change

try {
    $result = $apiInstance->change($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChangeApi->change: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\ASMP\Client\Model\ChangeRequest**](../Model/ChangeRequest.md)| Request a specific change |

### Return type

[**\ASMP\Client\Model\ChangeResponse**](../Model/ChangeResponse.md)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **check**
> \ASMP\Client\Model\CheckResponse check($body)

Define a list of desired changes using abstract constraints. Server should process these constraints, check if they can be fulfilled and respond with the possible resolutions.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\ChangeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\CheckRequest(); // \ASMP\Client\Model\CheckRequest | Check request

try {
    $result = $apiInstance->check($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChangeApi->check: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\ASMP\Client\Model\CheckRequest**](../Model/CheckRequest.md)| Check request |

### Return type

[**\ASMP\Client\Model\CheckResponse**](../Model/CheckResponse.md)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

