# Availability

A availability is a company in which an user with the role CLIENT can operate. You can see this as the assignment giver for a shift

## Create availability

> The returned JSON

```json
{
  "availability": [
    {
      "start": "2018-11-23T07:00:00.000000",
      "end": "2018-11-23T015:00:00.000000"
    }
    {
      "start": "2018-11-23T07:00:00.000000",
      "end": "2018-11-23T015:00:00.000000"
    }
  ]
}
```
> With a return code 200

Create availability for a user

### Request
`PUT /availability/<string:user_id>/`

### Path parameter
Parameter | Description
--------- | -----------
user_id | The user from whom you want to create the availability

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
[availability](#availability-parameter) | yes | Array | - | Array of the availability for a user

### Availability parameter
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
start | yes | Date (YYYY-MM-DDTHH:mm) | - | Start of the availability
end | yes | Date (YYYY-MM-DDTHH:mm) | - | End of the availability

## List availabilities

> The returned JSON

```json
{
  "availability": [
    {
      "start": "2018-11-23T07:00:00.000000",
      "end": "2018-11-23T015:00:00.000000"
    }
    {
      "start": "2018-11-23T07:00:00.000000",
      "end": "2018-11-23T015:00:00.000000"
    }
  ]
}
```
> With a return code 200

List of availability for a user

### Request
`GET /availability/<string:user_id>/`

### Path parameter
Parameter | Required | Description
--------- | -------  | -----------
year | yes | The year in which the availability should be
month | yes | The month in which the availability should be
