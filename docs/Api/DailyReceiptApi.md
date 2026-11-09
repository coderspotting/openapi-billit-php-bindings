# OpenAPI\Billit\DailyReceiptApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**dailyReceiptGetDailyReceiptBooks()**](DailyReceiptApi.md#dailyReceiptGetDailyReceiptBooks) | **GET** /v1/DailyReceiptBooks/{DailyReceiptBookID} | Get a daily receipt book with details |
| [**dailyReceiptGetDailyReceiptBooks_0()**](DailyReceiptApi.md#dailyReceiptGetDailyReceiptBooks_0) | **GET** /v1/DailyReceiptBooks | Get a daily receipt book list |
| [**dailyReceiptGetDailyReceiptEntry()**](DailyReceiptApi.md#dailyReceiptGetDailyReceiptEntry) | **GET** /v1/DailyReceiptBooks/DailyReceiptEntry/{DailyReceiptEntryID} | Get a daily receipt entry |
| [**dailyReceiptPostDailyReceiptBookEntry()**](DailyReceiptApi.md#dailyReceiptPostDailyReceiptBookEntry) | **POST** /v1/DailyReceiptBooks/commands/CreateEntryInOpenExistingOrNew | Add a new daily receipt to a new or open daily receipt book |


## `dailyReceiptGetDailyReceiptBooks()`

```php
dailyReceiptGetDailyReceiptBooks($daily_receipt_book_id): \OpenAPI\Billit\Model\DailyReceiptBookModelResponseModel
```

Get a daily receipt book with details

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DailyReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$daily_receipt_book_id = 56; // int

try {
    $result = $apiInstance->dailyReceiptGetDailyReceiptBooks($daily_receipt_book_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DailyReceiptApi->dailyReceiptGetDailyReceiptBooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **daily_receipt_book_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\DailyReceiptBookModelResponseModel**](../Model/DailyReceiptBookModelResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dailyReceiptGetDailyReceiptBooks_0()`

```php
dailyReceiptGetDailyReceiptBooks_0(): \OpenAPI\Billit\Model\DailyReceiptBookModelResponseModel
```

Get a daily receipt book list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DailyReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->dailyReceiptGetDailyReceiptBooks_0();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DailyReceiptApi->dailyReceiptGetDailyReceiptBooks_0: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\DailyReceiptBookModelResponseModel**](../Model/DailyReceiptBookModelResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dailyReceiptGetDailyReceiptEntry()`

```php
dailyReceiptGetDailyReceiptEntry($daily_receipt_entry_id): \OpenAPI\Billit\Model\GetDailyReceiptEntryResponseModel
```

Get a daily receipt entry

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DailyReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$daily_receipt_entry_id = 56; // int

try {
    $result = $apiInstance->dailyReceiptGetDailyReceiptEntry($daily_receipt_entry_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DailyReceiptApi->dailyReceiptGetDailyReceiptEntry: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **daily_receipt_entry_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\GetDailyReceiptEntryResponseModel**](../Model/GetDailyReceiptEntryResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `dailyReceiptPostDailyReceiptBookEntry()`

```php
dailyReceiptPostDailyReceiptBookEntry($daily_receipt_entry): \OpenAPI\Billit\Model\PostDailyReceiptBookEntryResponseModel
```

Add a new daily receipt to a new or open daily receipt book

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\DailyReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$daily_receipt_entry = new \OpenAPI\Billit\Model\DailyReceiptBookEntryModel(); // \OpenAPI\Billit\Model\DailyReceiptBookEntryModel

try {
    $result = $apiInstance->dailyReceiptPostDailyReceiptBookEntry($daily_receipt_entry);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DailyReceiptApi->dailyReceiptPostDailyReceiptBookEntry: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **daily_receipt_entry** | [**\OpenAPI\Billit\Model\DailyReceiptBookEntryModel**](../Model/DailyReceiptBookEntryModel.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\PostDailyReceiptBookEntryResponseModel**](../Model/PostDailyReceiptBookEntryResponseModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
