# GetBuyerBillingDetailsResponse


## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `httpMeta`                                                             | [components.HTTPMetadata](../../models/components/httpmetadata.md)     | :heavy_check_mark:                                                     | N/A                                                                    |
| `billingDetails`                                                       | [components.BillingDetails](../../models/components/billingdetails.md) | :heavy_minus_sign:                                                     | Returns the information about a buyer's billing details.               |
| `errorGeneric`                                                         | [components.ErrorGeneric](../../models/components/errorgeneric.md)     | :heavy_minus_sign:                                                     | Returns a generic error.                                               |