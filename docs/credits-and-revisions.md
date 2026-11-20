# Credits and Revisions

FramePrime deliberately separates the credit cost of **creating a new deliverable** from the cost of **refining an already delivered video**.

## Current public product contract

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**1 user Credit per started 2 minutes of input source video duration (rounded up)**

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

Monthly and one-time credit plans are part of the approved product contract. All amounts are tax-inclusive JPY. Credits do not expire; unused balances carry over even after subscription cancellation. The prices below describe the adopted pricing contract, not proof of generally enabled checkout in PRE-BETA.

### Monthly subscriptions (tax included)

| Monthly price | Credits granted monthly | Effective price per Credit* |
| --- | ---: | ---: |
| ¥2,900 | 16 | approx. ¥181.25 |
| ¥5,800 | 34 | approx. ¥170.59 |
| ¥9,800 | 61 | approx. ¥160.66 |
| ¥19,800 | 141 | approx. ¥140.43 |

*Effective unit price assumes all granted Credits are used. No separate per-video cash charge on top of the Credits consumed.

### One-time Credit packs (tax included)

| One-time price | Credits granted |
| --- | ---: |
| ¥1,000 | 5 |
| ¥3,000 | 15 |
| ¥6,000 | 30 |
| ¥10,000 | 50 |

One-time packs do not auto-renew. Separately, the **¥980 beta trial pack grants 10 Credits, one purchase per account, without automatic renewal**. Existing legacy ¥980/month Founder subscriptions are distinct and are not silently converted.

Credits have **no expiration** and unused balances **carry over**, including after subscription cancellation. The nominal consumption order is referral → subscription → signup bonus → purchased Credits; actual availability and functionality are subject to the current launch status.

**Pre-launch status:** The listed products describe the Owner-approved pricing contract, not proof that general checkout is currently enabled.

## Illustrative consumption by input video length

| Input video length | Credits | One-time-pack equivalent (¥200/Credit) |
| --- | ---: | ---: |
| Up to 2 minutes | 1 | ¥200 |
| 4 minutes | 2 | ¥400 |
| 10 minutes | 5 | ¥1,000 |
| 20 minutes | 10 | ¥2,000 |
| 30 minutes | 15 | ¥3,000 |

The 30-minute calculation is illustrative pricing mathematics; it does not establish that the current production runtime supports 30-minute processing.

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → ceil(input source video duration in minutes / 2) Credits when successfully delivered

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
