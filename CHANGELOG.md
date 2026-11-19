# Changelog

Semver. Minor = new endpoint/feature, patch = fix, major = breaking contract change.
The version is `info.version` in `openapi/v1/streamnext.yaml`.

## 0.4.0 — 2026-11-19
- Social sign-in and devices (M1 slice 3): `POST /v1/auth/apple`, `POST /v1/auth/google`, `PUT`/`DELETE /v1/devices/{deviceId}` (the first path parameter), and a shared 503 response.

## 0.3.0 — 2026-11-19
- Auth email flows and account (M1 slice 2): `POST /v1/auth/{verify-email,resend-verification,forgot-password,reset-password}`, `POST /v1/me/change-password`, `DELETE /v1/me`, and a shared 403 response.
- Email links (implemented by the Web repo later): `{APP_BASE_URL}/verify-email?token=…` and `{APP_BASE_URL}/reset-password?token=…`.

## 0.2.0 — 2026-11-19
- Auth core (M1 slice 1): `POST /v1/auth/{register,login,refresh,logout}`, `GET`/`PATCH /v1/me`, the `bearerAuth` scheme, and shared 400/401/409/429 responses.

## 0.1.0 — 2026-11-19
- `GET /v1/health` and the shared `Error` schema.
- buf module `buf.build/streamnext/streamnext` with `streamnext.v1.ApiError`.
