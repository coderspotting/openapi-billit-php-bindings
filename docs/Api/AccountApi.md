# OpenAPI\Billit\AccountApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**accountAddLicenseBillable()**](AccountApi.md#accountAddLicenseBillable) | **POST** /v1/account/license/addons | Add new License Billable |
| [**accountGetAccountInformation()**](AccountApi.md#accountGetAccountInformation) | **GET** /v1/account/accountInformation | Get account information about the current user |
| [**accountGetSSOToken()**](AccountApi.md#accountGetSSOToken) | **GET** /v1/account/ssoToken | Get an SSO token of the current user |
| [**accountPostSequences()**](AccountApi.md#accountPostSequences) | **POST** /v1/account/sequences | Update the sequence of a specific type |
| [**accountRegisterCompany()**](AccountApi.md#accountRegisterCompany) | **POST** /v1/account/registercompany | Registers a Company in the Billit-ecosphere |
| [**accountUpdateLicense()**](AccountApi.md#accountUpdateLicense) | **POST** /v1/account/license | Update the license |


## `accountAddLicenseBillable()`

```php
accountAddLicenseBillable($license_billable_model): int
```

Add new License Billable

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$license_billable_model = new \OpenAPI\Billit\Model\AddNewLicenseBillableModel(); // \OpenAPI\Billit\Model\AddNewLicenseBillableModel

try {
    $result = $apiInstance->accountAddLicenseBillable($license_billable_model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountAddLicenseBillable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **license_billable_model** | [**\OpenAPI\Billit\Model\AddNewLicenseBillableModel**](../Model/AddNewLicenseBillableModel.md)|  | |

### Return type

**int**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountGetAccountInformation()`

```php
accountGetAccountInformation(): \OpenAPI\Billit\Model\AccountInformation
```

Get account information about the current user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->accountGetAccountInformation();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetAccountInformation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\AccountInformation**](../Model/AccountInformation.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountGetSSOToken()`

```php
accountGetSSOToken(): object
```

Get an SSO token of the current user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->accountGetSSOToken();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountGetSSOToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountPostSequences()`

```php
accountPostSequences($sequence_request): string
```

Update the sequence of a specific type

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$sequence_request = new \OpenAPI\Billit\Model\SequenceRequest(); // \OpenAPI\Billit\Model\SequenceRequest

try {
    $result = $apiInstance->accountPostSequences($sequence_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountPostSequences: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sequence_request** | [**\OpenAPI\Billit\Model\SequenceRequest**](../Model/SequenceRequest.md)|  | |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountRegisterCompany()`

```php
accountRegisterCompany($register_account_request): \OpenAPI\Billit\Model\RegisterAccountResponse
```

Registers a Company in the Billit-ecosphere

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$register_account_request = new \OpenAPI\Billit\Model\RegisterAccountRequestModel(); // \OpenAPI\Billit\Model\RegisterAccountRequestModel

try {
    $result = $apiInstance->accountRegisterCompany($register_account_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountRegisterCompany: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **register_account_request** | [**\OpenAPI\Billit\Model\RegisterAccountRequestModel**](../Model/RegisterAccountRequestModel.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\RegisterAccountResponse**](../Model/RegisterAccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountUpdateLicense()`

```php
accountUpdateLicense($update_license_model): int
```

Update the license

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\AccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$update_license_model = new \OpenAPI\Billit\Model\UpdateLicenseRequestModel(); // \OpenAPI\Billit\Model\UpdateLicenseRequestModel

try {
    $result = $apiInstance->accountUpdateLicense($update_license_model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountApi->accountUpdateLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_license_model** | [**\OpenAPI\Billit\Model\UpdateLicenseRequestModel**](../Model/UpdateLicenseRequestModel.md)|  | |

### Return type

**int**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
