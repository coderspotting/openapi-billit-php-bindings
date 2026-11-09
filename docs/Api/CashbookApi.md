# OpenAPI\Billit\CashbookApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**cashbookCloseCashbook()**](CashbookApi.md#cashbookCloseCashbook) | **POST** /v1/Cashbook/Close | Permanently close the cash book |
| [**cashbookGetCashbook()**](CashbookApi.md#cashbookGetCashbook) | **GET** /v1/Cashbook | Get the current active cash book |
| [**cashbookGetCashbookEntries()**](CashbookApi.md#cashbookGetCashbookEntries) | **GET** /v1/Cashbook/Entries | Get an overview of all the entries in the current active cash book |
| [**cashbookGetCashbookHistory()**](CashbookApi.md#cashbookGetCashbookHistory) | **GET** /v1/Cashbook/{cashbookID}/History | Get an overview of all the entries in a closed cash book |
| [**cashbookGetCashbooks()**](CashbookApi.md#cashbookGetCashbooks) | **GET** /v1/Cashbook/History | Get an overview of all the closed cash books |
| [**cashbookInitializeCashbook()**](CashbookApi.md#cashbookInitializeCashbook) | **POST** /v1/Cashbook/Initialize | Initialize the cash book for first use |
| [**cashbookPostCashbookEntry()**](CashbookApi.md#cashbookPostCashbookEntry) | **POST** /v1/Cashbook/AddEntry | Add an entry to the current active cash book |


## `cashbookCloseCashbook()`

```php
cashbookCloseCashbook()
```

Permanently close the cash book

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->cashbookCloseCashbook();
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookCloseCashbook: ', $e->getMessage(), PHP_EOL;
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

## `cashbookGetCashbook()`

```php
cashbookGetCashbook(): \OpenAPI\Billit\Model\CashbookModel
```

Get the current active cash book

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->cashbookGetCashbook();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookGetCashbook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\CashbookModel**](../Model/CashbookModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cashbookGetCashbookEntries()`

```php
cashbookGetCashbookEntries($full_text_search): \OpenAPI\Billit\Model\PageResultCashbookEntry
```

Get an overview of all the entries in the current active cash book

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$full_text_search = 'full_text_search_example'; // string

try {
    $result = $apiInstance->cashbookGetCashbookEntries($full_text_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookGetCashbookEntries: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **full_text_search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\PageResultCashbookEntry**](../Model/PageResultCashbookEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cashbookGetCashbookHistory()`

```php
cashbookGetCashbookHistory($cashbook_id, $full_text_search): \OpenAPI\Billit\Model\PageResultCashbookEntry
```

Get an overview of all the entries in a closed cash book

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cashbook_id = 56; // int
$full_text_search = 'full_text_search_example'; // string

try {
    $result = $apiInstance->cashbookGetCashbookHistory($cashbook_id, $full_text_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookGetCashbookHistory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cashbook_id** | **int**|  | |
| **full_text_search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\PageResultCashbookEntry**](../Model/PageResultCashbookEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cashbookGetCashbooks()`

```php
cashbookGetCashbooks(): \OpenAPI\Billit\Model\CashbookModel[]
```

Get an overview of all the closed cash books

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->cashbookGetCashbooks();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookGetCashbooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\CashbookModel[]**](../Model/CashbookModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `cashbookInitializeCashbook()`

```php
cashbookInitializeCashbook($cashbook_initialization): int
```

Initialize the cash book for first use

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cashbook_initialization = new \OpenAPI\Billit\Model\CashbookInitialization(); // \OpenAPI\Billit\Model\CashbookInitialization

try {
    $result = $apiInstance->cashbookInitializeCashbook($cashbook_initialization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookInitializeCashbook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cashbook_initialization** | [**\OpenAPI\Billit\Model\CashbookInitialization**](../Model/CashbookInitialization.md)|  | |

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

## `cashbookPostCashbookEntry()`

```php
cashbookPostCashbookEntry($cashbook_input_entry): \OpenAPI\Billit\Model\CashbookEntry
```

Add an entry to the current active cash book

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\CashbookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$cashbook_input_entry = new \OpenAPI\Billit\Model\CashbookEntry(); // \OpenAPI\Billit\Model\CashbookEntry

try {
    $result = $apiInstance->cashbookPostCashbookEntry($cashbook_input_entry);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CashbookApi->cashbookPostCashbookEntry: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **cashbook_input_entry** | [**\OpenAPI\Billit\Model\CashbookEntry**](../Model/CashbookEntry.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\CashbookEntry**](../Model/CashbookEntry.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
