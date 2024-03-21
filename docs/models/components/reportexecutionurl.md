# ReportExecutionUrl

The temporary signed URL to download the result of a report execution
and its expiration date and time.


## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   | Example                                                                                       |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `url`                                                                                         | *string*                                                                                      | :heavy_minus_sign:                                                                            | The URL to download the report execution.                                                     | https://example.com/download                                                                  |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | The date and time when the download URL expires.                                              | 2013-07-16T19:23:00.000+00:00                                                                 |