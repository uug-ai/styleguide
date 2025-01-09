# Styleguide

This repository contains our code style guide, which is agnostic of programming languages. The goal of this guide is to improve the quality and uniformity of the code we write.

We currently implement the following programming languages:

- **Golang**: For APIs, microservices, and media.
- **Python**: For data science, machine learning, and computer vision (OpenCV).
- **TypeScript/JavaScript**: For building web-based user interfaces.

We may explore other programming languages in the future, such as Rust. The principles in this repository should apply to any language, and updates will be made as necessary.

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
11. [Domain driven design](#domain-driven-design)
12. [APIs and Contracts](#api)
13. [Observability](#observability)

## General Guidelines

- Repository naming should be easy, and ideally be a described using single word (cli, hub, admin, etc).
- Seperation of concerns: break down complex code in one ore more functions or repositories.

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

We use [GitHub Pull Requests](https://github.blog/developer-skills/github/beginners-guide-to-github-creating-a-pull-request/) to evaluate and contribute new work.

- Create a new branch named: (bug/pr-description, feature/pr-description, or enhancement/pr-description)
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

## Domain driven design

...

## APIs and contracts

...

## Observability

- OpenTelemetry (to be implemented).

## Contributions

We welcome contributions to improve this guide. Please follow the contribution guidelines outlined in [CONTRIBUTING.md](CONTRIBUTING.md).
