# Request > Order Deposit Query

```json
{
  "pid": 1382528827416576,
  "cid": 1382625403125760,
  "nonce": "pfvt1t",
  "timestamp": 1687851045181,
  "sign": "93aad14ccb8109cfafd68f024fe7248a"
}
```

### Response

#### Response Result

| Name | Type   | Description          |
| ---- | ------ | -------------------- |
| code | string | Response Code        |
| msg  | string | Response Message     |
| data | object | Response Data Object |

#### Response `data` Object

| Name             | Type           | Description           |
| ---------------- | -------------- | --------------------- |
| pid              | integer(int64) | Project ID            |
| address          | string         | Address               |
| chain\_id        | string         | Chain ID              |
| token\_id        | string         | Token ID              |
| currency         | string         | Currency Identifier   |
| amount           | string         | Amount                |
| real\_amount     | string         | Actual Amount         |
| status           | integer(int32) | Status                |
| third\_party\_id | string         | Caller Customized ID  |
| txid             | string         | Transaction hash      |
| block\_height    | string         | Transaction Height    |
| block\_time      | integer(int64) | Transaction Timestamp |

**`status` Enum Values**

| Value | Description           |
| ----- | --------------------- |
| 0     | Awaiting Confirmation |
| 1     | Successful            |
| 2     | Failed                |
| 3     | Timeout Cancellation  |
| 4     | Manual Cancellation   |

**Response Example**

```json
{
  "code": "00000",
  "msg": "ok",
  "data": {
    "pid": 1382528827416576,
    "address": "",
    "chain_id": "195",
    "token_id": "195",
    "currency": "TRX",
    "amount": "1.2",
    "real_amount": "0",
    "third_party_id": "c8fad34056714a539a5f33c3895ea133",
    "status": 1,
    "txid": "6dd05b0972075542219a3fcc116c58feaf9480f1f698cc46c4367ded83955cfd",
    "block_height": "34527604",
    "block_time": 1686814482000
  }
}
```
