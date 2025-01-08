# Styleguide

This repository contains our code style guide which is agnostic from programming languages.

## Table of Contents

1. [General Guidelines](#general-guidelines)
2. [Code Structure](#code-structure)
3. [Naming Conventions](#naming-conventions)
4. [Comments and Documentation](#comments-and-documentation)
5. [Formatting and Style](#formatting-and-style)
6. [Error Handling](#error-handling)
7. [Version Control](#version-control)
8. [Code Reviews](#code-reviews)
9. [Testing Practices](#testing-practices)
10. [Security Considerations](#security-considerations)

## General Guidelines

- **Consistency is key**: Follow a uniform style guide for the project or team.
- **Keep it simple**: Write code that is easy to understand, avoiding unnecessary complexity.
- **Focus on readability**: Optimize code for humans first, not just machines.
- **Adopt automation**: Use linters, formatters, and CI/CD tools to enforce standards.

## Code Structure

- Organize code logically with clear separation of concerns.
- Use modular design: Break down functionality into smaller, reusable components or functions.
- Avoid deeply nested structures; aim for a flat and concise hierarchy.
- Group related code together (e.g., functions, classes, constants).

## Naming Conventions

- Use meaningful, descriptive names for variables, functions, classes, and files.
- Follow consistent casing rules (e.g., camelCase, snake_case, or PascalCase).
- Avoid abbreviations unless they are widely recognized.
- Use plural forms appropriately (e.g. `users` for collections).

## Comments and Documentation

- Write comments to explain the "why," not the "what," unless the code is non-obvious.
- Keep comments up-to-date as the code evolves.
- Use docstrings or annotations for public APIs, functions, and modules.
- Maintain a clear and concise README file for project-level documentation.

## Formatting and Style

- Use consistent indentation (e.g., 2 or 4 spaces, never tabs).
- Limit line length (e.g., 80 or 120 characters).
- Include a blank line between sections of code to improve readability.
- Ensure braces, parentheses, and brackets are properly aligned and matched.

## Error Handling

- Validate inputs and handle edge cases explicitly.
- Log meaningful error messages to aid debugging.
- Avoid using generic exception handling; catch specific exceptions where possible.
- Ensure the application fails gracefully under unexpected conditions.

## Version Control

- Use meaningful commit messages that describe the changes made.
- Follow a branching strategy (e.g., Git Flow, Trunk-Based Development).
- Commit early and often, but ensure commits are atomic (single-purpose changes).
- Review and resolve merge conflicts thoughtfully.

## Code Reviews

- Focus on improving code quality, not criticizing the author.
- Review for functionality, readability, performance, and adherence to standards.
- Provide actionable, constructive feedback.
- Encourage discussions to clarify decisions or resolve ambiguities.

## Testing Practices

- Write unit tests for all critical functions or components.
- Use integration and end-to-end tests to validate overall functionality.
- Follow Test-Driven Development (TDD) where applicable.
- Aim for high test coverage without compromising test quality.

## Security Considerations

- Avoid hardcoding sensitive data like API keys, credentials, or tokens.
- Sanitize and validate all user inputs to prevent vulnerabilities.
- Use secure libraries and frameworks where possible.
- Regularly update dependencies to address known security issues.

## Contributions

We welcome contributions to improve this guide. Please follow the contribution guidelines outlined in [CONTRIBUTING.md](CONTRIBUTING.md).

## Domain driven design

- Protocol buffers

## API's and contracts

Within UUG.AI we embrace the concept of Microservices...

### Responses

#### Success response

    ...

#### Error response

    c.JSON(api.CreateError(
    		api.StatusBadRequest,
    		models.FILTER_TASKS_FAILED,
    		api.MetaData{
    			UserId: user.Id.Hex(),
    		},
    ))

### Request

#### [PATCH] Updating objects

To update information in the API, use the `PATCH` method. Construct the request URL with the resource identifier, such as `PATCH /{resource}/{id}`. The request body should contain the following parameters:

- **id**: A string representing the ID of the resource to be updated.
- **updates**: An object containing the delta with the fields that should be updated.

Fields that should never be updated will be removed from the request by the API before applying the updates.

Upon a successful update, the API should return a response with a status code of `200 OK`. The response body will include a `Data` object, which contains the fields that were updated, and a `message` string, which provides a success message indicating that the update was successful.
