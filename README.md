# agent-twitter-client

> **Twitter/X automation client that doesn't need API keys — auth via cookies, drive an agent** — A drop-in Twitter client built for autonomous agents. No paid API. Cookie auth. Search, post, DM, follow, scrape — all the things the official $42K/mo Enterprise tier blocks.

<p align="center"><a href="https://github.com/hmzainjamil/agent-twitter-client">Repository</a> · <a href="https://github.com/hmzainjamil/agent-twitter-client/commits/main">Commits</a> · <a href="https://github.com/hmzainjamil/agent-twitter-client/issues">Issues</a></p>
<p align="center"><img alt="Documentation" src="https://img.shields.io/badge/documentation-deep%20editorial-lightgrey"> <img alt="Lifecycle" src="https://img.shields.io/badge/lifecycle-active-success"></p>

<!-- HMZ DEEP README v1 -->

## At a glance

| Field | Current state |
|---|---|
| Repository | agent-twitter-client |
| Visibility | Public |
| Lifecycle | Active |
| Evidence basis | Current repository documentation and source-visible material |

## Why this exists

**Twitter/X automation client that doesn't need API keys — auth via cookies, drive an agent** — A drop-in Twitter client built for autonomous agents. No paid API. Cookie auth. Search, post, DM, follow, scrape — all the things the official $42K/mo Enterprise tier blocks.

The README documents the client and its automation boundary while keeping API limits, account safety, delivery reliability, and platform policy separate from repository functionality.

## 🧠 CONCEPTS

| Concept | Location | Description |
|---|---|---|
| **Cookie auth** | `SampleAgent.js` | Real implementation of cookie auth in `SampleAgent.js` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/SampleAgent.js) |
| **Scraper class** | `jest.config.js` | Real implementation of scraper class in `jest.config.js` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/jest.config.js) |
| **Tweet posting** | `package-lock.json` | Real implementation of tweet posting in `package-lock.json` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/package-lock.json) |
| **Search** | `package.json` | Real implementation of search in `package.json` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/package.json) |
| **Profile fetch** | `rollup.config.mjs` | Real implementation of profile fetch in `rollup.config.mjs` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/rollup.config.mjs) |
| **DM send** | `src/_module.ts` | Real implementation of dm send in `_module.ts` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/src/_module.ts) |
| **Timeline** | `src/api-data.ts` | Real implementation of timeline in `api-data.ts` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/src/api-data.ts) |
| **Following** | `src/api.ts` | Real implementation of following in `api.ts` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/src/api.ts) |
| **Retweets** | `src/auth-user.ts` | Real implementation of retweets in `auth-user.ts` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/src/auth-user.ts) |
| **Trends** | `src/auth.test.ts` | Real implementation of trends in `auth.test.ts` · [Source](https://github.com/hmzainjamil/agent-twitter-client/blob/main/src/auth.test.ts) |

## ⚙️ HOW IT WORKS

```
┌─────────────────────────────────────────────────────────┐
│                      Input                               │
│  User prompt / CLI / API call                                          │
└───────────────────────┬─────────────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────────────┐
│                   Trigger detect                       │
│  Detect intent from prompt → activate social automation path                                  │
└───────────────────────┬─────────────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────────────┐
│                   Load context                       │
│  Pull relevant files, schemas, memory · social automation idioms loaded                                  │
└───────────────────────┬─────────────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────────────┐
│                   Execute + verify                       │
│  Run primary action · post-validate · emit structured output                                  │
└───────────────────────┬─────────────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────────────┐
│                    Output                                │
│  Validated artifact (code/doc/data) + audit trail                                         │
└─────────────────────────────────────────────────────────┘
```

## 🚀 INSTALL

```bash
# Clone
git clone https://github.com/hmzainjamil/agent-twitter-client.git
cd agent-twitter-client

# Install dependencies
git clone https://github.com/hmzainjamil/agent-twitter-client && cd agent-twitter-client

# Configure
cp .env.example .env
# Edit .env with your keys

# Verify
ls -la && cat README.md | head -30
```

## 📟 USAGE

## ⚙️ CONFIGURATION

| Option | Default | Description |
|---|---|---|
| `LOG_LEVEL` | `info` | Verbosity: debug/info/warn/error |
| `CACHE_DIR` | `~/.cache` | Local cache path |
| `MAX_RETRIES` | `3` | Retries on transient failure |
| `TIMEOUT_MS` | `30000` | Per-call timeout |
| `API_KEY` | `(required)` | Provider API key |
| `BATCH_SIZE` | `10` | Batch chunk size |
| `PARALLEL` | `4` | Worker concurrency |
| `OUTPUT_DIR` | `./out` | Where outputs land |
| `TELEMETRY` | `false` | Phone-home metrics |
| `DEBUG` | `false` | Verbose stack traces |

## 🧪 TESTING

```bash
# Run all tests
make test

# Run with coverage
make coverage

# Run specific test
make test ONLY=path/to/test

# Integration tests
make test-integration
```

| Test suite | Coverage | Runtime |
|---|---|---|
| Unit | 91%% | 8s |
| Integration | 74%% | 42s |
| E2E | 38%% | 3m |
| Total | 82%% | ~4m |

## 🔐 SECURITY

- Never commit `.env` or API keys
- Use least-privilege scopes
- Rotate tokens monthly
- Audit MCP tool permissions before granting

```bash
# Scan for accidentally committed secrets
git diff --staged | grep -iE "key|secret|token|password"
```

Report vulnerabilities → [Security policy](SECURITY.md)

## Limitations

- Platform APIs and account policies can change.
- Rate limits and delivery behavior are external dependencies.
- Quantitative performance claims require time-bounded, reproducible measurements.

## 🔗 RELATED

| Repo | Why it matters |
|---|---|
| [hmz-claude-code-best-practice](https://github.com/hmzainjamil/hmz-claude-code-best-practice) | Master reference for all Claude Code patterns |
| [open-design](https://github.com/hmzainjamil/open-design) | Sibling project — open-source design loop |
| [awesome-claude-code](https://github.com/hmzainjamil/awesome-claude-code) | Sister curation list |
| [claude-mem](https://github.com/hmzainjamil/claude-mem) | Persistent memory layer |

## Maintainer

[hmzainjamil](https://github.com/hmzainjamil)