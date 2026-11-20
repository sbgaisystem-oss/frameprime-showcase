# Credits and Revisions

FramePrime deliberately separates the credit cost of **creating a new deliverable** from the cost of **refining an already delivered video**.

## Owner-approved target credit schedule (not yet applied in Production)

**Customer-visible Credit and internal integer Unit are different:** 0.5 customer Credit = 1 internal Unit. A 32-minute source uses 7 displayed Credits = 14 internal Units under the target schedule. The currently deployed runtime still uses the legacy 1 Credit per started 2 minutes; this target schedule is **NOT live** until protected financial and UI release is verified.

## Target product contract

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**0 < input duration <= 2 minutes: 0.5 displayed Credit; >2 to 8 minutes: 1 displayed Credit; above 8 minutes: 1 additional Credit per started 4-minute interval.** At exactly 32 minutes: 7 Credits. **This target is not yet applied to Production.**

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
| Up to 2 minutes | 0.5 | ¥100 |
| 4 minutes | 1 | ¥200 |
| 8 minutes | 1 | ¥200 |
| 10 minutes | 2 | ¥400 |
| 20 minutes | 4 | ¥800 |
| 30 minutes | 7 | ¥1,400 |
| 32 minutes | 7 | ¥1,400 |

The 30/32-minute calculations are target-schedule pricing illustrations only; the live runtime has not yet adopted this schedule, nor is long-form production support established.

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → target: 0.5 Credit up to 2 minutes; 1 Credit up to 8 minutes; +1 per started 4 minutes after 8 (NOT LIVE)

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
