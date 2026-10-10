# Credits and Revisions

FramePrime deliberately separates the credit cost of **creating a new deliverable** from the cost of **refining an already delivered video**.

## Current public product contract

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**1 user credit**

The generation path uses a reservation / settlement model so the system can distinguish a successful delivery from a terminal failure.

### System-terminal failure

A normal system-terminal failure releases the reservation:

**Net user credit cost: 0**

This is different from a quality-compensation case after a nominal delivery.

### Revision Render

Supported post-delivery Revision Render operations use:

**0 additional user credits**

This means a user can refine the delivered result through the supported revision workflow without paying another generation credit for each revision render.

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → 1 credit when successfully delivered

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
