# NewCheckoutSessionResponse


## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `httpMeta`                                                               | [components.HTTPMetadata](../../models/components/httpmetadata.md)       | :heavy_check_mark:                                                       | N/A                                                                      |
| `checkoutSession`                                                        | [components.CheckoutSession](../../models/components/checkoutsession.md) | :heavy_minus_sign:                                                       | Returns the new Checkout Session.                                        |
| `errorGeneric`                                                           | [components.ErrorGeneric](../../models/components/errorgeneric.md)       | :heavy_minus_sign:                                                       | Returns a generic error.                                                 |