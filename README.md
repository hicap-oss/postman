# Hicap Postman Collection

This repository contains Postman assets for the Hicap API.

It is organized as a Postman project with request definitions stored as YAML under `postman/collections/Hicap v1` and environment templates under `postman/environments`.

## What is included

- Chat completion and responses examples
- Function calling and multi-turn conversation examples
- Audio transcription and text-to-speech requests
- Embeddings requests
- Image generation requests
- Model and health-check requests

## Repository layout

```text
postman/
  collections/
    Hicap v1/
  environments/
    hicap.ai.environment.yaml
    fastly.environment.yaml
  globals/
    workspace.globals.yaml
.postman/
  resources.yaml
```

## Getting started

1. Clone this repository.
2. Open Postman.
3. Import the project folder or import the collection and environment files directly from this repository.
4. Select the environment that matches the endpoint you want to call.
5. Set these environment variables before sending requests:

| Variable | Required | Description |
| --- | --- | --- |
| `base_url` | Yes | Base URL for the Hicap API, for example `https://api.example.com` |
| `api-key` | Yes | API key sent in the `api-key` header |

Available environment templates:

- `postman/environments/hicap.ai.environment.yaml` for the primary Hicap API configuration
- `postman/environments/fastly.environment.yaml` for deployments that route requests through a Fastly-backed endpoint

## Running requests

Most requests live under `postman/collections/Hicap v1` and include basic test scripts that validate status codes and key response fields.

## Examples

- [Basic Chat Completion](postman/collections/Hicap%20v1/Chat%20Completions/Basic%20Chat%20Completion.request.yaml)
- [Basic Responses](postman/collections/Hicap%20v1/Chat%20Completions/Basic%20Responses.request.yaml)
- [Function Calling](postman/collections/Hicap%20v1/Chat%20Completions/Function%20Calling.request.yaml)
- [Audio Transcription](postman/collections/Hicap%20v1/Audio/Audio%20Transcription.request.yaml)
- [Create Embedding](postman/collections/Hicap%20v1/Embeddings/Create%20Embedding.request.yaml)
- [Generate Image](postman/collections/Hicap%20v1/Image%20Generation/Generate%20Image.request.yaml)
- [Get Model](postman/collections/Hicap%20v1/Models/Get%20Model.request.yaml)

## Notes for public use

- Do not commit secrets to environment files.
- The repository keeps `postman/environments/hicap.ai.environment.yaml` as a tracked template and ignores other local environment files through the root `.gitignore`.
- Request files are plain YAML, so changes can be reviewed in pull requests.
- Public reuse is governed by the [MIT License](LICENSE).

## Contributing

See `CONTRIBUTING.md` for conventions on adding or updating requests.