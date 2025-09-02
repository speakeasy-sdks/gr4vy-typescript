# Balances
(*giftCards.balances*)

## Overview

### Available Operations

* [list](#list) - List gift card balances

## list

Fetch the balances for one or more gift cards.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="list_gift_card_balances" method="post" path="/gift-cards/balances" -->
```typescript
import { Gr4vy, withToken } from "@gr4vy/sdk";
import fs from "fs";

const gr4vy = new Gr4vy({
    id: "example",
    server: "sandbox",
    merchantAccountId: "default",
    bearerAuth: withToken({
      privateKey: fs.readFileSync("private_key.pem", "utf8"),
    }),
});

async function run() {
  const result = await gr4vy.giftCards.balances.list({
    items: [
      {
        id: "356d56e5-fe16-42ae-97ee-8d55d846ae2e",
      },
      {
        id: "356d56e5-fe16-42ae-97ee-8d55d846ae2e",
      },
      {
        number: "4123455541234561234",
        pin: "1234",
      },
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { Gr4vyCore } from "@gr4vy/sdk/core.js";
import { giftCardsBalancesList } from "@gr4vy/sdk/funcs/giftCardsBalancesList.js";

// Use `Gr4vyCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const gr4vy = new Gr4vyCore({
  merchantAccountId: "<id>",
  bearerAuth: process.env["GR4VY_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await giftCardsBalancesList(gr4vy, {
    items: [
      {
        id: "356d56e5-fe16-42ae-97ee-8d55d846ae2e",
      },
      {
        id: "356d56e5-fe16-42ae-97ee-8d55d846ae2e",
      },
      {
        number: "4123455541234561234",
        pin: "1234",
      },
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("giftCardsBalancesList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `giftCardBalanceRequest`                                                                                                                                                       | [components.GiftCardBalanceRequest](../../models/components/giftcardbalancerequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `merchantAccountId`                                                                                                                                                            | *string*                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                             | The ID of the merchant account to use for this request.                                                                                                                        |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.GiftCardSummaries](../../models/components/giftcardsummaries.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.Error400            | 400                        | application/json           |
| errors.Error401            | 401                        | application/json           |
| errors.Error403            | 403                        | application/json           |
| errors.Error404            | 404                        | application/json           |
| errors.Error405            | 405                        | application/json           |
| errors.Error409            | 409                        | application/json           |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.Error425            | 425                        | application/json           |
| errors.Error429            | 429                        | application/json           |
| errors.Error500            | 500                        | application/json           |
| errors.Error502            | 502                        | application/json           |
| errors.Error504            | 504                        | application/json           |
| errors.SDKError            | 4XX, 5XX                   | \*/\*                      |