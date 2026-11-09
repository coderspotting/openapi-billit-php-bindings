# OpenAPI\Billit\OAuth2Api



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**oAuth2PostToken()**](OAuth2Api.md#oAuth2PostToken) | **POST** /OAuth2/token |  |
| [**oAuth2PostTokenRevoke()**](OAuth2Api.md#oAuth2PostTokenRevoke) | **POST** /OAuth2/revoke |  |


## `oAuth2PostToken()`

```php
oAuth2PostToken($o_auth_access_token_request): object
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OAuth2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$o_auth_access_token_request = new \OpenAPI\Billit\Model\OAuthAccessTokenRequest(); // \OpenAPI\Billit\Model\OAuthAccessTokenRequest

try {
    $result = $apiInstance->oAuth2PostToken($o_auth_access_token_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuth2Api->oAuth2PostToken: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **o_auth_access_token_request** | [**\OpenAPI\Billit\Model\OAuthAccessTokenRequest**](../Model/OAuthAccessTokenRequest.md)|  | |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/xml`, `text/xml`, `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `oAuth2PostTokenRevoke()`

```php
oAuth2PostTokenRevoke(): object
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\OAuth2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->oAuth2PostTokenRevoke();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OAuth2Api->oAuth2PostTokenRevoke: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
