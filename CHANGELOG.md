# Changelog

Semver. Minor = new endpoint/feature, patch = fix, major = breaking contract change.
The version is `info.version` in `openapi/v1/streamnext.yaml`.

## 0.2.0 — 2026-11-19
- Auth core (M1 slice 1): `POST /v1/auth/{register,login,refresh,logout}`, `GET`/`PATCH /v1/me`, the `bearerAuth` scheme, and shared 400/401/409/429 responses.

## 0.1.0 — 2026-11-19
- `GET /v1/health` and the shared `Error` schema.
- buf module `buf.build/streamnext/streamnext` with `streamnext.v1.ApiError`.
