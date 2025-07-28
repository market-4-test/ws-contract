# Contracts

This repository stores the WebSocket Service contracts for interaction between the client and the server.

-----

## Supported Languages

The contracts are automatically built and published to separate repositories for the following languages:

  * **TypeScript**: [market-4-test/contract-ts](https://github.com/market-4-test/contract-ts)

-----

## Usage

The `Taskfile` is used to generate code from the `.proto` files.

You can generate the code for all languages using the following command:

```bash
task generate
```

Or `task gen` for short.

This command will perform the following steps:

2.  Generate TypeScript code into the `dist/ts` directory.

-----

## CI/CD

The continuous integration and deployment process is set up using GitHub Actions.

When a new release is created in GitHub, the process of building and publishing packages is automatically triggered.

The main steps of the process are:

1.  Login to the GitHub Container Registry.
2.  Build `.proto` files using a Docker image.
3.  Publish the generated code to the corresponding repositories.

-----

## Dependencies

The project uses `@protobuf-ts/plugin` to generate TypeScript code.
