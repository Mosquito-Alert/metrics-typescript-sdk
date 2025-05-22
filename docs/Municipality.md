# Municipality

Serializer for the Municipality model.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | The unique code that identifies the region. | [default to undefined]
**name** | **string** | The name of the region. | [default to undefined]
**alt_name** | **string** | Alternative names for the region. If there is more than one, they will be delimited by \&quot;|\&quot;. | [optional] [default to undefined]

## Example

```typescript
import { Municipality } from 'anomaly-detection';

const instance: Municipality = {
    code,
    name,
    alt_name,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
