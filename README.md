# Rigetti Computing (rigetti)

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
