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
  ],
  "store": "b068eb9d-cd38-4e32-b756-fa4c6ace7243",
  "is_repeat": true,
  "users": [
    {
      "id":"882549fe-1503-4717-8f3a-26757a55ee36",
      "first_name":"test14",
      "last_name":"test14"
    },
    {
      "id":"b04d0f31-e642-4fb3-b2cc-15a4ab1f536a",
      "first_name":"test73",
      "last_name":"test73"
    }
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
store | yes | String | - | The id of the store
is_repeat | no | Boolean | False | If the shift needs to repeat every week
skills | no | Array | - | Id's of the skills the employees of the shift need
users | no | Array | - | Id's of the users of the shift need

## List shifts

> The returned JSON

```json
[
  {
    "id":"0afba225-f22d-4722-b044-c763d69e26a6",
    "title":"Test shift 29",
    "start":"2018-11-05T11:36:43.069257",
    "end":"2018-11-05T15:36:43.069257",
    "amount_of_minutes":240,
    "client":"eb54efa9-31b9-4ea6-a33b-26309dd2ca14",
    "skills":[
      {
        "id":"770e851f-352d-4951-b9b6-78bdc01fb1b9",
        "name":"> 2 jaar ervaring"
      },
      {
        "id":"f16d1875-5a43-44fc-9b8d-33f3a5e1ad6f",
        "name":"Public speaking"
      }
    ],
    "users": {
      "first_name": "Jessie",
      "lastname_name": "Liauw A Fong",
    }
  },
  {
    "id":"0e54421b-fece-41f9-9a18-57a85cd1b2a6",
    "title":"Test shift 21",
    "start":"2018-11-07T12:36:42.979309",
    "end":"2018-11-07T16:36:42.979309",
    "amount_of_minutes":240,
    "client":"eb54efa9-31b9-4ea6-a33b-26309dd2ca14",
    "skills":[
      {
        "id":"770e851f-352d-4951-b9b6-78bdc01fb1b9",
        "name":"> 2 jaar ervaring"
      },
      {
        "id":"f393f7ee-3520-49f3-9c2a-abbda1d09607",
        "name":"Bier tappen"
      }
    ]
  }
]
```
> With a return code 200

List of shifts

### Request
`GET /shift/?client-id=`

### Query parameter
Parameter | Required | Description
--------- | -------  | -----------
client-id | no | Gets the shifts but only of the given client

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
  ],
  "store": "b068eb9d-cd38-4e32-b756-fa4c6ace7243",
  "is_repeat": true,
  "users": [
    {
      "id":"882549fe-1503-4717-8f3a-26757a55ee36",
      "first_name":"test14",
      "last_name":"test14"
    },
    {
      "id":"b04d0f31-e642-4fb3-b2cc-15a4ab1f536a",
      "first_name":"test73",
      "last_name":"test73"
    }
  ]
}
```
> With a return code 201

Update a shift

### Request
`PATCH /shift/<>`

### Path parameter
Parameter | Description
--------- | -----------
id | The id of the shift that you want to update

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
start | yes | Date (YYYY-MM-DDTHH:mm) | - | Start of the shift
end | yes | Date (YYYY-MM-DDTHH:mm) | - | End of the shift
client | yes | String | - | The id of the client
store | yes | String | - | The id of the store
is_repeat | no | Boolean | False | If the shift needs to repeat every week
skills | no | Array | - | Id's of the skills the employees of the shift need
users | no | Array | - | Id's of the users of the shift need

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


## List of shifts for user

> The returned JSON

```json
{
  "shifts":[
    {
      "id":"7ebb4fa8-bb6f-4221-8475-7dda009e8d14",
      "title":"test",
      "start":"2018-11-29T15:00:00",
      "end":"2018-11-29T16:00:00",
      "client":"6958da3e-b35c-49ef-a39f-1fb2e7747a80"
    },
    {
      "id":"ac8ce338-5688-4d7e-b939-cc57bd322318",
      "title":"test",
      "start":"2019-11-28T15:15:00",
      "end":"2019-11-28T16:00:00",
      "client":"6958da3e-b35c-49ef-a39f-1fb2e7747a80"
    }
  ]
}
```
> With a return code 200

### Request
`GET /user/<int:user-id>/shifts/`

### Path parameter
Parameter | Required | Description
--------- | -------  | -----------
user-id | no | Get shifts based on employee
