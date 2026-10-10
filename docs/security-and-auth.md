# Security and Authentication Posture

This document describes FramePrime's **public security/authentication posture** at a high level.

It is not a security certification and does not publish private implementation details, secret values, internal privileged routes, or exploit-relevant recovery procedures.

## Authentication — passwordless email OTP

FramePrime currently uses **email-based passwordless authentication**.

For the PWA / Home Screen flow, the implemented path includes:

- email address entry,
- **6-digit email OTP**,
- one-time-code input support,
- resend cooldown,
- existing-user return flow.

## Why email OTP instead of a FramePrime password

The current design rationale is to **minimize the credential surface that FramePrime asks users to create and manage**.

In practical terms:

- the user does not create another FramePrime-specific password,
- sign-in proof is tied to control of the user's email inbox,
- mobile/PWA login remains low-friction,
- password-reset/recovery UX is not introduced as another FramePrime-specific credential workflow,
- the authentication provider performs the verification flow rather than FramePrime storing a custom password system.

This is a product/security tradeoff, not a claim that email OTP is universally stronger than every password/MFA design.

FramePrime does **not** present the current email-OTP flow as multi-factor authentication.

## What is remembered

For convenience, FramePrime may remember the **last login email address** on the device.

The implementation contract explicitly keeps:

- OTP **not persisted**,
- auth token **not persisted by the remembered-email feature**.

Remembered email is a usability aid, not an authentication credential.

## Access-control principles

Publicly relevant security principles include:

- owner-scoped access for user data,
- Row Level Security / authenticated-user boundaries on protected data paths,
- no customer data should become another user's learning corpus by default,
- private-learning reads remain same-user / owner scoped,
- internal privileged authority is not exposed as a normal client capability,
- secrets and credentials are excluded from this public repository.

## Secret handling

FramePrime's public documentation and Showcase intentionally exclude secret values.

Public GitHub should not contain:

- API keys,
- access / refresh tokens,
- passwords,
- private keys,
- webhook signing secrets,
- privileged backend credentials.

## Security and reliability boundaries already visible in the product design

Several technical contracts are relevant to security or integrity even when they are not traditional login features:

- fail-closed behavior when source evidence is insufficient,
- no silent conversion of missing data into measured zero,
- owner-scoped Private Learning,
- read-only / non-authoritative evaluation mirrors,
- no analysis provider receives video-authoring authority merely by being connected,
- future MCP / Agent access is required to preserve the same ownership / safety / credit rules as the GUI.

## Important current limitation — launch security audit is still open

FramePrime has implemented multiple security controls, but the **formal pre-launch authentication / authorization / information-leakage audit is still an open Launch gate**.

That audit is intended to cover areas including:

- OTP behavior,
- RLS / ownership boundaries,
- secret exposure,
- IDOR-style authorization failures,
- public/private permission boundaries,
- confirmation that no critical security defect remains before launch.

Therefore this repository should not be summarized as:

> “FramePrime security is fully audited/certified.”

A more accurate description is:

> “FramePrime has implemented passwordless auth, owner-scoped data controls, secret-handling boundaries, and fail-closed integrity patterns; its formal pre-launch security audit is still pending.”

## Vulnerability reporting

Do not disclose suspected vulnerabilities through a public Issue.

See [SECURITY.md](../SECURITY.md) for the private reporting path.
