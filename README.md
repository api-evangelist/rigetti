# Rigetti Computing (rigetti)

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

Rigetti Computing (Nasdaq, RGTI) is a Berkeley, California-based quantum computing company building superconducting quantum processors and the full-stack software needed to program and operate them. Founded in 2013 by Chad Rigetti, the company designs, manufactures, and operates multi-chip superconducting QPUs at its Fab-1 in Fremont, CA and offers cloud-based access through Quantum Cloud Services (QCS). Rigetti also sells the Novera QPU (9-qubit) for on-premises customers and provides Quantum Foundry Services for custom development. The current generation system Cepheus-1-108Q (107 qubits, deployed April 2026) is accessed via a hybrid REST + gRPC API surface, programmed using the open Quil instruction language, the pyQuil Python library, and the multi-language qcs-sdk (Rust core with Python bindings). Rigetti's hardware is also available indirectly through AWS Braket, Microsoft Azure Quantum, and as a Qiskit provider via qiskit-rigetti.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/rigetti/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/rigetti/refs/heads/main/apis.yml)

## Scope

- **Access:** 3rd-Party

## Tags

- Quantum Computing
- Superconducting Qubits
- Quantum Cloud Services
- QCS
- QPU
- Quil
- pyQuil
- NISQ
- Fault-Tolerant Quantum Computing
- Quantum-Classical Hybrid
- Public Company

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Rigetti QCS API

The Rigetti Quantum Cloud Services (QCS) HTTP API is the OpenAPI-specified REST surface for managing accounts, groups, users, billing, reservations, endpoints, engagements, and discovering quantum processor metadata including Instruction Set Architecture (ISA) and calibration. Authentication is OAuth2 (JWT bearer) issued via Okta. The API follows Google API Improvement Proposals (AIP) and is paired with a gRPC API for quantum program translation and controller execution against the QPU.

