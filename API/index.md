## Update

To update information in the API, use the `PATCH` method. Construct the request URL with the resource identifier, such as `PATCH /{resource}/{id}`. The request body should contain the following parameters:

- **id**: A string representing the ID of the resource to be updated.
- **updates**: An object containing the delta with the fields that should be updated.

Fields that should never be updated will be removed from the request by the API before applying the updates.

Upon a successful update, the API should return a response with a status code of `200 OK`. The response body will include a `Data` object, which contains the fields that were updated, and a `message` string, which provides a success message indicating that the update was successful.

## Responses

# Status codes:

Possible status codes returned by the API:

- `200`: **StatusOK** - OK
- `201`: **StatusCreated** - Created
- `401`: **StatusUnauthorized** - Unauthorized
- `400`: **StatusBadRequest** - Bad Request
- `500`: **StatusInternalServerError** - Internal Server Error
- `404`: **StatusNotFound** - Not Found

# Success

Upon a successful update, the API returns a 200 OK status code and these parameters:

- **status_code**: The HTTP status code of the response.
- **request_id**: A unique identifier for the request.
- **meta_data**: Metadata about the request, including the user ID, timestamp, any error information, and the request path.
- **success_code**: A custom code indicating the type of success.
- **message**: A message indicating that the update was successful.
- **data**: An object containing the updated fields of the resource.

Example response:

	{
			"statuscode": 200,
			"requestId": "123456",
			"meta_data": {
				"user_id": "123456",
				"timestamp": 1234567890,
				"error": "error"
				"path": "/api/v1/xxx"
			},
			"successCode": "success_code",
			"message": "Success message",
			"data": {}
	}

# Error

If the update fails, the API returns an appropriate error status code (e.g., 400 Bad Request, 500 Internal Server Error) and these parameters:

- **status_code**: The HTTP status code of the response.
- **request_id**: A unique identifier for the request.
- **meta_data**: Metadata about the request, including the user ID, timestamp, any error information, and the request path.
- **error_code**: A custom code indicating the type of error.
- **message**: A message indicating the reason for the failure.

Example response:

	{
		"statuscode": 400,
		"requestId": "123456",
		"meta_data": {
			"user_id": "123456",
			"timestamp": 1234567890,
			"error": "error"
			"path": "/api/v1/xxx"
		},
		"errorCode": "error_code",
		"message": "Error message"
	}
