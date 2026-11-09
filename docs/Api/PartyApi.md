# OpenAPI\Billit\PartyApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**partyGetParties()**](PartyApi.md#partyGetParties) | **GET** /v1/parties | Get a list of customers or suppliers |
| [**partyGetParty()**](PartyApi.md#partyGetParty) | **GET** /v1/parties/{partyID} | Get a party specified by the partyID |
| [**partyPatchParties()**](PartyApi.md#partyPatchParties) | **PATCH** /v1/parties/{partyID} | Patch Party Properties. NavigationProperties are not supported. |
| [**partyPostParty()**](PartyApi.md#partyPostParty) | **POST** /v1/parties | Create a new party or update an existing one |


## `partyGetParties()`

```php
partyGetParties($full_text_search): \OpenAPI\Billit\Model\PageResultParty
```

Get a list of customers or suppliers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PartyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$full_text_search = 'full_text_search_example'; // string

try {
    $result = $apiInstance->partyGetParties($full_text_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyApi->partyGetParties: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **full_text_search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\PageResultParty**](../Model/PageResultParty.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyGetParty()`

```php
partyGetParty($party_id): \OpenAPI\Billit\Model\Party
```

Get a party specified by the partyID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PartyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$party_id = 56; // int

try {
    $result = $apiInstance->partyGetParty($party_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyApi->partyGetParty: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **party_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\Party**](../Model/Party.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `partyPatchParties()`

```php
partyPatchParties($party_id, $delta)
```

Patch Party Properties. NavigationProperties are not supported.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PartyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$party_id = 56; // int
$delta = array('key' => new \stdClass); // object

try {
    $apiInstance->partyPatchParties($party_id, $delta);
} catch (Exception $e) {
    echo 'Exception when calling PartyApi->partyPatchParties: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **party_id** | **int**|  | |
| **delta** | **object**|  | |

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

## `partyPostParty()`

```php
partyPostParty($party): int
```

Create a new party or update an existing one

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PartyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$party = new \OpenAPI\Billit\Model\Party(); // \OpenAPI\Billit\Model\Party

try {
    $result = $apiInstance->partyPostParty($party);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartyApi->partyPostParty: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **party** | [**\OpenAPI\Billit\Model\Party**](../Model/Party.md)|  | |

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
