# Security status

- Frontend prototype only; no server-side trust boundary exists here.
- Demo login is intentionally non-secure and must never be used for real accounts.
- All data is synthetic and client-side; browser edits are not authoritative.
- Do not store real passwords, API keys, daemon tokens, or private credentials in this project.
- Production deployment requires backend authentication and role checks on every privileged route, CSRF protection for cookie-authenticated requests, secure session cookies, input validation, output encoding, rate limiting, audit logs, and server-side secret management.
