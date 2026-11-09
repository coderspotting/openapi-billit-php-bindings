# OpenAPI\Billit\ReportApi



All URIs are relative to https://api.billit.be, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**reportReportDetailGet()**](ReportApi.md#reportReportDetailGet) | **GET** /v1/reports/{reportID} | Get the result and name of the report specified by the reportID |
| [**reportReportListGet()**](ReportApi.md#reportReportListGet) | **GET** /v1/reports | Get a list of available reports for the current user |


## `reportReportDetailGet()`

```php
reportReportDetailGet($report_id): \OpenAPI\Billit\Model\ReportDetailModel
```

Get the result and name of the report specified by the reportID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ReportApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$report_id = 56; // int

try {
    $result = $apiInstance->reportReportDetailGet($report_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportApi->reportReportDetailGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **report_id** | **int**|  | |

### Return type

[**\OpenAPI\Billit\Model\ReportDetailModel**](../Model/ReportDetailModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reportReportListGet()`

```php
reportReportListGet(): \OpenAPI\Billit\Model\ReportsExportOverViewModel[]
```

Get a list of available reports for the current user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Billit\Api\ReportApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->reportReportListGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportApi->reportReportListGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Billit\Model\ReportsExportOverViewModel[]**](../Model/ReportsExportOverViewModel.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
