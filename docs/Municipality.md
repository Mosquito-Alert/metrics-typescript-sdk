# Municipality

Serializer for the Municipality model.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** |  | [readonly] [default to undefined]
**code** | **string** | The unique code that identifies the region. | [default to undefined]
**name** | **string** | The name of the region. | [default to undefined]
**alt_name** | **string** | Alternative names for the region. If there is more than one, they will be delimited by \&quot;|\&quot;. | [optional] [default to undefined]
**province** | **string** | Get the province name from the province related model. | [readonly] [default to undefined]

## Example

```typescript
import { Municipality } from 'metrics';

const instance: Municipality = {
    id,
    code,
    name,
    alt_name,
    province,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
