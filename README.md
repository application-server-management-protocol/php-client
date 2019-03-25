# SwaggerClient-php
Application Server Management Protocol server

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.php.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: asmp_auth
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-KEY', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-KEY', 'Bearer');

$apiInstance = new Swagger\Client\Api\ChangeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\ChangeRequest(); // \Swagger\Client\Model\ChangeRequest | Request a specific change

try {
    $result = $apiInstance->change($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChangeApi->change: ', $e->getMessage(), PHP_EOL;
}
?>
```

## Documentation for API Endpoints

All URIs are relative to *https://swagger.asmprotocol.org/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ChangeApi* | [**change**](docs/Api/ChangeApi.md#change) | **POST** /change | Request a specific change for one or multiple components as previously checked in a /check request
*CheckApi* | [**check**](docs/Api/CheckApi.md#check) | **POST** /check | Define a list of desired changes using abstract constraints. Server should process these constraints, check if they can be fulfilled and respond with the possible resolutions.
*RollbackApi* | [**rollback**](docs/Api/RollbackApi.md#rollback) | **POST** /rollback | Rollback a specific change set
*StatusApi* | [**status**](docs/Api/StatusApi.md#status) | **GET** /status/{id} | Get the current status for a given request ID

## Documentation For Models

 - [ChangeRequest](docs/Model/ChangeRequest.md)
 - [ChangeResponse](docs/Model/ChangeResponse.md)
 - [ChangeStatusCode](docs/Model/ChangeStatusCode.md)
 - [CheckRequest](docs/Model/CheckRequest.md)
 - [CheckResponse](docs/Model/CheckResponse.md)
 - [ComponentChange](docs/Model/ComponentChange.md)
 - [ComponentGroup](docs/Model/ComponentGroup.md)
 - [Constraint](docs/Model/Constraint.md)
 - [ConstraintGroup](docs/Model/ConstraintGroup.md)
 - [RollbackRequest](docs/Model/RollbackRequest.md)
 - [StatusResponse](docs/Model/StatusResponse.md)

## Documentation For Authorization


## asmp_auth

- **Type**: API key
- **API key parameter name**: X-API-KEY
- **Location**: HTTP header


## Author

info@asmprotocol.org

