# API Governance (governance)

API Governance is the practice of defining and enforcing the policies, standards, and processes that guide how APIs are designed, built, secured, versioned, and retired across an organization. This topic indexes the providers and tools that operationalize governance — and the machine-readable contracts (schemas, vocabulary, JSON-LD, examples) for describing a governance program as data.

## The Landscape

Governance happens on four axes. Each axis has dedicated tooling and a different point in the lifecycle where it bites.

### Spec Governance

Making the contract correct, complete, and parseable. The de facto engine is **Spectral**, an open-source JSON/YAML linter that ships rules for OpenAPI, AsyncAPI, and JSON Schema and is embedded inside most commercial platforms. **Vacuum** is a Go-based, Spectral-compatible alternative that adds OpenAPI 3.2 support, auto-fix, and change detection. **Apicurio Registry** governs spec correctness at the artifact level — OpenAPI, AsyncAPI, Avro, Protobuf, JSON Schema, GraphQL, WSDL, XSD — and enforces validity, compatibility, and integrity rules across versions.

### Design Governance

Making the contract good — consistent naming, error shape, pagination, versioning, and authentication scheme across the estate. This is where **style guides** live. **Stoplight Spaces** (now part of SmartBear's API Hub) provides built-in and custom Spectral rulesets at the workspace level. **Postman API Governance** ships a pre-built rule library, supports custom Spectral-compatible rules, and enforces them in collections, workspaces, and CI via the Postman CLI. **Redocly Reunite** wraps Redocly's OpenAPI linting into a Git-backed review workflow with previews and audit trails. **Speakeasy's linter** brings 90+ rules across SDK-readiness, correctness, best practices, security, schema validation, and Speakeasy-specific checks.

### Security Governance

Making the contract safe. **42Crunch** audits OpenAPI specifications against 300+ checks, runs automated fuzzing, calculates an API security score, and protects APIs at runtime against the OWASP API Security Top 10 — all keyed off the contract. Most spec governance engines (Spectral, vacuum, Speakeasy) also ship dedicated OWASP rulesets.

### Lifecycle Governance

Making the contract durable. **Apiwiz** delivers federated lifecycle governance across multiple gateways with build templates and policy enforcement. **Sensedia's SMART API Governance** is an AI-powered federated platform that centralizes contract validation, lifecycle policies, shadow API detection, and promotion workflows without requiring all traffic through a single gateway. **Optic** captures live traffic, diffs it against the OpenAPI contract, and turns every breaking change into a reviewable pull request. **Bump.sh** detects breaking changes at the documentation layer and pushes them into the team's notification surface. **Treblle** scores and audits production APIs in real time. **APIContext** (formerly Apimetrics) measures availability, performance, and conformance against published SLAs.

The historical **RepreZen API Studio** drove contract-first governance from a desktop IDE; the product line has been retired and `reprezen.com` is no longer maintained — its place is taken by browser-based design platforms.

## Providers and Tools Indexed

See [`apis.yml`](./apis.yml) for the full catalog. Fifteen entries, covering commercial platforms (Apiwiz, Treblle, 42Crunch, APIContext, Sensedia, Postman, Stoplight, Redocly, Speakeasy, Bump.sh), open-source engines (Spectral, Vacuum, Apicurio Registry, Optic), and one historical entry (RepreZen).

## What's In This Repo

- [`apis.yml`](./apis.yml) — apis.yml 0.19 catalog of governance providers, tools, and the local program artifacts.
- [`json-schema/governance-rule-schema.json`](./json-schema/governance-rule-schema.json) — JSON Schema for a single governance rule.
- [`json-schema/governance-policy-schema.json`](./json-schema/governance-policy-schema.json) — JSON Schema for a governance policy (bundle of rules).
- [`json-ld/governance-context.jsonld`](./json-ld/governance-context.jsonld) — JSON-LD context binding governance terms to schema.org.
- [`vocabulary/governance-vocabulary.yml`](./vocabulary/governance-vocabulary.yml) — Controlled vocabulary across objects, scope, target, lifecycle, severity, conformance, engine, enforcement, and status.
- [`examples/`](./examples/) — Sample governance policy and rule records:
  - `openapi-design-policy-example.json`
  - `security-governance-policy-example.json`
  - `lifecycle-governance-policy-example.json`
  - `asyncapi-governance-policy-example.json`
  - `spec-governance-rule-example.json`

## How This Fits The API Evangelist Network

API Evangelist already carries two long-running governance feeds: [policies](https://github.com/api-evangelist/policies) (the business reasons behind why we govern) and [rules](https://github.com/api-evangelist/rules) (the technical, machine-enforceable checks that operationalize those policies), plus the curated [spotlight-rules](https://github.com/api-evangelist/spotlight-rules) collection. This `governance` topic is the index layer above them: it catalogs the vendors and engines that publish, consume, or compete with those rules, and it captures the cross-cutting vocabulary used to describe a governance program as portable data.

## References

- [Spectral](https://stoplight.io/open-source/spectral)
- [Vacuum](https://github.com/daveshanley/vacuum)
- [Postman API Governance](https://www.postman.com/api-platform/api-governance/)
- [OWASP API Security Project](https://owasp.org/www-project-api-security/)
- [API Evangelist Policies Feed](https://developer.apievangelist.com/feeds/policies/)
- [API Evangelist Rules Feed](https://developer.apievangelist.com/feeds/rules/)

## Scope

- **Type:** Index
- **x-type:** topic

## Tags

- Governance
- Policies
- Rules
- Spectral
- Linting
- Lifecycle
- Compliance
- Standards
- OpenAPI
- AsyncAPI

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com

## Timestamps

- **Created:** 2026-05-22
- **Modified:** 2026-05-22
