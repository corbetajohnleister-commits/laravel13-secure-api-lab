# Submission: Secure API with Laravel 13

* **Name:** John Leister A. Corbeta
* **Course:**  BS Information Technology
* **Section:** Integrative Programming & Technologies II

## Postman Evidence Checklist

-   `evidence/01-public-api-200.png` — Public endpoint (`GET /api/hello`)
-   `evidence/02-register-201.png` — User registration (`POST /api/register`)[cite: 3]
-   `evidence/03-login-200.png` — User login & token generation (`POST /api/login`)[cite: 3]
-   `evidence/04-profile-no-token-401.png` — Protected access without token (`GET /api/profile`)[cite: 3]
-   `evidence/05-profile-with-token-200.png` — Authenticated profile access (`GET /api/profile`)[cite: 3]
-   `evidence/06-invalid-login-422.png` — Failed login with wrong password (`POST /api/login`)[cite: 3]
-   `evidence/07-logout-200.png` — Token revocation / Logout (`POST /api/logout`)[cite: 3]
-   `evidence/08-revoked-token-401.png` — Post-logout profile access check (`GET /api/profile`)[cite: 3]


## Reflection

A `401 Unauthorized` response indicates that the request lacks valid authentication credentials or that the provided token is missing/invalid, blocking access to protected routes. In contrast, a successful authenticated profile response returns the user's data when a valid Bearer token is provided. After logging out, the current access token is deleted from the database, rendering it invalid and causing any subsequent requests using that same token to fail with a `401 Unauthorized` error.