---
order: 20
---

# User Get Presence
Gets a user's presence if the query string `userId` is provided, otherwise it gets the callee's.

| URL | Requires Auth | HTTP Method | Query Parameters |
| :--- | :--- | :--- | :--- |
| `/api/v1/users.getPresence` | `yes` | `GET` | Optional: `userId=otherUserId` |

## Other Users Example Call
```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     http://localhost:3000/api/v1/users.getPresence?userId=BsNr28znDkG8aeo7W
```

## Example Result
```json
{
  "presence": "offline",
  "success": true
}
```

## Self Example Call
```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     http://localhost:3000/api/v1/users.getPresence
```

## Example Result
```json
{
  "presence": "offline",
  "connectionStatus": "offline",
  "lastLogin": "2016-12-08T18:26:03.612Z",
  "success": true
}
```
