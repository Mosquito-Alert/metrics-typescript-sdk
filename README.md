## anomaly-detection@0.1.17-BETA

This generator creates TypeScript/JavaScript client that utilizes [axios](https://github.com/axios/axios). The generated Node module can be used in the following environments:

Environment
* Node.js
* Webpack
* Browserify

Language level
* ES5 - you must have a Promises/A+ library installed
* ES6

Module system
* CommonJS
* ES6 module system

It can be used in both TypeScript and JavaScript. In TypeScript, the definition will be automatically resolved via `package.json`. ([Reference](https://www.typescriptlang.org/docs/handbook/declaration-files/consumption.html))

### Building

To build and compile the typescript sources to javascript use:
```
npm install
npm run build
```

### Publishing

First build the package then run `npm publish`

### Consuming

navigate to the folder of your consuming project and run one of the following commands.

_published:_

```
npm install anomaly-detection@0.1.17-BETA --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost:8000/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*MetricsApi* | [**batchCreate**](docs/MetricsApi.md#batchcreate) | **POST** /metrics/batch/ | 
*MetricsApi* | [**lastDateRetrieve**](docs/MetricsApi.md#lastdateretrieve) | **GET** /metrics/dates/last/ | 
*MetricsApi* | [**list**](docs/MetricsApi.md#list) | **GET** /metrics/ | 
*MetricsApi* | [**retrieve**](docs/MetricsApi.md#retrieve) | **GET** /metrics/{id}/ | 
*MetricsApi* | [**seasonalityRetrieve**](docs/MetricsApi.md#seasonalityretrieve) | **GET** /metrics/{id}/seasonality/ | 
*MetricsApi* | [**tilesRetrieve**](docs/MetricsApi.md#tilesretrieve) | **GET** /metrics/tiles/{z}/{x}/{y}/ | 
*MetricsApi* | [**trendRetrieve**](docs/MetricsApi.md#trendretrieve) | **GET** /metrics/{id}/trend/ | 
*RegionsApi* | [**autonomousCommunitiesTilesRetrieve**](docs/RegionsApi.md#autonomouscommunitiestilesretrieve) | **GET** /regions/autonomous_communities/tiles/{z}/{x}/{y}/ | 
*RegionsApi* | [**list**](docs/RegionsApi.md#list) | **GET** /regions/ | 
*RegionsApi* | [**municipalitiesTilesRetrieve**](docs/RegionsApi.md#municipalitiestilesretrieve) | **GET** /regions/municipalities/tiles/{z}/{x}/{y}/ | 
*RegionsApi* | [**provincesTilesRetrieve**](docs/RegionsApi.md#provincestilesretrieve) | **GET** /regions/provinces/tiles/{z}/{x}/{y}/ | 
*RegionsApi* | [**retrieve**](docs/RegionsApi.md#retrieve) | **GET** /regions/{id}/ | 
*RegionsApi* | [**tilesRetrieve**](docs/RegionsApi.md#tilesretrieve) | **GET** /regions/tiles/{z}/{x}/{y}/ | 
*SchemaApi* | [**openapiJsonRetrieve**](docs/SchemaApi.md#openapijsonretrieve) | **GET** /schema/openapi.json | 
*SchemaApi* | [**openapiYmlRetrieve**](docs/SchemaApi.md#openapiymlretrieve) | **GET** /schema/openapi.yml | 


### Documentation For Models

 - [LastMetricDate](docs/LastMetricDate.md)
 - [Metric](docs/Metric.md)
 - [MetricDetail](docs/MetricDetail.md)
 - [MetricFileRequest](docs/MetricFileRequest.md)
 - [MetricSeasonality](docs/MetricSeasonality.md)
 - [MetricTrend](docs/MetricTrend.md)
 - [MetricsListOrderingParameter](docs/MetricsListOrderingParameter.md)
 - [Municipality](docs/Municipality.md)
 - [MunicipalityRetrieve](docs/MunicipalityRetrieve.md)
 - [MunicipalityRetrieveGeometry](docs/MunicipalityRetrieveGeometry.md)
 - [MunicipalityRetrieveGeometryType](docs/MunicipalityRetrieveGeometryType.md)
 - [MunicipalityRetrieveProperties](docs/MunicipalityRetrieveProperties.md)
 - [MunicipalityRetrieveType](docs/MunicipalityRetrieveType.md)
 - [PaginatedMetricList](docs/PaginatedMetricList.md)
 - [PaginatedMunicipalityList](docs/PaginatedMunicipalityList.md)
 - [RegionsListOrderingParameter](docs/RegionsListOrderingParameter.md)
 - [SchemaOpenapiJsonRetrieveLangParameter](docs/SchemaOpenapiJsonRetrieveLangParameter.md)
 - [SchemaOpenapiYmlRetrieveFormatParameter](docs/SchemaOpenapiYmlRetrieveFormatParameter.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization


Authentication schemes defined for the API:
<a id="tokenAuth"></a>
### tokenAuth

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

