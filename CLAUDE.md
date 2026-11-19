# CLAUDE.md — Proto

API contracts for StreamNext. Read `../CLAUDE.md` and `../docs/specs/02-architecture.md` first.

- `openapi/v1/streamnext.yaml` is the REST contract: **hand-written**, never generated from backend code. Backend generates its server from it (oapi-codegen); clients generate theirs.
- `streamnext/v1/*.proto` are shared **messages and enums only** — no `service` blocks. Published to BSR `buf.build/streamnext/streamnext` by CI on `main` (`BUF_TOKEN` repo secret).
- Error bodies are lowercase `{code, message}`.
- Every contract change bumps `info.version` and adds a `CHANGELOG.md` entry (semver; major = breaking).
- Lint locally: `buf lint && npx --yes @redocly/cli@1.34.5 lint openapi/v1/streamnext.yaml`.

## Git
Work on `develop`, open a PR to `main`, auto-merge when CI is green. No AI attribution trailers in commits.
