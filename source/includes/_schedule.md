# Schedule

## Schedule all shifts

The schedule app allows you to schedule all your employees with shifts based on availability

> Returns a return code 200

### Request
`GET /schedule/<int:year>-<int:month>/`

### Path parameter
Parameter | Description
--------- | -----------
year | The year in which the shifts you want to plan are
month | The month in which the shifts you want to plan are

<aside class="info">
We are planning on creating a from and to api endpoint
</aside>

## Get potential employees for shift

Get the potential employees for a shift based on the year and month


> Returns a return code 200

### Request
`POST /schedule/employees/`

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
start | yes | Date (YYYY-MM-DDTHH:mm) | - | Start of the shift
end | yes | Date (YYYY-MM-DDTHH:mm) | - | End of the shift
skills | no | Array | - | Array of ids of the skills
shift_id | no | UUID | - | If you want to edit a skill and want the potential employees add this. This is because of repeated shifts
