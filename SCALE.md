# Scaling


## Amounts

Asset quantities and totals transmitted via the Coinfloor API are encoded as integers with an implicit scale factor that depends on the particular asset type.

| Asset Type | Asset Code | Scale Factor | Atomic Unit |
|:----------:|-----------:|-------------:|------------:|
|     XBT    |     0xF800 |        10000 |     Ƀ0.0001 |
|     GBP    |     0xFA20 |          100 |       £0.01 |

### Examples

| Logical Amount | Integer Encoding |
|---------------:|-----------------:|
|       Ƀ12.3456 |           123456 |
|       £9876.54 |           987654 |
|           Ƀ1.5 |            15000 |
|            £20 |             2000 |


## Prices

Prices transmitted via the Coinfloor API are encoded as integers with an implicit scale factor that depends on the particular asset pair.

| Asset Pair | Scale Factor |
|:----------:|-------------:|
|   XBT:GBP  |          100 |

### Examples

| Logical Price | Integer Encoding |
|--------------:|-----------------:|
|   £543.21/XBT |            54321 |
|     £1000/XBT |           100000 |
