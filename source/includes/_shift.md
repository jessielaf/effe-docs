# Shift

A shift is a assignment in which a specific time box can be set

## Create shift

```json
{
  "id": "e09929f8-91e8-45fb-95c0-fef48d92a0f0",
  "start": "2018-11-23T07:00:00.000000",
  "end": "2018-11-23T11:00:00.000000",
  "client": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
  "skills": [
    "7ac0419f-a139-4005-b22a-8acbebc0caf3",
    "b068eb9d-cd38-4e32-b756-fa4c6ace7243"
  ]
}
```
> With a return code 201

Create a shift

### Request
`POST /shift/`

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
start | yes | Date (YYYY-MM-DDTHH:mm) | - | Start of the shift
end | yes | Date (YYYY-MM-DDTHH:mm) | - | End of the shift
client | yes | String | - | The id of the client
skills | yes (empty allowed) | Array | - | Id's of the skills the employees of the shift need

## List shifts

> The returned JSON

```json
[
  {
    "id": "e09929f8-91e8-45fb-95c0-fef48d92a0f0",
    "start": "2018-11-23T07:00:00.000000",
    "end": "2018-11-23T11:00:00.000000",
    "client": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
    "skills": [
      "7ac0419f-a139-4005-b22a-8acbebc0caf3",
      "b068eb9d-cd38-4e32-b756-fa4c6ace7243"
    ]
  },
  {
    "id": "6ab8fc45-d358-40c6-9fe0-2cb0d60a6279",
    "start": "2018-11-25T08:00:00.000000",
    "end": "2018-11-23T12:00:00.000000",
    "client": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
    "skills": [
      "b59ab513-0ed7-4232-882a-8707874e92b2",
      "b068eb9d-cd38-4e32-b756-fa4c6ace7243"
    ]
  }
]
```
> With a return code 200

List of shifts

### Request
`GET /shift/`

## Retrieve shift

Getting a single shift

> The returned JSON

```json
{
  "id": "e09929f8-91e8-45fb-95c0-fef48d92a0f0",
  "start": "2018-11-23T07:00:00.000000",
  "end": "2018-11-23T11:00:00.000000",
  "client": "25c9e981-27eb-4fd6-88b8-a56fd1182b49",
  "skills": [
    "7ac0419f-a139-4005-b22a-8acbebc0caf3",
    "b068eb9d-cd38-4e32-b756-fa4c6ace7243"
  ]
}
```
> With a return code 200

### Request
`GET /shift/<id:string>/`

### Path parameter
Parameter | Description
--------- | -----------
id | The id of the shift that you want to retrieve
