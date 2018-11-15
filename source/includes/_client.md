# Client

A client is a company in which an user with the role CLIENT can operate. You can see this as the assignment giver for a shift

## Creating

> The returned JSON

```json
{
  "id": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
  "name": "Client 1"
}
```
> With a return code 201

Create a client

### Request
`POST /client/`

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
name | yes | String | - | The name of the client

## List

> The returned JSON

```json
[
  {
    "id": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
    "name": "Client 1"
  },
  {
    "id": "c66eec36-a328-4676-9847-9c3b756f7849",
    "name": "Client 2"
  }
]
```
> With a return code 200

List of clients

### Request
`GET /client/`

## Retrieve

Getting a single client

> The returned JSON

```json
{
  "id": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
  "name": "Client 1"
}
```
> With a return code 200

### Request
`GET /client/<id:string>/`

### Path parameter
Parameter | Description
--------- | -----------
id | The id of the client that you want to retrieve
