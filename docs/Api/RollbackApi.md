# ASMP\Client\RollbackApi

All URIs are relative to *https://swagger.asmp.io/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**rollback**](RollbackApi.md#rollback) | **POST** /rollback | Rollback a specific change set

# **rollback**
> \ASMP\Client\Model\ChangeResponse rollback($body)

Rollback a specific change set

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: asmp_auth
$config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = ASMP\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new ASMP\Client\Api\RollbackApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \ASMP\Client\Model\RollbackRequest(); // \ASMP\Client\Model\RollbackRequest | Define the changeset that should be rolled back

try {
    $result = $apiInstance->rollback($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RollbackApi->rollback: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\ASMP\Client\Model\RollbackRequest**](../Model/RollbackRequest.md)| Define the changeset that should be rolled back |

### Return type

[**\ASMP\Client\Model\ChangeResponse**](../Model/ChangeResponse.md)

### Authorization

[asmp_auth](../../README.md#asmp_auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

