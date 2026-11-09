# OpenAPI\Billit\GLAccountApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**gLAccountPostGLAccount()**](GLAccountApi.md#gLAccountPostGLAccount) | **POST** /v1/glaccounts | Create a general ledger account |
| [**gLAccountPostGLAccountBulk()**](GLAccountApi.md#gLAccountPostGLAccountBulk) | **POST** /v1/glaccounts/commands/import | Create multiple general ledger accounts using a list |


## `gLAccountPostGLAccount()`

```php
gLAccountPostGLAccount($account): int
```

Create a general ledger account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\GLAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$account = new \OpenAPI\Billit\Model\GLAccount(); // \OpenAPI\Billit\Model\GLAccount

try {
    $result = $apiInstance->gLAccountPostGLAccount($account);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GLAccountApi->gLAccountPostGLAccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account** | [**\OpenAPI\Billit\Model\GLAccount**](../Model/GLAccount.md)|  | |

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

## `gLAccountPostGLAccountBulk()`

```php
gLAccountPostGLAccountBulk($accounts)
```

Create multiple general ledger accounts using a list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\GLAccountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$accounts = array(new \OpenAPI\Billit\Model\GLAccount()); // \OpenAPI\Billit\Model\GLAccount[]

try {
    $apiInstance->gLAccountPostGLAccountBulk($accounts);
} catch (Exception $e) {
    echo 'Exception when calling GLAccountApi->gLAccountPostGLAccountBulk: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **accounts** | [**\OpenAPI\Billit\Model\GLAccount[]**](../Model/GLAccount.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
