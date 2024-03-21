# ResponseBody

The JSON response body for the log entry.


## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `code`                                                   | *string*                                                 | :heavy_minus_sign:                                       | The error code.                                          | bad_request                                              |
| `message`                                                | *string*                                                 | :heavy_minus_sign:                                       | The error message.                                       | Request failed validation                                |
| `status`                                                 | *number*                                                 | :heavy_minus_sign:                                       | The HTTP error code.                                     | 400                                                      |
| `type`                                                   | *string*                                                 | :heavy_minus_sign:                                       | Type of the log entry.                                   | error                                                    |
| `details`                                                | [components.Details](../../models/components/details.md) | :heavy_minus_sign:                                       | Details of the log entry, stack trace and endpoint.      |                                                          |