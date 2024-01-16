# Request > Order Deposit Creation

### API URL

POST /api/v1/deposit

### Request

#### Request Parameters

| Name             | Type           | Required | Description                                                                                                                                                    |
| ---------------- | -------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| pid              | integer(int64) | Yes      | Project ID                                                                                                                                                     |
| currency         | string         | Yes      | Currency Identifier                                                                                                                                            |
| amount           | string         | Yes      | Amount                                                                                                                                                         |
| callback\_url    | string         | Yes      | Callback URL, If funds are received through an address generated by this API, refer to [Broken link](broken-reference "mention") section for callback details. |
| third\_party\_id | string         | Yes      | Caller Customized ID                                                                                                                                           |
| timeout          | integer(int32) | No       | Timeout (in minutes), default is 10 mins                                                                                                                       |
| remark           | string         | No       | Remark                                                                                                                                                         |
| nonce            | string         | Yes      | 6-digit random string                                                                                                                                          |
| timestamp        | integer(int64) | Yes      | Timestamp                                                                                                                                                      |
| sign             | string         | Yes      | Signature                                                                                                                                                      |

**Request Example**

```json
{
  "pid": 1382528827416576,
  "callback_url": "http://xxxx.com/deposit/callback",
  "amount": "1.2",
  "currency": "TRON@Shasta",
  "remark": "423423",
  "third_party_id": "0828ebaa64f44b04a4da836b2c2d1da1",
  "timeout": 10,
  "nonce": "ubqso3",
  "timestamp": 1687850657960,
  "sign": "f5be13fdd8c6f63951ca4427359457cb"
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

| Name    | Type           | Description         |
| ------- | -------------- | ------------------- |
| address | string         | Address             |
| cid     | integer(int64) | Order Serial Number |

**Response Example**

```json
{
  "code": "00000",
  "msg": "ok",
  "data": {
    "cid": 1382686995161088,
    "address": "TBotPUNNgeSJmqWkSE7JoHdAnsdMyVnUca"
  }
}
```