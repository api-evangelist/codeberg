# Codeberg (codeberg)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
