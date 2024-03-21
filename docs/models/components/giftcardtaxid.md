# GiftCardTaxID

The tax information associated with the billing details.


## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        | Example                                                            |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `value`                                                            | *string*                                                           | :heavy_check_mark:                                                 | The tax ID for the buyer.                                          | 12345678931                                                        |
| `kind`                                                             | [components.GiftCardKind](../../models/components/giftcardkind.md) | :heavy_check_mark:                                                 | The kind of tax ID.                                                | gb.vat                                                             |