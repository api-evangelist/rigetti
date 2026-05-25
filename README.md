# Rigetti Computing (rigetti)

Rigetti Computing (Nasdaq: RGTI) is a Berkeley, California-based quantum computing company building superconducting quantum processors and the full-stack software needed to program and operate them. Founded in 2013 by Chad Rigetti, the company designs, manufactures, and operates multi-chip superconducting QPUs at its Fab-1 in Fremont, CA and offers cloud-based access through Quantum Cloud Services (QCS). The current generation system Cepheus-1-108Q (107 qubits, deployed April 2026) is accessed via a hybrid REST + gRPC API surface, programmed using the open Quil instruction language, the pyQuil Python library, and the multi-language qcs-sdk (Rust core with Python and C bindings).

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/rigetti/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Quantum Computing, Superconducting Qubits, Quantum Cloud Services, QCS, QPU, Quil, pyQuil, NISQ, Fault-Tolerant Quantum Computing, Quantum-Classical Hybrid, Public Company

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Hardware

| QPU | Qubits | 1Q Fidelity | 2Q (CZ) Fidelity | T1 | T2 | Deployed |
|---|---|---|---|---|---|---|
| Cepheus-1-108Q | 107 | 99.84% | 98.77% | 26 us | 10 us | 2026-04-07 |
| Novera QPU (on-prem) | 9 | — | — | — | — | shipping |

## APIs

### Rigetti QCS API

The Rigetti Quantum Cloud Services HTTP API — OpenAPI-specified REST surface for accounts, groups, users, billing, reservations, endpoints, engagements, and quantum-processor discovery (including ISA and calibration calendar). Authenticated with OAuth2 / JWT bearer tokens issued by Okta; follows Google AIP design principles.

