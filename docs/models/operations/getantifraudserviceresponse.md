# GetAntiFraudServiceResponse


## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `httpMeta`                                                                 | [components.HTTPMetadata](../../models/components/httpmetadata.md)         | :heavy_check_mark:                                                         | N/A                                                                        |
| `antiFraudService`                                                         | [components.AntiFraudService](../../models/components/antifraudservice.md) | :heavy_minus_sign:                                                         | Returns the information about a anti-fraud service.                        |
| `errorGeneric`                                                             | [components.ErrorGeneric](../../models/components/errorgeneric.md)         | :heavy_minus_sign:                                                         | Returns a generic error.                                                   |