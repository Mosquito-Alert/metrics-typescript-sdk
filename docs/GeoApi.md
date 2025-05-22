# GeoApi

All URIs are relative to *http://localhost:8000/api/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**tilesRetrieve**](#tilesretrieve) | **GET** /geo/tiles/{z}/{x}/{y} | |

# **tilesRetrieve**
> tilesRetrieve()

ViewSet for the Municipality model with MVT rendering.

### Example

```typescript
import {
    GeoApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new GeoApi(configuration);

let x: number; // (default to undefined)
let y: number; // (default to undefined)
let z: number; // (default to undefined)

const { status, data } = await apiInstance.tilesRetrieve(
    x,
    y,
    z
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **x** | [**number**] |  | defaults to undefined|
| **y** | [**number**] |  | defaults to undefined|
| **z** | [**number**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | No response body |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

