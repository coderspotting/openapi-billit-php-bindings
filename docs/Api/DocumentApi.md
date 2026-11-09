# OpenAPI\Billit\DocumentApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**documentGetDocument()**](DocumentApi.md#documentGetDocument) | **GET** /v1/documents/{documentID} | Get a document specified by the documentID |
| [**documentGetDocuments()**](DocumentApi.md#documentGetDocuments) | **GET** /v1/documents | Get a list of documents |
| [**documentPostDocument()**](DocumentApi.md#documentPostDocument) | **POST** /v1/documents | Save a document |


## `documentGetDocument()`

```php
documentGetDocument($document_id): \OpenAPI\Billit\Model\DocumentAPIView
```

Get a document specified by the documentID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$document_id = 56; // int

try {
    $result = $apiInstance->documentGetDocument($document_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->documentGetDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\DocumentAPIView**](../Model/DocumentAPIView.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `documentGetDocuments()`

```php
documentGetDocuments($full_text_search): \OpenAPI\Billit\Model\PageResultDocumentAPIView
```

Get a list of documents

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$full_text_search = 'full_text_search_example'; // string

try {
    $result = $apiInstance->documentGetDocuments($full_text_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->documentGetDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **full_text_search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\PageResultDocumentAPIView**](../Model/PageResultDocumentAPIView.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `documentPostDocument()`

```php
documentPostDocument($document): int
```

Save a document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$document = new \OpenAPI\Billit\Model\Document(); // \OpenAPI\Billit\Model\Document

try {
    $result = $apiInstance->documentPostDocument($document);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentApi->documentPostDocument: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document** | [**\OpenAPI\Billit\Model\Document**](../Model/Document.md)|  | |

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
