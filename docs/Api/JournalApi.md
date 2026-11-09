# OpenAPI\Billit\JournalApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**journalPostGLAccount()**](JournalApi.md#journalPostGLAccount) | **POST** /v1/journals/commands/import | Import a list of journals |


## `journalPostGLAccount()`

```php
journalPostGLAccount($journals)
```

Import a list of journals

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\JournalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$journals = array(new \OpenAPI\Billit\Model\Journal()); // \OpenAPI\Billit\Model\Journal[]

try {
    $apiInstance->journalPostGLAccount($journals);
} catch (Exception $e) {
    echo 'Exception when calling JournalApi->journalPostGLAccount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **journals** | [**\OpenAPI\Billit\Model\Journal[]**](../Model/Journal.md)|  | |

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
