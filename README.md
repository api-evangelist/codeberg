# Codeberg (codeberg)

Codeberg is a community-run, non-profit platform for hosting Git repositories and collaborating on free and open source software, operated by the Codeberg e.V. association in Germany. It runs on [Forgejo](https://forgejo.org/) (a community fork of Gitea) and exposes a Forgejo/Gitea-compatible REST API at `https://codeberg.org/api/v1` for repositories, issues, pull requests, releases, Git content, users, and organizations.

## Access model (read this first)

- **Free, donation-funded.** Codeberg is a registered non-profit. Hosting and the API are free to use; there are no paid API tiers. The service is sustained by donations and membership in Codeberg e.V. Use is expected to be for free and open source content and to stay within fair-use limits.
- **Authentication.** Most read access to public repositories works unauthenticated. For authenticated and write access, send a **personal access token** as `Authorization: token YOUR_TOKEN` (note the literal word `token`, not `Bearer`). **OAuth2** is also supported for apps, as is HTTP Basic auth (optionally with a TOTP header when two-factor auth is enabled). Create tokens under your Codeberg account settings.
- **Base URL.** `https://codeberg.org/api/v1`. The same API surface exists on any self-hosted Forgejo or Gitea instance.
- **Fair use.** Codeberg asks that automated/API use be reasonable and not degrade the shared community service; heavy scraping or bulk automation is discouraged. There are no published fixed numeric rate limits, but the instance may throttle abusive traffic.

**Live specification:** [https://codeberg.org/swagger.v1.json](https://codeberg.org/swagger.v1.json) (interactive UI at [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger))

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/codeberg/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/codeberg/refs/heads/main/apis.yml)

## Tags

- Code Hosting
- Git
- Git Hosting
- Version Control
- Repositories
- Pull Requests
- Issue Tracking
- Open Source
- Forgejo
- Non-Profit

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

### Codeberg Repositories API

Create, search, get, edit, and delete Git repositories, and list and create branches and tags. The core repository surface of the Forgejo/Gitea API, covering both user-owned and organization-owned repositories.

- **Human URL:** [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger)
- **Base URL:** `https://codeberg.org/api/v1`

#### Tags

- Repositories
- Git Hosting
- Branches

#### Properties

- [Documentation](https://docs.codeberg.org/advanced/api-usage/)
- [API Reference](https://codeberg.org/api/swagger)
- [OpenAPI](openapi/codeberg-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/codeberg.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/codeberg.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Codeberg Issues API

List, search, create, get, edit, and comment on issues within a repository. Supports cross-repository issue search across repositories the authenticated user can access.

- **Human URL:** [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger)
- **Base URL:** `https://codeberg.org/api/v1`

#### Tags

- Issue Tracking
- Issues
- Comments

#### Properties

- [Documentation](https://docs.codeberg.org/advanced/api-usage/)
- [API Reference](https://codeberg.org/api/swagger)
- [OpenAPI](openapi/codeberg-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/codeberg.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/codeberg.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Codeberg Pull Requests API

List, create, get, and update pull requests, check whether a pull request has been merged, and merge it. The code-review and contribution surface of the Forgejo/Gitea API.

- **Human URL:** [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger)
- **Base URL:** `https://codeberg.org/api/v1`

#### Tags

- Pull Requests
- Code Review
- Merge

#### Properties

- [Documentation](https://docs.codeberg.org/advanced/api-usage/)
- [API Reference](https://codeberg.org/api/swagger)
- [OpenAPI](openapi/codeberg-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/codeberg.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/codeberg.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Codeberg Users and Organizations API

Get the authenticated user, look up and search users, list who a user follows and is followed by, and get and manage organizations and the repositories they own.

- **Human URL:** [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger)
- **Base URL:** `https://codeberg.org/api/v1`

#### Tags

- Users
- Organizations
- Profiles

#### Properties

- [Documentation](https://docs.codeberg.org/advanced/api-usage/)
- [API Reference](https://codeberg.org/api/swagger)
- [OpenAPI](openapi/codeberg-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/codeberg.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/codeberg.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Codeberg Releases API

List, create, get, update, and delete repository releases, and fetch the latest non-prerelease release. Releases attach downloadable assets to Git tags.

- **Human URL:** [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger)
- **Base URL:** `https://codeberg.org/api/v1`

#### Tags

- Releases
- Tags
- Distribution

#### Properties

- [Documentation](https://docs.codeberg.org/advanced/api-usage/)
- [API Reference](https://codeberg.org/api/swagger)
- [OpenAPI](openapi/codeberg-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/codeberg.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/codeberg.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Codeberg Git Content API

Read and write repository contents - list directory entries, get and create, update, or delete files, fetch raw file bytes, list commits, and read the Git tree. The file-and-content surface of the Forgejo/Gitea API.

- **Human URL:** [https://codeberg.org/api/swagger](https://codeberg.org/api/swagger)
- **Base URL:** `https://codeberg.org/api/v1`

#### Tags

- Git Content
- Files
- Commits

#### Properties

- [Documentation](https://docs.codeberg.org/advanced/api-usage/)
- [API Reference](https://codeberg.org/api/swagger)
- [OpenAPI](openapi/codeberg-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/codeberg.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/codeberg.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Domain Security](security/codeberg-domain-security.yml)
- [Authentication](authentication/codeberg-authentication.yml)
- [GitHub Organization](https://github.com/forgejo/forgejo)
- [Fediverse](https://social.anoxinon.de/@codeberg)
- [Website](https://codeberg.org)
- [Documentation](https://docs.codeberg.org)
- [Plans](plans/codeberg-plans-pricing.yml)
- [Rate Limits](rate-limits/codeberg-rate-limits.yml)
- [Fin Ops](finops/codeberg-finops.yml)
- [Blog](https://blog.codeberg.org/)

## Review

An API Evangelist review of whether Codeberg exposes a documented public WebSocket API is in [review.yml](review.yml). Answer: **no** - Codeberg's API is REST over HTTPS with outbound webhooks for eventing; there is no documented `wss://` endpoint, so no AsyncAPI document was authored.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
