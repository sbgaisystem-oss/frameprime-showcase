# Credits and Revisions

FramePrime deliberately separates the credit cost of **creating a new deliverable** from the cost of **refining an already delivered video**.

## Owner-approved integer Credit schedule (not yet applied in Production)

**The same integer Credit is used for customer display and internal accounting.** At normal one-time-pack rates, 2 Credits = ¥200. A 32-minute source uses 14 Credits. The previous fractional-credit and secondary-Unit design was superseded. Current Production still uses the legacy 1 Credit per started 2 minutes; the integer schedule is **NOT live** until protected financial, balances and UI release are verified.

## Target product contract

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**0 < input duration <= 2 minutes: 1 Credit; >2 to 8 minutes: 2 Credits; above 8 minutes: 2 additional Credits per started 4-minute interval.** At exactly 32 minutes: 14 Credits. **This target is not yet applied to Production.**

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
| ¥2,900 | 32 | approx. ¥90.63 |
| ¥5,800 | 68 | approx. ¥85.29 |
| ¥9,800 | 122 | approx. ¥80.33 |
| ¥19,800 | 282 | approx. ¥70.21 |

*Effective unit price assumes all granted Credits are used. No separate per-video cash charge on top of the Credits consumed.

### One-time Credit packs (tax included)

| One-time price | Credits granted |
| --- | ---: |
| ¥1,000 | 10 |
| ¥3,000 | 30 |
| ¥6,000 | 60 |
| ¥10,000 | 100 |

One-time packs do not auto-renew. Separately, the **¥980 beta trial pack grants 20 Credits, one purchase per account, without automatic renewal**. Existing legacy ¥980/month Founder subscriptions are distinct and are not silently converted.

Credits have **no expiration** and unused balances **carry over**, including after subscription cancellation. Signup bonus = 10 Credits; qualifying referral rewards = 4 Credits for each side; referral budget = 800 Credits. These new denominations are not yet live in Production. The nominal consumption order is referral → subscription → signup bonus → purchased Credits; actual availability and functionality are subject to the current launch status.

**Pre-launch status:** The listed products describe the Owner-approved pricing contract, not proof that general checkout is currently enabled.

## Illustrative consumption by input video length

| Input video length | Credits | One-time-pack equivalent (¥100/Credit) |
| --- | ---: | ---: |
| Up to 2 minutes | 1 | ¥100 |
| 4 minutes | 2 | ¥200 |
| 8 minutes | 2 | ¥200 |
| 10 minutes | 4 | ¥400 |
| 20 minutes | 8 | ¥800 |
| 30 minutes | 14 | ¥1,400 |
| 32 minutes | 14 | ¥1,400 |

The 30/32-minute calculations are target-schedule pricing illustrations only; the live runtime has not yet adopted this schedule, nor is long-form production support established.

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → target: 1 Credit up to 2 minutes; 2 Credits up to 8 minutes; +2 per started 4 minutes after 8 (NOT LIVE)

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
