# FlowRuleOutcomes

Defines the outcome of a rule in a flow.
Currently the outcomes can be a boolean value, or a list of string
values. The meaning of this outcome depends on the `action` this rule
is triggered for.


## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `items`                              | *components.FlowRuleOutcomesItems*[] | :heavy_minus_sign:                   | A list of outcomes.                  |