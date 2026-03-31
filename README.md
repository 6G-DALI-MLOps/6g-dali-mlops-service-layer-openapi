# 6G-DALI MLOps Service Layer — OpenAPI Specification

This repository contains the OpenAPI 3.1 specification of the **6G-DALI MLOps Service Management Layer**, developed by Nextworks within the [6G-DALI](https://6g-dali.eu) project (Grant Agreement No. 101192750, funded by the European Union under the Horizon Europe programme).

The specification documents the northbound AIaaS REST API exposed by the MLOps Service Layer backend, grounding each endpoint and schema in the **3GPP TS 28.105** information model where applicable and covering all DALI-specific extensions.

---

## Repository Structure

| File | Description |
|------|-------------|
| `openapi.json` | Full OpenAPI 3.1 specification auto-generated from the running service |

---

## API Domains

The specification covers six operational domains:

| Tag | Description |
|-----|-------------|
| `Authentication` | Token-based authentication — login, token refresh, logout, current user profile |
| `Administration` | Platform-level user, project, membership and access-policy management |
| `Testbed` | Testbed registration, hardware capabilities and ML tools stack management |
| `Model Catalogue` | MLModel registration, discovery, lineage tracking and S3 artefact storage |
| `Training` | MLTrainingFunction — MLTrainingRequest / MLTrainingProcess / MLTrainingReport lifecycle |
| `Deployment` | MLDeploymentFunction — MLDeploymentRequest / MLDeploymentProcess / MLDeploymentReport lifecycle and live inference endpoints |

---

## Exploring the Specification

The `openapi.json` file can be imported into any OpenAPI-compatible tool:

- **[editor.swagger.io](https://editor.swagger.io)** — paste or import the file for interactive rendering and validation
- **[Swagger UI](https://swagger.io/tools/swagger-ui/)** — serve locally for a full try-it-out interface
- **[Postman](https://www.postman.com)** — import directly as a collection

When running the service locally, the live specification and interactive UI are available at:
```
GET /api/openapi.json   ← raw specification
GET /api/docs           ← Swagger UI
GET /api/redoc          ← ReDoc
```

---

## Context

This specification is part of the initial implementation results of the **MLOps Service Management Layer** described in Deliverable D3.1 of the 6G-DALI project. The Service Layer provides a unified, tool-agnostic management interface for the full ML lifecycle — covering training, validation, deployment, monitoring, hyperparameter optimisation, federated learning, transfer learning, and trustworthiness assessment — exposed as AIaaS REST APIs to experimenters and administrators across the 6G-DALI testbed federation.

---

## Authors
Nextworks S.r.l.
