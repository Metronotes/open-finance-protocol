---
sort: 5
---
# List Instruments

list instruments method used to synchronize information about tradeable instruments between counterparties. Clearinghouse or liquidity provider can call exchange with that method to get a list of all supported instruments before sending any limits or quotes.

Example of "**list_instruments**" request:

```
[1,42,"list_instruments",["spot", "active"]
```

In response method sends information about requested instruments. Each instrument described with three arguments.

|  №   | Name                | Data type |  Example  |
| :--: | ------------------- | :-------: | :-------: |
|  1   | type                |  string   |  "spot"   |
|  2   | instrument          |  string   | "BTC/USD" |
|  3   | base_unit           |  string   | "BTC" |
|  4   | quote_unit          |  string   | "USD" |
|  5   | min_price_increment |   float   |    0.1    |


Example of "**list_instruments**" response:

```
[2,42,"list_instruments",["spot", "BTC/USD", 0.1, "spot", "ETH/USD", 0.01]
```
