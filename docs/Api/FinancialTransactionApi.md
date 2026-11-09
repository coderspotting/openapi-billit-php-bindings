# OpenAPI\Billit\FinancialTransactionApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**financialTransactionGetBankTransactions()**](FinancialTransactionApi.md#financialTransactionGetBankTransactions) | **GET** /v1/financialTransactions |  |
| [**financialTransactionPostImport()**](FinancialTransactionApi.md#financialTransactionPostImport) | **POST** /v1/financialTransactions/commands/import | Create transactions using a list |
| [**financialTransactionPostImportFile()**](FinancialTransactionApi.md#financialTransactionPostImportFile) | **POST** /v1/financialTransactions/importFile | Upload a coda file and import the transactions |


## `financialTransactionGetBankTransactions()`

```php
financialTransactionGetBankTransactions($full_text_search)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\FinancialTransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$full_text_search = 'full_text_search_example'; // string

try {
    $apiInstance->financialTransactionGetBankTransactions($full_text_search);
} catch (Exception $e) {
    echo 'Exception when calling FinancialTransactionApi->financialTransactionGetBankTransactions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **full_text_search** | **string**|  | [optional] |

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

## `financialTransactionPostImport()`

```php
financialTransactionPostImport($transactions)
```

Create transactions using a list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\FinancialTransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$transactions = array(new \OpenAPI\Billit\Model\Transaction()); // \OpenAPI\Billit\Model\Transaction[]

try {
    $apiInstance->financialTransactionPostImport($transactions);
} catch (Exception $e) {
    echo 'Exception when calling FinancialTransactionApi->financialTransactionPostImport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **transactions** | [**\OpenAPI\Billit\Model\Transaction[]**](../Model/Transaction.md)|  | |

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

## `financialTransactionPostImportFile()`

```php
financialTransactionPostImportFile($import_file)
```

Upload a coda file and import the transactions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\FinancialTransactionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$import_file = new \OpenAPI\Billit\Model\File(); // \OpenAPI\Billit\Model\File

try {
    $apiInstance->financialTransactionPostImportFile($import_file);
} catch (Exception $e) {
    echo 'Exception when calling FinancialTransactionApi->financialTransactionPostImportFile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_file** | [**\OpenAPI\Billit\Model\File**](../Model/File.md)|  | |

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
