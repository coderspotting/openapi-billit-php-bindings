# OpenAPI\Billit\FileApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**fileGetOrders()**](FileApi.md#fileGetOrders) | **GET** /v1/files/{fileID} | Get a file specified by the fileID |


## `fileGetOrders()`

```php
fileGetOrders($file_id): \OpenAPI\Billit\Model\File
```

Get a file specified by the fileID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\FileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$file_id = 'file_id_example'; // string

try {
    $result = $apiInstance->fileGetOrders($file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FileApi->fileGetOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file_id** | **string**|  | |

### Return type

[**\OpenAPI\Billit\Model\File**](../Model/File.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
