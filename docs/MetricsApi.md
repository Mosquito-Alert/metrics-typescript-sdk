# MetricsApi

All URIs are relative to *http://localhost:8000/api/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**batchCreate**](#batchcreate) | **POST** /metrics/batch/ | |
|[**datesList**](#dateslist) | **GET** /metrics/dates/ | |
|[**lastDateRetrieve**](#lastdateretrieve) | **GET** /metrics/dates/last/ | |
|[**list**](#list) | **GET** /metrics/ | |
|[**retrieve**](#retrieve) | **GET** /metrics/{id}/ | |
|[**seasonalityRetrieve**](#seasonalityretrieve) | **GET** /metrics/{id}/seasonality/ | |
|[**tilesRetrieve**](#tilesretrieve) | **GET** /metrics/tiles/{z}/{x}/{y}/ | |
|[**timeseriesTilesRetrieve**](#timeseriestilesretrieve) | **GET** /metrics/timeseries/tiles/{z}/{x}/{y}/ | |
|[**trendRetrieve**](#trendretrieve) | **GET** /metrics/{id}/trend/ | |

# **batchCreate**
> batchCreate(metricFileRequest)

Action that creates a batch of metrics, and calls a Predictor model to predict values.  The endpoint accepts a **CSV file** with the following filename format: **\"bites_YYYY-MM-DD.csv**\", and with the following columns: **[code, est]**.  The CSV should contain every region for a specific day (specified in the filename), where the \"code\" is the region code and the \"est\" is the value.

### Example

```typescript
import {
    MetricsApi,
    Configuration,
    MetricFileRequest
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let metricFileRequest: MetricFileRequest; //

const { status, data } = await apiInstance.batchCreate(
    metricFileRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **metricFileRequest** | **MetricFileRequest**|  | |


### Return type

void (empty response body)

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: application/json, application/x-www-form-urlencoded, multipart/form-data
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | File processes successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **datesList**
> Array<LastMetricDate> datesList()

Action that returns the all the dates in which there are metrics available.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let ordering: string; //Which field to use when ordering the results. (optional) (default to undefined)

const { status, data } = await apiInstance.datesList(
    ordering
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ordering** | [**string**] | Which field to use when ordering the results. | (optional) defaults to undefined|


### Return type

**Array<LastMetricDate>**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **lastDateRetrieve**
> LastMetricDate lastDateRetrieve()

Action that returns the last date in which there are metrics available.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

const { status, data } = await apiInstance.lastDateRetrieve();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**LastMetricDate**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list**
> PaginatedMetricList list()

ViewSet for Metric model.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let dateFrom: string; //Starting date from which the results will return. (optional) (default to undefined)
let dateTo: string; //Ending date which to the results will return. (optional) (default to undefined)
let ordering: MetricsListOrderingParameter; //Order by `date` (asc) or `-date` (desc) (optional) (default to undefined)
let page: number; //A page number within the paginated result set. (optional) (default to undefined)
let pageSize: number; //Number of results to return per page. (optional) (default to undefined)
let regionCode: string; //Determines the region of the results (history). (optional) (default to undefined)

const { status, data } = await apiInstance.list(
    dateFrom,
    dateTo,
    ordering,
    page,
    pageSize,
    regionCode
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **dateFrom** | [**string**] | Starting date from which the results will return. | (optional) defaults to undefined|
| **dateTo** | [**string**] | Ending date which to the results will return. | (optional) defaults to undefined|
| **ordering** | **MetricsListOrderingParameter** | Order by &#x60;date&#x60; (asc) or &#x60;-date&#x60; (desc) | (optional) defaults to undefined|
| **page** | [**number**] | A page number within the paginated result set. | (optional) defaults to undefined|
| **pageSize** | [**number**] | Number of results to return per page. | (optional) defaults to undefined|
| **regionCode** | [**string**] | Determines the region of the results (history). | (optional) defaults to undefined|


### Return type

**PaginatedMetricList**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve**
> MetricDetail retrieve()

ViewSet for Metric model.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let id: string; //A UUID string identifying this Metric. (default to undefined)

const { status, data } = await apiInstance.retrieve(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | A UUID string identifying this Metric. | defaults to undefined|


### Return type

**MetricDetail**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **seasonalityRetrieve**
> MetricSeasonality seasonalityRetrieve()

Action that returns the seasonality of a specific metric.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let id: string; //A UUID string identifying this Metric. (default to undefined)

const { status, data } = await apiInstance.seasonalityRetrieve(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | A UUID string identifying this Metric. | defaults to undefined|


### Return type

**MetricSeasonality**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tilesRetrieve**
> Metric tilesRetrieve()

Action that returns the tiles of a specified area and zoom

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let date: string; //Date of the results to return. (default to undefined)
let x: string; // (default to undefined)
let y: string; // (default to undefined)
let z: string; // (default to undefined)

const { status, data } = await apiInstance.tilesRetrieve(
    date,
    x,
    y,
    z
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **date** | [**string**] | Date of the results to return. | defaults to undefined|
| **x** | [**string**] |  | defaults to undefined|
| **y** | [**string**] |  | defaults to undefined|
| **z** | [**string**] |  | defaults to undefined|


### Return type

**Metric**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.mapbox-vector-tile


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **timeseriesTilesRetrieve**
> Metric timeseriesTilesRetrieve()

ViewSet for Metric model.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let date: string; //Date of the results to return. (default to undefined)
let x: string; // (default to undefined)
let y: string; // (default to undefined)
let z: string; // (default to undefined)
let days: number; //Number of days to return in the time series. (optional) (default to undefined)

const { status, data } = await apiInstance.timeseriesTilesRetrieve(
    date,
    x,
    y,
    z,
    days
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **date** | [**string**] | Date of the results to return. | defaults to undefined|
| **x** | [**string**] |  | defaults to undefined|
| **y** | [**string**] |  | defaults to undefined|
| **z** | [**string**] |  | defaults to undefined|
| **days** | [**number**] | Number of days to return in the time series. | (optional) defaults to undefined|


### Return type

**Metric**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.mapbox-vector-tile


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trendRetrieve**
> MetricTrend trendRetrieve()

Action that returns the trend of a specific metric.

### Example

```typescript
import {
    MetricsApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let id: string; //A UUID string identifying this Metric. (default to undefined)

const { status, data } = await apiInstance.trendRetrieve(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | A UUID string identifying this Metric. | defaults to undefined|


### Return type

**MetricTrend**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

