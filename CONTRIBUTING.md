# Contributing

## Scope

This repository is intended to hold shareable Postman assets for the Hicap API.

Keep changes focused on:

- request definitions
- environment templates without secrets
- test scripts that validate API responses
- repository documentation

## Guidelines

1. Do not commit API keys, tokens, or private endpoints.
2. Treat files under `postman/environments` as templates unless they are explicitly meant to be tracked.
3. Prefer descriptive request names that match the API capability being demonstrated.
4. Keep request examples minimal and reproducible.
5. When adding tests, validate stable fields such as status codes, IDs, object types, and response structure.
6. Preserve the existing folder structure under `postman/collections/Hicap v1` unless there is a clear organizational reason to change it.

## Adding a new request

1. Place the request in the appropriate folder under `postman/collections/Hicap v1`.
2. Use `{{base_url}}` and `{{api-key}}` instead of hard-coded values.
3. Add a small `afterResponse` test script when practical.
4. Make sure the example body is safe to publish.

## Reviewing changes

Before opening a pull request, verify:

- the request still uses environment variables for credentials and host configuration
- any example payloads are public-safe
- tests match the actual response schema
- documentation stays in sync with the collection structure