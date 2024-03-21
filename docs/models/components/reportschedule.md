# ReportSchedule

Specifies the schedule of this report.

If this is a one-off report, this value is `once`.

If this is a recurring report, this value is set to the
frequency by which the report will be executed. For example, a
`monthly` schedule means that this report will be periodically
executed at the start of each month.

Note that a `weekly` schedule means that the report is executed
at the start of every Monday.


## Values

| Name      | Value     |
| --------- | --------- |
| `Daily`   | daily     |
| `Monthly` | monthly   |
| `Once`    | once      |
| `Weekly`  | weekly    |