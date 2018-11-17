# Skill

A skill is something a shift and a user can have. It determines if a user is fit to work in a shift

## Create skill

> The returned JSON

```json
{
  "id": "7ac0419f-a139-4005-b22a-8acbebc0caf3",
  "name": "Skill 1"
}
```
> With a return code 201

Create a skill

### Request
`POST /skill/`

### Body
Parameter | Required | Type | Default | Description
--------- | ------- | ------- | ------- | -----------
name | yes | String | - | The name of the skill

## List skills

> The returned JSON

```json
[
  {
    "id": "7ac0419f-a139-4005-b22a-8acbebc0caf3",
    "name": "Skill 1"
  },
  {
    "id": "b068eb9d-cd38-4e32-b756-fa4c6ace7243",
    "name": "Skill 2"
  }
]
```
> With a return code 200

List of skills

### Request
`GET /skill/`

## Retrieve skill

Getting a single skill

> The returned JSON

```json
{
  "id": "7ac0419f-a139-4005-b22a-8acbebc0caf3",
  "name": "Skill 1"
}
```
> With a return code 200

### Request
`GET /skill/<id:string>/`

### Path parameter
Parameter | Description
--------- | -----------
id | The id of the skill that you want to retrieve
