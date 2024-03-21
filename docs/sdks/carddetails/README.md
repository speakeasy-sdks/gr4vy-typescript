# CardDetails
(*cardDetails*)

## Overview

Endpoints to retrieve details of a card by utilising a BIN lookup table.

### Available Operations

* [getCardDetails](#getcarddetails) - Get card details

## getCardDetails

Retrieves details about a card using either that
card's BIN or for stored cards the `payment_method_id`.

### Example Usage

```typescript
import { Gr4vy } from "@gr4vy/node";
import { Intent, PaymentSource } from "@gr4vy/node/models/operations";

async function run() {
  const sdk = new Gr4vy({
    bearerAuth: "<YOUR_BEARER_TOKEN_HERE>",
  });

  const result = await sdk.cardDetails.getCardDetails({
    currency: "USD",
    amount: 500,
    bin: "42424242",
    country: "US",
    intent: Intent.Capture,
    isSubsequentPayment: true,
    merchantInitiated: true,
    metadata: "{\"restricted_items\": \"True\"}",
    paymentMethodId: "46973e9d-88a7-44a6-abfe-be4ff0134ff4",
    paymentSource: PaymentSource.Recurring,
  });

  // Handle the result
  console.log(result)
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetCardDetailsRequest](../../models/operations/getcarddetailsrequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |


### Response

**Promise<[operations.GetCardDetailsResponse](../../models/operations/getcarddetailsresponse.md)>**
### Errors

| Error Object                | Status Code                 | Content Type                |
| --------------------------- | --------------------------- | --------------------------- |
| errors.Error400BadRequest   | 400                         | application/json            |
| errors.Error401Unauthorized | 401                         | application/json            |
| errors.SDKError             | 4xx-5xx                     | */*                         |
