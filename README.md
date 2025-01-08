# Styleguide

This repository contains our code style guide which is agnostic from programming languages.

## API's and contracts

Within UUG.AI we embrace the concept of Microservices... 

### Error response

    c.JSON(api.CreateError(
			api.StatusBadRequest,
			models.FILTER_TASKS_FAILED,
			api.MetaData{
				UserId: user.Id.Hex(),
			},
    ))

