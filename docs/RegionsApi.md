# RegionsApi

All URIs are relative to *https://metrics.mosquitoalert.com/api/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**autonomousCommunitiesTilesRetrieve**](#autonomouscommunitiestilesretrieve) | **GET** /regions/autonomous_communities/tiles/{z}/{x}/{y}/ | |
|[**list**](#list) | **GET** /regions/ | |
|[**municipalitiesTilesRetrieve**](#municipalitiestilesretrieve) | **GET** /regions/municipalities/tiles/{z}/{x}/{y}/ | |
|[**provincesTilesRetrieve**](#provincestilesretrieve) | **GET** /regions/provinces/tiles/{z}/{x}/{y}/ | |
|[**retrieve**](#retrieve) | **GET** /regions/{id}/ | |
|[**tilesRetrieve**](#tilesretrieve) | **GET** /regions/tiles/{z}/{x}/{y}/ | |

# **autonomousCommunitiesTilesRetrieve**
> Municipality autonomousCommunitiesTilesRetrieve()

Action that returns the tiles of a specified autonomous community and zoom

### Example

```typescript
import {
    RegionsApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new RegionsApi(configuration);

let x: string; // (default to undefined)
let y: string; // (default to undefined)
let z: string; // (default to undefined)

const { status, data } = await apiInstance.autonomousCommunitiesTilesRetrieve(
    x,
    y,
    z
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **x** | [**string**] |  | defaults to undefined|
| **y** | [**string**] |  | defaults to undefined|
| **z** | [**string**] |  | defaults to undefined|


### Return type

**Municipality**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.mapbox-vector-tile


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list**
> PaginatedMunicipalityList list()

ViewSet for the Municipality model with MVT rendering.

### Example

```typescript
import {
    RegionsApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new RegionsApi(configuration);

let ordering: RegionsListOrderingParameter; //Order by `code`, `name` or `province`. (optional) (default to undefined)
let page: number; //A page number within the paginated result set. (optional) (default to undefined)
let pageSize: number; //Number of results to return per page. (optional) (default to undefined)
let regionName: string; //Region name. (optional) (default to 'Lloret de Mar')

const { status, data } = await apiInstance.list(
    ordering,
    page,
    pageSize,
    regionName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ordering** | **RegionsListOrderingParameter** | Order by &#x60;code&#x60;, &#x60;name&#x60; or &#x60;province&#x60;. | (optional) defaults to undefined|
| **page** | [**number**] | A page number within the paginated result set. | (optional) defaults to undefined|
| **pageSize** | [**number**] | Number of results to return per page. | (optional) defaults to undefined|
| **regionName** | [**string**] | Region name. | (optional) defaults to 'Lloret de Mar'|


### Return type

**PaginatedMunicipalityList**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **municipalitiesTilesRetrieve**
> Municipality municipalitiesTilesRetrieve()

Action that returns the tiles of a specified municipality and zoom

### Example

```typescript
import {
    RegionsApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new RegionsApi(configuration);

let x: string; // (default to undefined)
let y: string; // (default to undefined)
let z: string; // (default to undefined)

const { status, data } = await apiInstance.municipalitiesTilesRetrieve(
    x,
    y,
    z
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **x** | [**string**] |  | defaults to undefined|
| **y** | [**string**] |  | defaults to undefined|
| **z** | [**string**] |  | defaults to undefined|


### Return type

**Municipality**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.mapbox-vector-tile


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **provincesTilesRetrieve**
> Municipality provincesTilesRetrieve()

Action that returns the tiles of a specified province and zoom

### Example

```typescript
import {
    RegionsApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new RegionsApi(configuration);

let x: string; // (default to undefined)
let y: string; // (default to undefined)
let z: string; // (default to undefined)

const { status, data } = await apiInstance.provincesTilesRetrieve(
    x,
    y,
    z
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **x** | [**string**] |  | defaults to undefined|
| **y** | [**string**] |  | defaults to undefined|
| **z** | [**string**] |  | defaults to undefined|


### Return type

**Municipality**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.mapbox-vector-tile


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retrieve**
> MunicipalityRetrieve retrieve()

ViewSet for the Municipality model with MVT rendering.

### Example

```typescript
import {
    RegionsApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new RegionsApi(configuration);

let id: number; //A unique integer value identifying this Municipality. (default to undefined)

const { status, data } = await apiInstance.retrieve(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**number**] | A unique integer value identifying this Municipality. | defaults to undefined|


### Return type

**MunicipalityRetrieve**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **tilesRetrieve**
> Municipality tilesRetrieve()

Action that returns the tiles of a specified region and zoom. This endpoint is dynamic, so it will return the tiles for a municipality, province, or autonomous community based on the zoom level.

### Example

```typescript
import {
    RegionsApi,
    Configuration
} from 'metrics';

const configuration = new Configuration();
const apiInstance = new RegionsApi(configuration);

let x: string; // (default to undefined)
let y: string; // (default to undefined)
let z: string; // (default to undefined)

const { status, data } = await apiInstance.tilesRetrieve(
    x,
    y,
    z
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **x** | [**string**] |  | defaults to undefined|
| **y** | [**string**] |  | defaults to undefined|
| **z** | [**string**] |  | defaults to undefined|


### Return type

**Municipality**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.mapbox-vector-tile


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

