# SchemaApi

All URIs are relative to *http://localhost:8000/api/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**openapiJsonRetrieve**](#openapijsonretrieve) | **GET** /schema/openapi.json | |
|[**openapiYmlRetrieve**](#openapiymlretrieve) | **GET** /schema/openapi.yml | |

# **openapiJsonRetrieve**
> { [key: string]: any; } openapiJsonRetrieve()

OpenApi3 schema for this API. Format can be selected via content negotiation.  - YAML: application/vnd.oai.openapi - JSON: application/vnd.oai.openapi+json

### Example

```typescript
import {
    SchemaApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new SchemaApi(configuration);

let lang: SchemaOpenapiJsonRetrieveLangParameter; // (optional) (default to undefined)

const { status, data } = await apiInstance.openapiJsonRetrieve(
    lang
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **lang** | **SchemaOpenapiJsonRetrieveLangParameter** |  | (optional) defaults to undefined|


### Return type

**{ [key: string]: any; }**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.oai.openapi+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **openapiYmlRetrieve**
> { [key: string]: any; } openapiYmlRetrieve()

OpenApi3 schema for this API. Format can be selected via content negotiation.  - YAML: application/vnd.oai.openapi - JSON: application/vnd.oai.openapi+json

### Example

```typescript
import {
    SchemaApi,
    Configuration
} from 'anomaly-detection';

const configuration = new Configuration();
const apiInstance = new SchemaApi(configuration);

let format: SchemaOpenapiYmlRetrieveFormatParameter; // (optional) (default to undefined)
let lang: SchemaOpenapiJsonRetrieveLangParameter; // (optional) (default to undefined)

const { status, data } = await apiInstance.openapiYmlRetrieve(
    format,
    lang
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **format** | **SchemaOpenapiYmlRetrieveFormatParameter** |  | (optional) defaults to undefined|
| **lang** | **SchemaOpenapiJsonRetrieveLangParameter** |  | (optional) defaults to undefined|


### Return type

**{ [key: string]: any; }**

### Authorization

[tokenAuth](../README.md#tokenAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/vnd.oai.openapi, application/yaml, application/vnd.oai.openapi+json, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

