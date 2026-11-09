# OpenAPI\Billit\ToProcessApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**toProcessDeleteToProcess()**](ToProcessApi.md#toProcessDeleteToProcess) | **DELETE** /v1/toProcess/{uploadID} | Delete a document to process |
| [**toProcessGetToProcess()**](ToProcessApi.md#toProcessGetToProcess) | **GET** /v1/toProcess |  |
| [**toProcessPostToProcess()**](ToProcessApi.md#toProcessPostToProcess) | **POST** /v1/toProcess | Save a new document to process |


## `toProcessDeleteToProcess()`

```php
toProcessDeleteToProcess($upload_id)
```

Delete a document to process

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ToProcessApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$upload_id = 56; // int

try {
    $apiInstance->toProcessDeleteToProcess($upload_id);
} catch (Exception $e) {
    echo 'Exception when calling ToProcessApi->toProcessDeleteToProcess: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **upload_id** | **int**|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `toProcessGetToProcess()`

```php
toProcessGetToProcess()
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ToProcessApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->toProcessGetToProcess();
} catch (Exception $e) {
    echo 'Exception when calling ToProcessApi->toProcessGetToProcess: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `toProcessPostToProcess()`

```php
toProcessPostToProcess($to_process): int
```

Save a new document to process

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ToProcessApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$to_process = new \OpenAPI\Billit\Model\ToProcessSaveRequest(); // \OpenAPI\Billit\Model\ToProcessSaveRequest

try {
    $result = $apiInstance->toProcessPostToProcess($to_process);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ToProcessApi->toProcessPostToProcess: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **to_process** | [**\OpenAPI\Billit\Model\ToProcessSaveRequest**](../Model/ToProcessSaveRequest.md)|  | |

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
