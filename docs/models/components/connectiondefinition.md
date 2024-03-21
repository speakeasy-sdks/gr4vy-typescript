# ConnectionDefinition

A connection that can be configured.


## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                | Example                                                    |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `id`                                                       | *string*                                                   | :heavy_minus_sign:                                         | The ID of the connection.                                  | stripe-card                                                |
| `type`                                                     | *string*                                                   | :heavy_minus_sign:                                         | `connection-definition`.                                   | connection-definition                                      |
| `name`                                                     | *string*                                                   | :heavy_minus_sign:                                         | The name of this connection.                               | Stripe                                                     |
| `count`                                                    | *number*                                                   | :heavy_minus_sign:                                         | The number of configured connections.                      | 1                                                          |
| `group`                                                    | [components.Group](../../models/components/group.md)       | :heavy_minus_sign:                                         | N/A                                                        | payment-service                                            |
| `category`                                                 | [components.Category](../../models/components/category.md) | :heavy_minus_sign:                                         | N/A                                                        | card                                                       |
| `iconUrl`                                                  | *string*                                                   | :heavy_minus_sign:                                         | An icon to display for the connection.                     | https://cdn.gr4vy.app/stripe.svg                           |
| `provider`                                                 | *string*                                                   | :heavy_minus_sign:                                         | The provider for this connection.                          | Stripe                                                     |