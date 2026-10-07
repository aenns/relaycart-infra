# RelayCart Infrastructure: product scope

## Status

Design baseline approved. Implementation has not started; no functioning features, pipelines, releases or deployments are claimed.

## Purpose

Infrastructure as code, local container orchestration and manifests recording compatible application releases.

## Planned stack

Terraform and Docker Compose

## Engineering contract

- This repository owns its source, checks, documentation and releases.
- Public interfaces are versioned and tested.
- The development harness is optional tooling, not a runtime dependency.
- Examples and demonstration data are synthetic.
- Architecture decisions and exact local commands will be documented
  as their implementation checkpoints pass.

## Approved design baseline

- Own Terraform provider modules, documented account/secret bootstrap, Compose and a manifest of compatible commits/artifact digests.
- Package a separate Envoy gateway with CORS, token/route policy, per-instance rate limits and bypass rejection tests; confirm free-host compatibility before deployment claims.
- Implement per-service secret delivery, protected state, rotation procedures and minimum CI/deployment permissions.
- Provide optional protected telemetry aggregation and central sanitized availability observations with freshness/unknown states.
- Demonstrate portability through clean self-hosted deployment, data restore and repeated security tests; provider adapters and migration costs remain explicit.
- Free hosting is selected; the paid profile is optional. The purchased personal domain is the only currently authorized recurring project expense.

## Required engineering evidence

Each component has applicable automated checks: unit, integration, functional/contract and security tests; dependency/container/IaC scanning and secret detection where relevant. Main builds, deployments, scheduled regressions and availability observations are distinct. Build/candidate numbers increment automatically; stable semantic versions are calculated from reviewed changes and promoted through the release-readiness gate. Retain immutable artifacts, sanitized evidence and compatible rollback instructions. These are requirements, not implementation claims.

Use the portable harness during development once its core is usable; record any bypasses and feedback. The application does not import the harness at runtime.

## Design references

- [Harness release scope](https://github.com/aenns/portable-ai-harness/blob/96cc799/docs/release-scope.md)
- [Harness architecture](https://github.com/aenns/portable-ai-harness/blob/40476cf/docs/architecture.md)
- [Harness configuration and commands](https://github.com/aenns/portable-ai-harness/blob/99d47a1/docs/configuration-and-commands.md)
- [RelayCart system architecture, revision 4](https://github.com/aenns/relaycart-docs/blob/f5cf12d/docs/architecture/system.md)
