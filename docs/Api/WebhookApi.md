# OpenAPI\Billit\WebhookApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**webhookDeleteWebhooks()**](WebhookApi.md#webhookDeleteWebhooks) | **DELETE** /v1/webhooks/{webhookID} | Delete a webhook |
| [**webhookGetWebhooks()**](WebhookApi.md#webhookGetWebhooks) | **GET** /v1/webhooks | Get all webhooks |
| [**webhookPostWebhook()**](WebhookApi.md#webhookPostWebhook) | **POST** /v1/webhooks | Create a webhook |
| [**webhookRefreshWebhookSecret()**](WebhookApi.md#webhookRefreshWebhookSecret) | **POST** /v1/webhooks/refresh/{webhookID} | Refresh a webhook secret |


## `webhookDeleteWebhooks()`

```php
webhookDeleteWebhooks($webhook_id): bool
```

Delete a webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$webhook_id = 56; // int

try {
    $result = $apiInstance->webhookDeleteWebhooks($webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookDeleteWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `webhookGetWebhooks()`

```php
webhookGetWebhooks(): \OpenAPI\Billit\Model\Webhook[]
```

Get all webhooks

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->webhookGetWebhooks();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookGetWebhooks: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

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

## `webhookPostWebhook()`

```php
webhookPostWebhook($webhook): \OpenAPI\Billit\Model\Webhook
```

Create a webhook

Sample request:                    POST /v1/webhooks      {         \"EntityType\": \"Order\",         \"WebhookURL\": \"https://my.Webhook.url.com/Callback\"      }

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$webhook = new \OpenAPI\Billit\Model\Webhook(); // \OpenAPI\Billit\Model\Webhook

try {
    $result = $apiInstance->webhookPostWebhook($webhook);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookPostWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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

## `webhookRefreshWebhookSecret()`

```php
webhookRefreshWebhookSecret($webhook_id): string
```

Refresh a webhook secret

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$webhook_id = 56; // int

try {
    $result = $apiInstance->webhookRefreshWebhookSecret($webhook_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhookRefreshWebhookSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
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
