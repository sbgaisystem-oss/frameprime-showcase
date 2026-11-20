# Credits and Revisions

FramePrime deliberately separates the credit cost of **creating a new deliverable** from the cost of **refining an already delivered video**.

## Current public product contract

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**1 user Credit for each started 2 minutes of the final video duration (rounded up)**

The generation path uses a reservation / settlement model so the system can distinguish a successful delivery from a terminal failure.

### System-terminal failure

A normal system-terminal failure releases the reservation:

**Net user credit cost: 0**

This is different from a quality-compensation case after a nominal delivery.

### Revision Render

Supported post-delivery Revision Render operations use:

**0 additional user credits**

This means a user can refine the delivered result through the supported revision workflow without paying another generation credit for each revision render.

## Credit plans and pre-launch availability

Monthly and one-time credit plans are part of the product contract. Credits have no expiration and can carry over. Specific pricing and general checkout availability must match the current production offering; PRE-BETA documentation does not claim that public checkout has launched.

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → ceil(final video duration in minutes / 2) Credits when successfully delivered

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
