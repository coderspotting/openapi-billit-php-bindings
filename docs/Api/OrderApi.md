# OpenAPI\Billit\OrderApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**orderDeleteOrder()**](OrderApi.md#orderDeleteOrder) | **DELETE** /v1/orders/{orderID} | Delete a specific order |
| [**orderESignOrder()**](OrderApi.md#orderESignOrder) | **POST** /v1/orders/commands/eSign/{orderID} | E-Sign an order |
| [**orderGetDeleted()**](OrderApi.md#orderGetDeleted) | **GET** /v1/orders/deleted | Get a list of deleted orders |
| [**orderGetOrder()**](OrderApi.md#orderGetOrder) | **GET** /v1/orders/{orderID} | Get a specific order |
| [**orderGetOrders()**](OrderApi.md#orderGetOrders) | **GET** /v1/orders | Get a list of invoices/credit notes/order/... |
| [**orderPatchOrders()**](OrderApi.md#orderPatchOrders) | **PATCH** /v1/orders/{orderID} | Patch an order |
| [**orderPostOrderPayment()**](OrderApi.md#orderPostOrderPayment) | **POST** /v1/orders/{orderID}/payments | Add a partial or full payment to an order |
| [**orderPostOrders()**](OrderApi.md#orderPostOrders) | **POST** /v1/orders | Create a new order or update an existing one |
| [**orderPostSend()**](OrderApi.md#orderPostSend) | **POST** /v1/orders/commands/send | Send a list of orders via a specified channel |
| [**orderPutOrderBookings()**](OrderApi.md#orderPutOrderBookings) | **PUT** /v1/orders/{orderID}/bookingEntries | Add a booking lines collection |


## `orderDeleteOrder()`

```php
orderDeleteOrder($order_id): bool
```

Delete a specific order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = 56; // int

try {
    $result = $apiInstance->orderDeleteOrder($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderDeleteOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **int**|  | |

### Return type

**bool**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderESignOrder()`

```php
orderESignOrder($order_id): bool
```

E-Sign an order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = 56; // int

try {
    $result = $apiInstance->orderESignOrder($order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderESignOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **int**|  | |

### Return type

**bool**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderGetDeleted()`

```php
orderGetDeleted(): \OpenAPI\Billit\Model\PageResultOrder
```

Get a list of deleted orders

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->orderGetDeleted();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderGetDeleted: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\PageResultOrder**](../Model/PageResultOrder.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderGetOrder()`

```php
orderGetOrder($order_id, $document_type): \OpenAPI\Billit\Model\Order
```

Get a specific order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = 56; // int
$document_type = 'document_type_example'; // string

try {
    $result = $apiInstance->orderGetOrder($order_id, $document_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderGetOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **int**|  | |
| **document_type** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\Order**](../Model/Order.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderGetOrders()`

```php
orderGetOrders($full_text_search): \OpenAPI\Billit\Model\PageResultOrder
```

Get a list of invoices/credit notes/order/...

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$full_text_search = 'full_text_search_example'; // string

try {
    $result = $apiInstance->orderGetOrders($full_text_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderGetOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **full_text_search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Billit\Model\PageResultOrder**](../Model/PageResultOrder.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderPatchOrders()`

```php
orderPatchOrders($order_id, $delta)
```

Patch an order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = 56; // int
$delta = array('key' => new \stdClass); // object

try {
    $apiInstance->orderPatchOrders($order_id, $delta);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPatchOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **int**|  | |
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

## `orderPostOrderPayment()`

```php
orderPostOrderPayment($order_id, $data)
```

Add a partial or full payment to an order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = 56; // int
$data = new \OpenAPI\Billit\Model\PostPaymentRequest(); // \OpenAPI\Billit\Model\PostPaymentRequest

try {
    $apiInstance->orderPostOrderPayment($order_id, $data);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPostOrderPayment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **int**|  | |
| **data** | [**\OpenAPI\Billit\Model\PostPaymentRequest**](../Model/PostPaymentRequest.md)|  | |

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

## `orderPostOrders()`

```php
orderPostOrders($order): int
```

Create a new order or update an existing one

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order = new \OpenAPI\Billit\Model\Order(); // \OpenAPI\Billit\Model\Order

try {
    $result = $apiInstance->orderPostOrders($order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPostOrders: ', $e->getMessage(), PHP_EOL;
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

## `orderPostSend()`

```php
orderPostSend($send_request)
```

Send a list of orders via a specified channel

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$send_request = new \OpenAPI\Billit\Model\SendRequest(); // \OpenAPI\Billit\Model\SendRequest

try {
    $apiInstance->orderPostSend($send_request);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPostSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **send_request** | [**\OpenAPI\Billit\Model\SendRequest**](../Model/SendRequest.md)|  | |

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

## `orderPutOrderBookings()`

```php
orderPutOrderBookings($order_id, $booking_entries)
```

Add a booking lines collection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$order_id = 56; // int
$booking_entries = array(new \OpenAPI\Billit\Model\BookingEntry()); // \OpenAPI\Billit\Model\BookingEntry[]

try {
    $apiInstance->orderPutOrderBookings($order_id, $booking_entries);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPutOrderBookings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **int**|  | |
| **booking_entries** | [**\OpenAPI\Billit\Model\BookingEntry[]**](../Model/BookingEntry.md)|  | |

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
