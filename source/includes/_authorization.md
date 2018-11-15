# Authorization

Before you can do any other call you need to be authorized. We use jwt to authenticate to the backend.

## Authorize per request

```shell
curl "http://example.com/<string:url>"
  -H "Authorization: <string:token>"
```

For each request you need to send the jwt token along. You can do this by sending a header with your request.

`Authorization: Bearer <string:token>`

## Get jwt token for user

> The returned JSON

```json
{
  "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c"
}
```
> With a return code 200

Before you send any other request the token is required. This is how you get such a token

### Request
`POST /authenticate/`

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
username | true | String | - | The username of the user you want to login as
password | true | String | - | The password of the user you want to login as
