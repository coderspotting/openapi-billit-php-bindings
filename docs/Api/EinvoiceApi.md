# OpenAPI\Billit\EinvoiceApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**einvoiceDeleteRegistration()**](EinvoiceApi.md#einvoiceDeleteRegistration) | **DELETE** /v1/einvoices/registrations/{registrationID} | Delete a registration |
| [**einvoiceDeleteRegistrationIntegration()**](EinvoiceApi.md#einvoiceDeleteRegistrationIntegration) | **DELETE** /v1/einvoices/registrations/{registrationID}/integrations/{integrationID} | Deactivate an integration |
| [**einvoiceDeleteWebhooks()**](EinvoiceApi.md#einvoiceDeleteWebhooks) | **DELETE** /v1/einvoices/registrations/{registrationID}/webhooks/{webhookID} | Delete a webhook |
| [**einvoiceGetFile()**](EinvoiceApi.md#einvoiceGetFile) | **GET** /v1/einvoices/registrations/{registrationID}/files/{fileID} | Get a file specified by the fileID |
| [**einvoiceGetOrder()**](EinvoiceApi.md#einvoiceGetOrder) | **GET** /v1/einvoices/registrations/{registrationID}/orders/{orderID} | Get an order specified by the orderID |
| [**einvoiceGetOrders()**](EinvoiceApi.md#einvoiceGetOrders) | **GET** /v1/einvoices/registrations/{registrationID}/orders | Get a list of orders |
| [**einvoiceGetRegistration()**](EinvoiceApi.md#einvoiceGetRegistration) | **GET** /v1/einvoices/registrations/{registrationID} | Retrieve an E-invoice registration |
| [**einvoiceGetRegistrations()**](EinvoiceApi.md#einvoiceGetRegistrations) | **GET** /v1/einvoices/registrations | Retrieve all E-invoice registrations |
| [**einvoiceGetWebhooks()**](EinvoiceApi.md#einvoiceGetWebhooks) | **GET** /v1/einvoices/registrations/{registrationID}/webhooks | Get all webhooks |
| [**einvoicePatchEntity()**](EinvoiceApi.md#einvoicePatchEntity) | **PATCH** /v1/einvoices/registrations/{registrationID} | Update an E-invoice registration |
| [**einvoicePatchOrder()**](EinvoiceApi.md#einvoicePatchOrder) | **PATCH** /v1/einvoices/registrations/{registrationID}/orders/{orderID} | Patch an E-document |
| [**einvoicePostKYCInitiation()**](EinvoiceApi.md#einvoicePostKYCInitiation) | **POST** /v1/einvoices/registrations/{registrationID}/identification | Initiate a KYC procedure |
| [**einvoicePostRegistration()**](EinvoiceApi.md#einvoicePostRegistration) | **POST** /v1/einvoices/registrations | Create an E-invoice registration for a new entity |
| [**einvoicePostRegistrationIntegration()**](EinvoiceApi.md#einvoicePostRegistrationIntegration) | **POST** /v1/einvoices/registrations/{registrationID}/integrations | Activate a new integration |
| [**einvoicePostSend()**](EinvoiceApi.md#einvoicePostSend) | **POST** /v1/einvoices/registrations/{registrationID}/commands/send | Create and send an E-document |
| [**einvoicePostWebhook()**](EinvoiceApi.md#einvoicePostWebhook) | **POST** /v1/einvoices/registrations/{registrationID}/webhooks | Create a webhook |
| [**einvoiceRefreshWebhookSecret()**](EinvoiceApi.md#einvoiceRefreshWebhookSecret) | **POST** /v1/einvoices/registrations/{registrationID}/webhooks/refresh/{webhookID} | Refresh an webhook secret |


## `einvoiceDeleteRegistration()`

```php
einvoiceDeleteRegistration($registration_id): bool
```

Delete a registration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int

try {
    $result = $apiInstance->einvoiceDeleteRegistration($registration_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceDeleteRegistration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |

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

## `einvoiceDeleteRegistrationIntegration()`

```php
einvoiceDeleteRegistrationIntegration($registration_id, $integration_id): bool
```

Deactivate an integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$integration_id = 56; // int

try {
    $result = $apiInstance->einvoiceDeleteRegistrationIntegration($registration_id, $integration_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceDeleteRegistrationIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **integration_id** | **int**|  | |

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

## `einvoiceDeleteWebhooks()`

```php
einvoiceDeleteWebhooks($registration_id, $webhook_id): bool
```

Delete a webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$webhook_id = 56; // int

try {
    $result = $apiInstance->einvoiceDeleteWebhooks($registration_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceDeleteWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **webhook_id** | **int**|  | |

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

## `einvoiceGetFile()`

```php
einvoiceGetFile($registration_id, $file_id): \OpenAPI\Billit\Model\File
```

Get a file specified by the fileID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$file_id = 'file_id_example'; // string

try {
    $result = $apiInstance->einvoiceGetFile($registration_id, $file_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceGetFile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
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

## `einvoiceGetOrder()`

```php
einvoiceGetOrder($registration_id, $order_id): \OpenAPI\Billit\Model\Order
```

Get an order specified by the orderID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$order_id = 56; // int

try {
    $result = $apiInstance->einvoiceGetOrder($registration_id, $order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceGetOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **order_id** | **int**|  | |

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

## `einvoiceGetOrders()`

```php
einvoiceGetOrders($registration_id, $full_text_search): \OpenAPI\Billit\Model\PageResultOrder
```

Get a list of orders

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$full_text_search = 'full_text_search_example'; // string

try {
    $result = $apiInstance->einvoiceGetOrders($registration_id, $full_text_search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceGetOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
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

## `einvoiceGetRegistration()`

```php
einvoiceGetRegistration($registration_id): \OpenAPI\Billit\Model\GetEinvoiceAccountsReponse
```

Retrieve an E-invoice registration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int

try {
    $result = $apiInstance->einvoiceGetRegistration($registration_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceGetRegistration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\GetEinvoiceAccountsReponse**](../Model/GetEinvoiceAccountsReponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoiceGetRegistrations()`

```php
einvoiceGetRegistrations(): \OpenAPI\Billit\Model\GetEinvoiceAccountsReponse
```

Retrieve all E-invoice registrations

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->einvoiceGetRegistrations();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceGetRegistrations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\GetEinvoiceAccountsReponse**](../Model/GetEinvoiceAccountsReponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoiceGetWebhooks()`

```php
einvoiceGetWebhooks($registration_id): \OpenAPI\Billit\Model\Webhook[]
```

Get all webhooks

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int

try {
    $result = $apiInstance->einvoiceGetWebhooks($registration_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceGetWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\Webhook[]**](../Model/Webhook.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoicePatchEntity()`

```php
einvoicePatchEntity($registration_id, $einvoice_registration_patch): bool
```

Update an E-invoice registration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$einvoice_registration_patch = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->einvoicePatchEntity($registration_id, $einvoice_registration_patch);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePatchEntity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **einvoice_registration_patch** | **object**|  | |

### Return type

**bool**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoicePatchOrder()`

```php
einvoicePatchOrder($registration_id, $order_id, $delta)
```

Patch an E-document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$order_id = 56; // int
$delta = array('key' => new \stdClass); // object

try {
    $apiInstance->einvoicePatchOrder($registration_id, $order_id, $delta);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePatchOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
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

## `einvoicePostKYCInitiation()`

```php
einvoicePostKYCInitiation($registration_id, $post): \OpenAPI\Billit\Model\KYCInitiationResponse
```

Initiate a KYC procedure

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$post = new \OpenAPI\Billit\Model\KYCInitiationPost(); // \OpenAPI\Billit\Model\KYCInitiationPost

try {
    $result = $apiInstance->einvoicePostKYCInitiation($registration_id, $post);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePostKYCInitiation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **post** | [**\OpenAPI\Billit\Model\KYCInitiationPost**](../Model/KYCInitiationPost.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\KYCInitiationResponse**](../Model/KYCInitiationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoicePostRegistration()`

```php
einvoicePostRegistration($registration_request): \OpenAPI\Billit\Model\AccountRegistrationResponse
```

Create an E-invoice registration for a new entity

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_request = new \OpenAPI\Billit\Model\EinvoiceRegistrationPost(); // \OpenAPI\Billit\Model\EinvoiceRegistrationPost

try {
    $result = $apiInstance->einvoicePostRegistration($registration_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePostRegistration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_request** | [**\OpenAPI\Billit\Model\EinvoiceRegistrationPost**](../Model/EinvoiceRegistrationPost.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\AccountRegistrationResponse**](../Model/AccountRegistrationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoicePostRegistrationIntegration()`

```php
einvoicePostRegistrationIntegration($registration_id, $post): \OpenAPI\Billit\Model\EinvoiceIntegration
```

Activate a new integration

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$post = new \OpenAPI\Billit\Model\IntegrationPost(); // \OpenAPI\Billit\Model\IntegrationPost

try {
    $result = $apiInstance->einvoicePostRegistrationIntegration($registration_id, $post);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePostRegistrationIntegration: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **post** | [**\OpenAPI\Billit\Model\IntegrationPost**](../Model/IntegrationPost.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\EinvoiceIntegration**](../Model/EinvoiceIntegration.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoicePostSend()`

```php
einvoicePostSend($registration_id, $send_request): \OpenAPI\Billit\Model\CreateAndSendEdocumentResponse
```

Create and send an E-document

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$send_request = new \OpenAPI\Billit\Model\CreateAndSendEDocumentPost(); // \OpenAPI\Billit\Model\CreateAndSendEDocumentPost

try {
    $result = $apiInstance->einvoicePostSend($registration_id, $send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePostSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **send_request** | [**\OpenAPI\Billit\Model\CreateAndSendEDocumentPost**](../Model/CreateAndSendEDocumentPost.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\CreateAndSendEdocumentResponse**](../Model/CreateAndSendEdocumentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoicePostWebhook()`

```php
einvoicePostWebhook($registration_id, $webhook): \OpenAPI\Billit\Model\Webhook
```

Create a webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$webhook = new \OpenAPI\Billit\Model\Webhook(); // \OpenAPI\Billit\Model\Webhook

try {
    $result = $apiInstance->einvoicePostWebhook($registration_id, $webhook);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoicePostWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **webhook** | [**\OpenAPI\Billit\Model\Webhook**](../Model/Webhook.md)|  | |

### Return type

[**\OpenAPI\Billit\Model\Webhook**](../Model/Webhook.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `einvoiceRefreshWebhookSecret()`

```php
einvoiceRefreshWebhookSecret($registration_id, $webhook_id): string
```

Refresh an webhook secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\EinvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$registration_id = 56; // int
$webhook_id = 56; // int

try {
    $result = $apiInstance->einvoiceRefreshWebhookSecret($registration_id, $webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EinvoiceApi->einvoiceRefreshWebhookSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **registration_id** | **int**|  | |
| **webhook_id** | **int**|  | |

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
