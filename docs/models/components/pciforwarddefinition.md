# PCIForwardDefinition

An available Vault Forward definition that can be configured.


## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             | Example                                                                 |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `id`                                                                    | *string*                                                                | :heavy_minus_sign:                                                      | The ID of the Vault Forward definition.                                 | amadeus                                                                 |
| `type`                                                                  | *string*                                                                | :heavy_minus_sign:                                                      | The type of this resource. It is always `vault-forward-definition`.     | vault-forward-definition                                                |
| `displayName`                                                           | *string*                                                                | :heavy_minus_sign:                                                      | The display name of this definition.                                    | Amadeus                                                                 |
| `hosts`                                                                 | *string*[]                                                              | :heavy_minus_sign:                                                      | The hosts where Vault Forward requests are allowed for this definition. | [<br/>"https://api.amadeus.com",<br/>"https://test.api.amadeus.com"<br/>] |