- **Human URL:** [https://docs.api.qcs.rigetti.com/](https://docs.api.qcs.rigetti.com/)
- **Base URL:** `https://api.qcs.rigetti.com`

#### Tags

- Quantum Computing
- Quantum Cloud Services
- QCS
- Account Management
- QPU Access
- Reservations
- Billing

#### Properties

- [Documentation](https://docs.api.qcs.rigetti.com/)
- [Documentation](https://docs.rigetti.com/qcs/references/qcs-api)
- [Documentation](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)
- [OpenAPI](openapi/rigetti-qcs-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rigetti-qcs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rigetti-qcs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/rigetti-quantum-processor-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/rigetti-reservation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/rigetti-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [SDK](https://github.com/rigetti/qcs-api-client-rust)
- [SDK](https://github.com/rigetti/qcs-api-client-python)

### Rigetti QCS Translation Service (gRPC)

gRPC Translation service that compiles native Quil programs into encrypted Controller Jobs for execution on a Rigetti QPU. Operations include TranslateQuilToEncryptedControllerJob and GetQuantumProcessorQuilCalibrationProgram. Authenticated with the same JWT bearer token used by the QCS HTTP API and consumed via qcs-sdk-rust/qcs-sdk-python or the Rust qcs-api-client-grpc crate.

- **Human URL:** [https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)

#### Tags

- Quantum Computing
- QCS
- Translation
- Compilation
- Quil
- gRPC

#### Properties

- [Documentation](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)
- [Protocol Buffers](https://github.com/rigetti/qcs-api-client-rust/tree/main/qcs-api-client-grpc/proto/translation)
- [SDK](https://github.com/rigetti/qcs-api-client-rust)
- [Postman Collection](collections/rigetti-qcs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rigetti-qcs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Rigetti QCS Controller Service (gRPC)

gRPC Controller service that executes encrypted Controller Jobs on a Rigetti QPU endpoint and returns measurement (readout) results. Operations include ExecuteControllerJob, BatchExecuteControllerJobs, GetControllerJobResults, CancelControllerJobs, and GetControllerJobStatus. Used through qcs-sdk-rust / qcs-sdk-python after obtaining a CreateEngagement token from the QCS HTTP API.

- **Human URL:** [https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)

#### Tags

- Quantum Computing
- QCS
- Execution
- Controller
- Jobs
- gRPC

#### Properties

- [Documentation](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)
- [Protocol Buffers](https://github.com/rigetti/qcs-api-client-rust/tree/main/qcs-api-client-grpc/proto/controller)
- [SDK](https://github.com/rigetti/qcs-api-client-rust)
- [Postman Collection](collections/rigetti-qcs-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rigetti-qcs-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://www.rigetti.com)
- [Sign Up](https://qcs.rigetti.com/)
- [Documentation](https://docs.rigetti.com/qcs)
- [Getting Started](https://docs.rigetti.com/qcs/getting-started/installation-and-setup)
- [Documentation](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)
- [Documentation](https://docs.api.qcs.rigetti.com/)
- [Authentication](https://qcs.rigetti.com/auth/token)
- [Pricing](https://www.rigetti.com/qcs)
- [Pricing](https://www.rigetti.com/novera)
- [Pricing](https://www.rigetti.com/foundry)
- [Support](mailto:support@rigetti.com)
- [Support](https://rigetti.zendesk.com)
- [Status Page](https://docs.rigetti.com/qcs/troubleshooting)
- [Blog](https://www.rigetti.com/blog)
- [Press](https://investors.rigetti.com/news-events/news-releases)
- [GitHub Organization](https://github.com/rigetti)
- [SDK](https://github.com/rigetti/pyquil)
- [SDK](https://github.com/rigetti/qcs-sdk-rust)
- [SDK](https://github.com/rigetti/qcs-sdk-rust/tree/main/crates/python)
- [SDK](https://github.com/rigetti/qcs-sdk-c)
- [SDK](https://github.com/rigetti/qcs-api-client-rust)
- [SDK](https://github.com/rigetti/qcs-api-client-python)
- [SDK](https://github.com/rigetti/quil-rs)
- [SDK](https://github.com/rigetti/qiskit-rigetti)
- [SDK](https://github.com/rigetti/pyquil-for-azure-quantum)
- [SDK](https://github.com/rigetti/qcs-sdk-qir)
- [Tool](https://github.com/rigetti/qcs-cli)
- [Tool](https://github.com/rigetti/quilc)
- [Tool](https://github.com/rigetti/qvm)
- [Tool](https://github.com/rigetti/rpcq)
- [Tool](https://github.com/rigetti/rigetti-resource-estimation)
- [Code Examples](https://github.com/rigetti/forest-tutorials)
- [Code Examples](https://github.com/rigetti/grove)
- [Code Examples](https://github.com/rigetti/forest-benchmarking)
- [Code Examples](https://github.com/rigetti/qcs-paper)
- [Integrations](https://aws.amazon.com/braket/)
- [Integrations](https://azure.microsoft.com/en-us/products/quantum)
- [Integrations](https://quantumai.google/cirq/hardware/rigetti)
- [Protocol Buffers](https://github.com/rigetti/qcs-api-client-rust/tree/main/qcs-api-client-grpc/proto)
- [Specification](https://github.com/quil-lang/quil)
- [Documentation](https://pyquil.readthedocs.io)
- [Documentation](https://docs.rs/qcs)
- [Privacy Policy](https://www.rigetti.com/privacy-policy)
- [Terms of Service](https://www.rigetti.com/terms-of-service)
- [Plans](plans/rigetti-plans-pricing.yml)
- [Rate Limits](rate-limits/rigetti-rate-limits.yml)
- [Fin Ops](finops/rigetti-finops.yml)
- [Vocabulary](vocabulary/rigetti-vocabulary.yml)
- [JSON-LD](json-ld/rigetti-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)
