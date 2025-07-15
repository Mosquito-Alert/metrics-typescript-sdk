# MunicipalityRetrieveProperties


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | The unique code that identifies the region. | [optional] [default to undefined]
**name** | **string** | The name of the region. | [optional] [default to undefined]
**alt_name** | **string** | Alternative names for the region. If there is more than one, they will be delimited by \&quot;|\&quot;. | [optional] [default to undefined]
**province** | **string** | Get the province name from the province related model. | [optional] [readonly] [default to undefined]

## Example

```typescript
import { MunicipalityRetrieveProperties } from 'metrics';

const instance: MunicipalityRetrieveProperties = {
    code,
    name,
    alt_name,
    province,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
