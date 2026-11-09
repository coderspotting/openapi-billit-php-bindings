# OpenAPI\Billit\MiscApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**miscGetCompanySearch()**](MiscApi.md#miscGetCompanySearch) | **GET** /v1/misc/companysearch/{Keywords} | Search for parties/companies based on a keyword |
| [**miscGetTranslation()**](MiscApi.md#miscGetTranslation) | **GET** /v1/misc/typecodes/{TypeCodeType}/{key}/{language} | Get a translations of a key of a typecode, optionally in a specified language |
| [**miscGetTypeCodes()**](MiscApi.md#miscGetTypeCodes) | **GET** /v1/misc/typecodes/{TypeCodeType} | Get all translations of a specified TypeCode |


## `miscGetCompanySearch()`

```php
miscGetCompanySearch($keywords): \OpenAPI\Billit\Model\CompanySearchResult
```

Search for parties/companies based on a keyword

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\MiscApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$keywords = 'keywords_example'; // string

try {
    $result = $apiInstance->miscGetCompanySearch($keywords);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscApi->miscGetCompanySearch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **keywords** | **string**|  | |

### Return type

[**\OpenAPI\Billit\Model\CompanySearchResult**](../Model/CompanySearchResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `miscGetTranslation()`

```php
miscGetTranslation($type_code_type, $key, $language): \OpenAPI\Billit\Model\TypeCodeResult
```

Get a translations of a key of a typecode, optionally in a specified language

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\MiscApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type_code_type = 'type_code_type_example'; // string
$key = 'key_example'; // string
$language = 'language_example'; // string

try {
    $result = $apiInstance->miscGetTranslation($type_code_type, $key, $language);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscApi->miscGetTranslation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **type_code_type** | **string**|  | |
| **key** | **string**|  | |
| **language** | **string**|  | |

### Return type

[**\OpenAPI\Billit\Model\TypeCodeResult**](../Model/TypeCodeResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `miscGetTypeCodes()`

```php
miscGetTypeCodes($type_code_type): \OpenAPI\Billit\Model\TypeCodeResult
```

Get all translations of a specified TypeCode

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\MiscApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$type_code_type = 'type_code_type_example'; // string

try {
    $result = $apiInstance->miscGetTypeCodes($type_code_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MiscApi->miscGetTypeCodes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **type_code_type** | **string**|  | |

### Return type

[**\OpenAPI\Billit\Model\TypeCodeResult**](../Model/TypeCodeResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
