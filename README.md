# Sozu

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
