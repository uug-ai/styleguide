# Styleguide

This repository contains our code style guide which is agnostic from programming languages.

## Domain driven design

- Protocol buffers

## API's and contracts

Within UUG.AI we embrace the concept of Microservices... 

### Success response

    ... 

### Error response

    c.JSON(api.CreateError(
			api.StatusBadRequest,
			models.FILTER_TASKS_FAILED,
			api.MetaData{
				UserId: user.Id.Hex(),
			},
    ))


### Updating / PATCH

To update information in the API, use the `PATCH` method. Construct the request URL with the resource identifier, such as `PATCH /{resource}/{id}`. The request body should contain the following parameters:

- **id**: A string representing the ID of the resource to be updated.
- **updates**: An object containing the delta with the fields that should be updated.

Fields that should never be updated will be removed from the request by the API before applying the updates.

Upon a successful update, the API should return a response with a status code of `200 OK`. The response body will include a `Data` object, which contains the fields that were updated, and a `message` string, which provides a success message indicating that the update was successful.
