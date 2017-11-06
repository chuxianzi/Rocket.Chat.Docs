---
order: 65
---

# Channel Renamef
修改频道名称

| URL | Requires Auth | HTTP Method |
| :--- | :--- | :--- |
| `/api/v1/channels.renamef` | `yes` | `POST` |

## Payload
| Argument | Example | Required | Description |
| :--- | :--- | :--- | :--- |
| `roomId` | `ByehQjC44FwMeiLbX` | Required | The channel's id |
| `fname` | `频道名称` | 必须的 | The new name the channel will have, it can not be the same as another or the existing name |

## Example Call
```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     -H "Content-type: application/json" \
     http://localhost:3000/api/v1/channels.renamef \
     -d '{ "roomId": "ByehQjC44FwMeiLbX", "fname": "new-fname" }'
```

## Example Result
```json
{
  "channel": {
    "_id": "ByehQjC44FwMeiLbX",
    "fname": "new-fname",
    "t": "c",
    "usernames": [
      "testing1"
    ],
    "msgs": 4,
    "u": {
      "_id": "aobEdbYhXfu5hkeqG",
      "username": "testing1"
    },
    "ts": "2016-12-09T15:08:58.042Z",
    "ro": false,
    "sysMes": true,
    "_updatedAt": "2016-12-09T15:57:44.686Z"
  },
  "success": true
}
```

## Change Log
| Version | Description |
| :--- | :--- |
| 0.48.0 | Added |
