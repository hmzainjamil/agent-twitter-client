# agent-twitter-client

A TypeScript/JavaScript client package for interacting with X/Twitter. The source includes authentication, search, profile, timeline, relationship, tweet, and media/space modules. It supports cookie-based account login and a v2 API client path; access and behavior depend on the configured account and platform.

## At a glance

| Item | Source evidence |
|---|---|
| Package | `agent-twitter-client`, version field `0.0.18` in `package.json` |
| Build | Rollup build via `npm run build` |
| Tests | Jest via `npm test`; tests exist in `src/` |
| Example credentials | `.env.example` lists login, API credential, and optional proxy variables |
| CI | A GitHub Actions workflow installs dependencies and runs the build on pushes to `main`; this does not establish current CI results |
| Verification | No build, test, login, or account action was run for this documentation update |

## Install and build

Use Node.js and npm compatible with the project dependencies:

```bash
npm ci
npm run build
```

The package manifest also defines `npm test`. Review the test setup before running tests that may need credentials or network access.

For API details, read the source under [`src/`](src/) and the [sample agent](SampleAgent.js). The sample's login and posting code is commented out; it is not an active demo.

## Authentication and account actions

The code supports cookie-based login and API credential authentication. Treat passwords, cookies, session tokens, API keys, and proxy configuration as secrets. Use a dedicated test account where possible. Review any post, reply, follow, message, or other write action before executing it.

This is an unofficial client. Platform behavior, access, and permitted use can change. This README makes no claim that cookie login avoids API costs, bypasses limits, or guarantees account access.

## License and provenance

See [LICENSE](LICENSE) for the terms and copyright notices included with this source. Preserve those notices when redistributing or adapting the package.

## Documentation

See the [documentation index](docs/README.md) and [security notes](SECURITY.md).
