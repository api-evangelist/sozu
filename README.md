# Sozu

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Sōzu is an open-source, fast and lightweight HTTP reverse proxy written in Rust, designed for high-performance traffic management in immutable infrastructure environments. It is configurable at runtime through a protobuf-based IPC protocol without requiring restarts, making it ideal for always-up deployments. Sōzu supports TLS termination, load balancing, and dynamic cluster configuration, and is developed by the sozu-proxy open-source organization on GitHub.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/sozu/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Proxy
- Reverse Proxy
- Load Balancing
- Rust
- Open Source

## Timestamps

- **Created:** 2026-03-27
- **Modified:** 2026-05-02

## APIs

### Sozu Command API

The Sozu Command API provides programmatic control of the Sōzu HTTP reverse proxy at runtime. External tools communicate with the Sozu main process through a secure Unix socket using a protobuf-based binary protocol (IPC). The sozu-command-lib crate ships the protobuf schema, configuration parser, replicated state, channels, and file descriptor passing helpers. This enables dynamic cluster configuration, certificate management, and backend routing changes without restarts.

- [Documentation](https://docs.sozu.io/)
- [GitHub](https://github.com/sozu-proxy/sozu)
- [Getting Started](https://docs.sozu.io/getting-started/)
- [Configuration Guide](https://github.com/sozu-proxy/sozu/blob/main/doc/configure.md)
- [JSON Schema - Cluster](https://raw.githubusercontent.com/api-evangelist/sozu/refs/heads/main/json-schema/sozu-cluster-schema.json)
- [JSON Schema - Frontend](https://raw.githubusercontent.com/api-evangelist/sozu/refs/heads/main/json-schema/sozu-frontend-schema.json)

### Sozu ACME Integration

The Sozu ACME integration automates TLS certificate requests from Let's Encrypt and other ACME-enabled certificate authorities. Now integrated directly into the main Sōzu binary.

- [GitHub](https://github.com/sozu-proxy/sozu-acme)

### Sozu Command Futures API

The sozu-command-futures library provides a futures-based async Rust API for configuring the Sōzu HTTP reverse proxy programmatically.

- [GitHub](https://github.com/sozu-proxy/sozu-command-futures)

## Common Properties

- [Website](https://www.sozu.io/)
- [Documentation](https://docs.sozu.io/)
- [GitHub Organization](https://github.com/sozu-proxy)
- [GitHub Repository](https://github.com/sozu-proxy/sozu)
- [Releases](https://github.com/sozu-proxy/sozu/releases)
- [Dashboard](https://github.com/sozu-proxy/dashboard)
- [Integration Tests](https://github.com/sozu-proxy/sozu-integration-tests)

## Artifacts

### JSON Schemas

| Schema | Description |
|---|---|
| [sozu-cluster-schema.json](json-schema/sozu-cluster-schema.json) | Backend cluster configuration including load balancing and backend instances |
| [sozu-frontend-schema.json](json-schema/sozu-frontend-schema.json) | Frontend routing rule binding hostname/path to a backend cluster |

### JSON Structure

| Structure | Description |
|---|---|
| [sozu-configuration-structure.json](json-structure/sozu-configuration-structure.json) | Hierarchical structure of proxy configuration: listeners, clusters, frontends, and certificates |

### JSON-LD Context

| Context | Description |
|---|---|
| [sozu-context.jsonld](json-ld/sozu-context.jsonld) | Linked data context mapping Sozu proxy configuration vocabulary to schema.org |

### Examples

| Example | Description |
|---|---|
| [sozu-cluster-example.json](examples/sozu-cluster-example.json) | Sample cluster configuration with two backend instances |
| [sozu-frontend-example.json](examples/sozu-frontend-example.json) | Sample HTTPS frontend routing rule |

### Vocabulary

| Vocabulary | Description |
|---|---|
| [sozu-vocabulary.yml](vocabulary/sozu-vocabulary.yml) | Domain vocabulary for Sozu reverse proxy configuration and operations |

## GitHub Organization Repositories

The [sozu-proxy](https://github.com/sozu-proxy) GitHub organization maintains the following repositories:

| Repository | Description |
|---|---|
| [sozu](https://github.com/sozu-proxy/sozu) | Main HTTP reverse proxy binary and library |
| [sozu-acme](https://github.com/sozu-proxy/sozu-acme) | ACME/Let's Encrypt certificate automation |
| [sozu-command-futures](https://github.com/sozu-proxy/sozu-command-futures) | Futures-based async Rust API for Sozu configuration |
| [dashboard](https://github.com/sozu-proxy/dashboard) | Experimental management dashboard |
| [sozu-integration-tests](https://github.com/sozu-proxy/sozu-integration-tests) | Integration test suite using Testcontainers |
| [tube-cheese](https://github.com/sozu-proxy/tube-cheese) | Configuration manager based on Traefik patterns |
| [sozu-demo](https://github.com/sozu-proxy/sozu-demo) | Demo configurations and usage examples |

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
