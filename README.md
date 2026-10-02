# @crowsi/interaction-transport

Carry bounded UI interaction messages between a caller and an application handler.

## What you can do

- Validate transport framing and cancellation.
- Keep opaque interaction payloads within declared limits.

## Current scope

The host supplies application routing and authority. Transport does not interpret the business operation.

Package distribution is not activated by this documentation. Use the checked-in source and the declared dependency versions; published availability must be verified separately.

## Getting started

Use the package manager matching the checked-in lockfile and the Node.js version declared in `engines` in `package.json`. Run from this repository:

```sh
npm install
npm run test
```

## Documentation and source

[Usage guide](docs/getting-started.md)

[Implementation and public interfaces](src) · [Verification cases](test) · [Contributing](CONTRIBUTING.md) · [Security reporting](SECURITY.md) · [License](LICENSE) · [Attribution notices](NOTICE)
