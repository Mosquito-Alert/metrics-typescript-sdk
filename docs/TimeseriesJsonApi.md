# TimeseriesJsonApi

All URIs are relative to *https://metrics.mosquitoalert.com/api/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**jsonRetrieve**](#jsonretrieve) | **GET** /timeseries-json/ | |

# **jsonRetrieve**
> jsonRetrieve()


### Example

```typescript
import {
    TimeseriesJsonApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new TimeseriesJsonApi(configuration);

let date: string; //Date of the results to return. (default to undefined)
let days: number; //Number of days to return in the time series. (optional) (default to undefined)

const { status, data } = await apiInstance.jsonRetrieve(
    date,
    days
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **date** | [**string**] | Date of the results to return. | defaults to undefined|
| **days** | [**number**] | Number of days to return in the time series. | (optional) defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | No response body |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