**Human URL:** [https://docs.api.qcs.rigetti.com/](https://docs.api.qcs.rigetti.com/)
**Base URL:** `https://api.qcs.rigetti.com`

- [Documentation — Reference](https://docs.api.qcs.rigetti.com/)
- [Documentation — Guide](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)
- [OpenAPI](openapi/rigetti-qcs-api-openapi.yml)
- [JSON Schema — Quantum Processor](json-schema/rigetti-quantum-processor-schema.json)
- [JSON Schema — Reservation](json-schema/rigetti-reservation-schema.json)
- [JSON-LD Context](json-ld/rigetti-context.jsonld)
- [Naftiko Capability — Quantum Processors](capabilities/qcs-quantum-processors.yaml)
- [Naftiko Capability — Reservations](capabilities/qcs-reservations.yaml)
- [Naftiko Capability — Endpoints + Engagements](capabilities/qcs-endpoints-engagements.yaml)
- [Naftiko Capability — Billing](capabilities/qcs-billing.yaml)
- SDK: [qcs-api-client-rust](https://github.com/rigetti/qcs-api-client-rust)
- SDK: [qcs-api-client-python](https://github.com/rigetti/qcs-api-client-python)

### Rigetti QCS Translation Service (gRPC)

Compiles Quil programs into encrypted Controller Jobs for execution on a QPU. Two RPCs: `TranslateQuilToEncryptedControllerJob` and `GetQuantumProcessorQuilCalibrationProgram`.

**Human URL:** [https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)

- [Protocol Buffer Definitions](https://github.com/rigetti/qcs-api-client-rust/tree/main/qcs-api-client-grpc/proto/translation)
- SDK: [qcs-sdk-rust](https://github.com/rigetti/qcs-sdk-rust)

### Rigetti QCS Controller Service (gRPC)

Executes encrypted Controller Jobs against a QPU endpoint and returns measurement results. RPCs: `ExecuteControllerJob`, `BatchExecuteControllerJobs`, `GetControllerJobResults`, `CancelControllerJobs`, `GetControllerJobStatus`.

**Human URL:** [https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api](https://docs.rigetti.com/qcs/guides/the-rigetti-qcs-api)

- [Protocol Buffer Definitions](https://github.com/rigetti/qcs-api-client-rust/tree/main/qcs-api-client-grpc/proto/controller)
- SDK: [qcs-sdk-rust](https://github.com/rigetti/qcs-sdk-rust)

## SDKs

| SDK | Language | Purpose |
|---|---|---|
| [pyquil](https://github.com/rigetti/pyquil) | Python | Quil program authoring, compilation, simulation, and QPU execution |
| [qcs-sdk-rust](https://github.com/rigetti/qcs-sdk-rust) | Rust | Core QCS SDK — translation, execution, results retrieval |
| qcs-sdk-python | Python | PyO3 bindings to qcs-sdk-rust |
| [qcs-sdk-c](https://github.com/rigetti/qcs-sdk-c) | C | C SDK for QCS |
| [qcs-api-client-rust](https://github.com/rigetti/qcs-api-client-rust) | Rust | REST + gRPC client crates |
| [qcs-api-client-python](https://github.com/rigetti/qcs-api-client-python) | Python | Generated Python client for the QCS HTTP API |
| [qcs-sdk-qir](https://github.com/rigetti/qcs-sdk-qir) | Rust | QIR (Quantum Intermediate Representation) compiler |
| [qiskit-rigetti](https://github.com/rigetti/qiskit-rigetti) | Python | Qiskit provider for Rigetti hardware |
| [pyquil-for-azure-quantum](https://github.com/rigetti/pyquil-for-azure-quantum) | Python | Azure Quantum integration |

## Tools

- [qcs-cli](https://github.com/rigetti/qcs-cli) — Quantum Cloud Services CLI
- [quilc](https://github.com/rigetti/quilc) — Quil compiler
- [qvm](https://github.com/rigetti/qvm) — Quantum Virtual Machine
- [rpcq](https://github.com/rigetti/rpcq) — RPC framework
- [Rigetti Resource Estimation](https://github.com/rigetti/rigetti-resource-estimation) (RRE)

## Examples and Tutorials

- [forest-tutorials](https://github.com/rigetti/forest-tutorials) — Binder-hosted notebooks
- [grove](https://github.com/rigetti/grove) — Quantum algorithms with pyQuil
- [forest-benchmarking](https://github.com/rigetti/forest-benchmarking) — QCVV library
- [qcs-paper](https://github.com/rigetti/qcs-paper) — QCS paper supplementary notebooks

## Integrations

- AWS Braket — Rigetti as third-party Braket device
- Microsoft Azure Quantum — Rigetti as a Quantum provider
- Google Cirq — Rigetti hardware module
- Qiskit — via `qiskit-rigetti`
- OpenFermion — via `forest-openfermion`
- QIR Alliance — via `qcs-sdk-qir`

## Solutions

- **Quantum Cloud Services (QCS)** — managed cloud access to Rigetti QPUs
- **Novera QPU** — 9-qubit on-premises superconducting system
- **Quantum Foundry Services** — custom QPU development and partner program

## Commercial / FinOps Artifacts

- [Plans / Pricing](plans/rigetti-plans-pricing.yml)
- [Rate Limits](rate-limits/rigetti-rate-limits.yml)
- [FinOps (FOCUS-aligned)](finops/rigetti-finops.yml)
- [Vocabulary](vocabulary/rigetti-vocabulary.yml)

## Authentication

All access to the QCS HTTP API requires OAuth2 authentication via Okta. Users request access through https://www.rigetti.com/get-quantum; once approved, an access token can be downloaded from https://qcs.rigetti.com/auth/token. Tokens are valid for 24 hours after issuance. The same JWT bearer is used for the gRPC services, though execution against a QPU additionally requires an Engagement (short-lived credential scoped to a specific endpoint) created via `POST /v1/engagements`.

## QPU Access Workflow

1. Authenticate against QCS (Okta OAuth2) and obtain a 24-hour JWT.
2. Discover available QPUs via `GET /v1/quantumProcessors`.
3. Inspect the target QPU's ISA via `GET /v1/quantumProcessors/{id}/instructionSetArchitecture`.
4. Find an open reservation slot via `GET /v1/reservations:findAvailable`, then `POST /v1/reservations` to book.
5. At the reserved time, `POST /v1/engagements` to obtain a Controller-service access token.
6. Compile your Quil program (locally with quilc or via the gRPC Translation service) into a Controller Job.
7. Submit the job via the gRPC Controller `ExecuteControllerJob` and retrieve results with `GetControllerJobResults`.

## Sources

- https://www.rigetti.com/
- https://docs.rigetti.com/qcs/
- https://docs.api.qcs.rigetti.com/
- https://github.com/rigetti
