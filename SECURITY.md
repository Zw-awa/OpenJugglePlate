# Security Policy

[English](./SECURITY.md) | [简体中文](./SECURITY.zh-CN.md) | [繁體中文](./SECURITY.zh-TW.md)

## Reporting A Vulnerability

Please do not open a public issue for issues that could realistically be abused as a security vulnerability.
If a report involves remote control, command injection, unauthorized access, credential exposure, unsafe update behavior, or any exploit path that others could reuse, report it privately first.

If you discover a vulnerability, report it privately through the repository owner's available contact channel and include:

- a clear summary
- affected files or subsystem
- reproduction steps if known
- possible impact
- suggested mitigation if available

## What Counts As A Security Issue Here

Examples include:

- remote or local control paths that could be abused by an attacker
- unsafe command handling across software or controller boundaries
- credential, token, or secret exposure once deployment or device provisioning exists
- insecure update, provisioning, or remote-management behavior
- vulnerabilities that could enable dangerous unintended motion through unauthorized or malicious control

## What Does Not Belong In The Private Security Process

The following are generally **not** security reports and should not be sent through the private vulnerability path:

- generic firmware bugs with no security impact
- expected prototype instability or unsafe behavior caused by unfinished tuning
- board-level hardware design limitations in third-party development boards
- soldering defects, assembly mistakes, wiring mistakes, or damaged parts
- chip defects, counterfeit parts, or vendor manufacturing issues
- failures caused by ignoring documented setup, calibration, or operating guidance
- user-side experimentation outside the documented safe envelope
- "it does not work" reports without a plausible security angle

Those issues should usually be handled as:

- a normal public bug report
- a support/question issue
- or a local hardware debugging task outside project maintenance scope

## Scope Boundaries

This repository is an open hardware prototype project, not a guarantee of correctness for every third-party board, module, solder joint, power setup, or assembly outcome.

The project security process is intended for vulnerabilities in the repository's own design, code, documented behavior, or supported workflows.
It is not intended to triage every failure in:

- third-party dev boards
- user-built hardware quality
- individual assembly quality
- unofficial modifications
- off-spec usage
- undocumented operating procedures

## Supported Scope

At this stage, the repository is in active planning and prototyping.
Support is best-effort, and response time may vary.

## Disclosure Guidance

Please allow time for review and mitigation before publishing detailed exploit steps.
Coordinated disclosure is preferred.
