# RefundStatus

The status of the refund.
It may change over time as asynchronous processing events occur.

- `processing` - The refund is being processed.
- `succeeded` - The refund was successful.
- `declined` - The refund was declined by the underlying PSP.
- `failed` - The refund could not proceed due to a technical issue.
- `voided` - The refund was voided and will not proceed.


## Values

| Name         | Value        |
| ------------ | ------------ |
| `Processing` | processing   |
| `Succeeded`  | succeeded    |
| `Declined`   | declined     |
| `Failed`     | failed       |
| `Voided`     | voided       |