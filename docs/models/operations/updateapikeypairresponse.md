# UpdateApiKeyPairResponse


## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `httpMeta`                                                         | [components.HTTPMetadata](../../models/components/httpmetadata.md) | :heavy_check_mark:                                                 | N/A                                                                |
| `apiKeyPair`                                                       | [components.APIKeyPair](../../models/components/apikeypair.md)     | :heavy_minus_sign:                                                 | Returns the updated key pair.                                      |
| `errorGeneric`                                                     | [components.ErrorGeneric](../../models/components/errorgeneric.md) | :heavy_minus_sign:                                                 | Returns a generic error.                                           |