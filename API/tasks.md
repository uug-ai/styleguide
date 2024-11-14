# Tasks

## Create Task

## Read Task

## Update Task

### Request

PATCH /tasks/{id}

- id: string \
Id of the task

- updates: object \
The fields of the task that should be updated

#### Notes

- Any fields that should never be updated like _id, user_id, or creation_date will be removed from the updates data. \

### Response

**200**

- Data: object \
The fields that were updated

- message: string \
Success message

## Delete Task
