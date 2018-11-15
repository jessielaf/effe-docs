# User

## Creating

> The returned JSON

```json
{
  "id": "00329c9d-cea0-4c32-ae69-6002222d32ec",
  "username": "test6",
  "first_name": "test6",
  "last_name": "test6",
  "role": "TEMP_WORKER",
  "date_of_birth": "2018-01-01",
  "profile_image": null | "<string:Base64>",
  "location": "Amsterdam",
  "skills": [
    "150a0419-4cca-4d96-9112-fa972b9ec170",
    "1cef7ebc-9524-4ae4-a16e-ab016e2503ec",
  ],
  "max_amount_of_hours": 10
}
```
> With a return code 201

Create a user

### Request
`POST /user/`

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
username | yes | String | - | The username of the user
first_name | yes | String | - | The first_name of the user
last_name | yes | String | - | The last_name of the user
date_of_birth | yes | Date (YYYY-MM-DD) | - | The date of birth of the user
profile_image | no | Base64 | - | The  of the user
location | yes | String | - | The location of the user
max_amount_of_hours | yes | Integer | - | The max amount of hours a user may work
[role](#role-parameter) | yes | String | - | The role of the user
skills | yes(empty allowed) | Array | - | List of id's of the skills a user possesses

### Role parameter
You can choose from

Role | Description
--------- | -----------
TEMP_WORKER | This role is given if the user is a temp worker or flex worker
EMPLOYMENT_AGENCY | This role is given if the user is a employee of a employment agency
CLIENT | This role is given if a user is a client from a specific employment agency

## List

> The returned JSON

```json
{
  {
    "id": "00329c9d-cea0-4c32-ae69-6002222d32ec",
    "username": "test6",
    "first_name": "test6",
    "last_name": "test6",
    "role": "TEMP_WORKER",
    "date_of_birth": "2018-01-01",
    "profile_image": null,
    "location": "Amsterdam",
    "max_amount_of_hours": 10,
    "location_lat": 52.35862,
    "location_lng": 4.90794,
    "employment_agency": {
        "id": "89914eeb-96bb-4cc6-b59a-04030b087d18",
        "name": "employmentAgencyCompany"
    },
    "skills": [
      {
        "id": "150a0419-4cca-4d96-9112-fa972b9ec170",
        "name": "Dienblad lopen"
      },
      {
        "id": "1cef7ebc-9524-4ae4-a16e-ab016e2503ec",
        "name": "> 1 jaar ervaring"
      },
      {
        "id": "885add89-ccf1-454c-b9f2-1930a9d3d681",
        "name": "> 2 jaar ervaring"
      },
      {
        "id": "e6a98f39-b3c9-4cc2-923f-726ed7abff64",
        "name": "> 3 jaar ervaring"
      }
    ]
  },
  {
    "id": "02e617f0-17b1-419a-a09c-eaa2b2829717",
    "username": "test65",
    "first_name": "test65",
    "last_name": "test65",
    "role": "TEMP_WORKER",
    "date_of_birth": "2018-01-01",
    "profile_image": null,
    "location": "Amsterdam",
    "max_amount_of_hours": 6,
    "location_lat": 52.35862,
    "location_lng": 4.90794,
    "employment_agency": {
        "id": "89914eeb-96bb-4cc6-b59a-04030b087d18",
        "name": "employmentAgencyCompany"
    },
    "skills": [
        {
            "id": "1cef7ebc-9524-4ae4-a16e-ab016e2503ec",
            "name": "> 1 jaar ervaring"
        },
        {
            "id": "37fe9a2d-639c-41b5-9f91-819add19ea9a",
            "name": "Public speaking"
        },
        {
            "id": "57957379-fd85-4d28-96c3-4045a533298e",
            "name": "Bier tappen"
        },
        {
            "id": "e6a98f39-b3c9-4cc2-923f-726ed7abff64",
            "name": "> 3 jaar ervaring"
        }
    ]
  }
}
```
> With a return code 200

List of users

### Request
`GET /user/`

## Retrieve

Getting a single user

> The returned JSON

```json
{
  "id": "00329c9d-cea0-4c32-ae69-6002222d32ec",
  "username": "test6",
  "first_name": "test6",
  "last_name": "test6",
  "role": "TEMP_WORKER",
  "date_of_birth": "2018-01-01",
  "profile_image": null,
  "location": "Amsterdam",
  "max_amount_of_hours": 10,
  "location_lat": 52.35862,
  "location_lng": 4.90794,
  "employment_agency": {
      "id": "89914eeb-96bb-4cc6-b59a-04030b087d18",
      "name": "employmentAgencyCompany"
  },
  "skills": [
    {
      "id": "150a0419-4cca-4d96-9112-fa972b9ec170",
      "name": "Dienblad lopen"
    },
    {
      "id": "1cef7ebc-9524-4ae4-a16e-ab016e2503ec",
      "name": "> 1 jaar ervaring"
    },
    {
      "id": "885add89-ccf1-454c-b9f2-1930a9d3d681",
      "name": "> 2 jaar ervaring"
    },
    {
      "id": "e6a98f39-b3c9-4cc2-923f-726ed7abff64",
      "name": "> 3 jaar ervaring"
    }
  ]
}
```
> With a return code 200

### Request
`GET /user/<id:string>/`

### Path parameter
Parameter | Description
--------- | -----------
id | The id of the user that you want to retrieve
