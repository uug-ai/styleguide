# Tasks

## Create Task

## Read Task

## Update Task

### Request

PATCH /tasks/{id}

- id: string
Id of the task

- updates: object
The fields of the task that should be updated

### Response

**200**

- Data: object
The fields that were updated

- message: string
success message

## Delete Task