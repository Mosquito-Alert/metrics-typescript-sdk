# Metric

Serializer for the Metrics.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [readonly] [default to undefined]
**date** | **string** | The date of the metric. | [default to undefined]
**value** | **number** | The actual value of the metric. | [optional] [default to undefined]
**predicted_value** | **number** | The predicted value of the metric. This value will be estimated at creation. | [optional] [default to undefined]
**lower_value** | **number** | The predicted lower band value of the metric, from which values will be             considerated as anomalies. This value will be estimated at creation. | [optional] [default to undefined]
**upper_value** | **number** | The predicted upper band value of the metric, from which values will be             considerated as anomalies. This value will be estimated at creation. | [optional] [default to undefined]
**anomaly_degree** | **number** | The degree of the anomaly, a range of values that starts on -1 (a lower anomaly of the             highest degree) and ends on +1 (a upper anomaly of the highest degree). The 0 value means that             these is no anomaly. This value will be estimated at creation. | [readonly] [default to undefined]
**region_code** | **string** |  | [readonly] [default to undefined]

## Example

```typescript
import { Metric } from 'metrics';

const instance: Metric = {
    id,
    date,
    value,
    predicted_value,
    lower_value,
    upper_value,
    anomaly_degree,
    region_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
