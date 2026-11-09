# OpenAPI\Billit\ProductApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**productGetProduct()**](ProductApi.md#productGetProduct) | **GET** /v1/products/{productID} | Get a specific product |
| [**productGetProducts()**](ProductApi.md#productGetProducts) | **GET** /v1/products | Get a list of products |
| [**productPostProduct()**](ProductApi.md#productPostProduct) | **POST** /v1/products | Create a new product or update an existing one |


## `productGetProduct()`

```php
productGetProduct($product_id): \OpenAPI\Billit\Model\Product
```

Get a specific product

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$product_id = 56; // int

try {
    $result = $apiInstance->productGetProduct($product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->productGetProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\Product**](../Model/Product.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productGetProducts()`

```php
productGetProducts(): \OpenAPI\Billit\Model\PageResultProduct
```

Get a list of products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->productGetProducts();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->productGetProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\PageResultProduct**](../Model/PageResultProduct.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productPostProduct()`

```php
productPostProduct($product): int
```

Create a new product or update an existing one

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$product = new \OpenAPI\Billit\Model\Product(); // \OpenAPI\Billit\Model\Product

try {
    $result = $apiInstance->productPostProduct($product);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->productPostProduct: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product** | [**\OpenAPI\Billit\Model\Product**](../Model/Product.md)|  | |

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
