# OpenAPI\Billit\PeppolApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**peppolDeleteParticipant()**](PeppolApi.md#peppolDeleteParticipant) | **DELETE** /v1/peppol/participants | Delete a Peppol registration for a specific company |
| [**peppolGetInbox()**](PeppolApi.md#peppolGetInbox) | **GET** /v1/peppol/inbox | Lists the first 10 peppol items in the inbox. Use the file api to download the actual message. Use the confirm or refuse endpoint to remove it from the queue |
| [**peppolGetParticipantInformation()**](PeppolApi.md#peppolGetParticipantInformation) | **GET** /v1/peppol/participantInformation/{VATorCBE} | Get Peppol participant information. API key is not required |
| [**peppolInboxItemConfirm()**](PeppolApi.md#peppolInboxItemConfirm) | **POST** /v1/peppol/inbox/{inboxItemId}/confirm | Confirm an inbox item and remove it from the queue |
| [**peppolInboxItemRefuse()**](PeppolApi.md#peppolInboxItemRefuse) | **POST** /v1/peppol/inbox/{inboxItemId}/refuse | Refuse an inbox item and remove it from the queue |
| [**peppolPostParticipant()**](PeppolApi.md#peppolPostParticipant) | **POST** /v1/peppol/participants | Create a new Peppol registration for a specific company |
| [**peppolPostSendOrder()**](PeppolApi.md#peppolPostSendOrder) | **POST** /v1/peppol/sendOrder | Send a direct Peppol message. Compatible with receivers that support Invoice5, Creditnote5, BisV3 Invoice or BisV3 Creditnote |


## `peppolDeleteParticipant()`

```php
peppolDeleteParticipant($register_request)
```

Delete a Peppol registration for a specific company

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$register_request = new \OpenAPI\Billit\Model\DeleteParticipantRequest(); // \OpenAPI\Billit\Model\DeleteParticipantRequest

try {
    $apiInstance->peppolDeleteParticipant($register_request);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolDeleteParticipant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **register_request** | [**\OpenAPI\Billit\Model\DeleteParticipantRequest**](../Model/DeleteParticipantRequest.md)|  | |

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

## `peppolGetInbox()`

```php
peppolGetInbox($receiver_company_id): \OpenAPI\Billit\Model\InboxGetResult
```

Lists the first 10 peppol items in the inbox. Use the file api to download the actual message. Use the confirm or refuse endpoint to remove it from the queue

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$receiver_company_id = 'receiver_company_id_example'; // string

try {
    $result = $apiInstance->peppolGetInbox($receiver_company_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolGetInbox: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **receiver_company_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\InboxGetResult**](../Model/InboxGetResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `peppolGetParticipantInformation()`

```php
peppolGetParticipantInformation($va_tor_cbe, $only_check_dns): \OpenAPI\Billit\Model\ParticipantInformationResponse
```

Get Peppol participant information. API key is not required

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$va_tor_cbe = 'va_tor_cbe_example'; // string
$only_check_dns = True; // bool

try {
    $result = $apiInstance->peppolGetParticipantInformation($va_tor_cbe, $only_check_dns);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolGetParticipantInformation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **va_tor_cbe** | **string**|  | |
| **only_check_dns** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\ParticipantInformationResponse**](../Model/ParticipantInformationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `peppolInboxItemConfirm()`

```php
peppolInboxItemConfirm($inbox_item_id)
```

Confirm an inbox item and remove it from the queue

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$inbox_item_id = 56; // int

try {
    $apiInstance->peppolInboxItemConfirm($inbox_item_id);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolInboxItemConfirm: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inbox_item_id** | **int**|  | |

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

## `peppolInboxItemRefuse()`

```php
peppolInboxItemRefuse($inbox_item_id, $request)
```

Refuse an inbox item and remove it from the queue

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$inbox_item_id = 56; // int
$request = new \OpenAPI\Billit\Model\RefusePeppolItemRequest(); // \OpenAPI\Billit\Model\RefusePeppolItemRequest

try {
    $apiInstance->peppolInboxItemRefuse($inbox_item_id, $request);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolInboxItemRefuse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inbox_item_id** | **int**|  | |
| **request** | [**\OpenAPI\Billit\Model\RefusePeppolItemRequest**](../Model/RefusePeppolItemRequest.md)|  | |

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

## `peppolPostParticipant()`

```php
peppolPostParticipant($register_request)
```

Create a new Peppol registration for a specific company

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$register_request = new \OpenAPI\Billit\Model\RegisterParticipantRequest(); // \OpenAPI\Billit\Model\RegisterParticipantRequest

try {
    $apiInstance->peppolPostParticipant($register_request);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolPostParticipant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **register_request** | [**\OpenAPI\Billit\Model\RegisterParticipantRequest**](../Model/RegisterParticipantRequest.md)|  | |

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

## `peppolPostSendOrder()`

```php
peppolPostSendOrder($order): int
```

Send a direct Peppol message. Compatible with receivers that support Invoice5, Creditnote5, BisV3 Invoice or BisV3 Creditnote

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\PeppolApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order = new \OpenAPI\Billit\Model\Order(); // \OpenAPI\Billit\Model\Order

try {
    $result = $apiInstance->peppolPostSendOrder($order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PeppolApi->peppolPostSendOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | [**\OpenAPI\Billit\Model\Order**](../Model/Order.md)|  | |

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
