# Credits and Revisions

FramePrime deliberately separates the credit cost of **creating a new deliverable** from the cost of **refining an already delivered video**.

## Owner-approved integer Credit schedule (Production applied; general E2E validation pending)

**The same integer Credit is used for customer display and internal accounting.** At normal one-time-pack rates, 2 Credits = ¥200. A 32-minute source uses 14 Credits. The previous fractional-credit and secondary-Unit design was superseded. Production Finance24 DB was migrated to the integer Credit schedule on 2026-11-21. Production signup and checkout are enabled. A limited production check on 2026-11-22 confirmed a Stripe Live ¥3,000 one-time purchase, 30 purchased Credits and 4 referral Credits for each side. The continuous sequence of a new-price purchase → new video delivery → Credit settlement has not yet been verified.

## Current product contract

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**0 < input duration <= 2 minutes: 1 Credit; >2 to 8 minutes: 2 Credits; above 8 minutes: 2 additional Credits per started 4-minute interval.** At exactly 32 minutes: 14 Credits. **This schedule is applied to the Production financial DB. Phased customer availability and complete general-user payment-to-video-delivery E2E require separate verification; neither is guaranteed by gate activation alone.**

The generation path uses a reservation / settlement model so the system can distinguish a successful delivery from a terminal failure.

### System-terminal failure

A normal system-terminal failure releases the reservation:

**Net user credit cost: 0**

This is different from a quality-compensation case after a nominal delivery.

### Revision Render

Supported post-delivery Revision Render operations use:

**0 additional user credits**

This means a user can refine the delivered result through the supported revision workflow without paying another generation credit for each revision render.

## Credit plans and current availability

Monthly and one-time credit plans are part of the approved product contract. All amounts are tax-inclusive JPY. Credits do not expire; unused balances carry over even after subscription cancellation. The following prices are the current adopted catalog with live checkout activated; availability, eligibility, successful payment and completed new-video delivery are separately verified.

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

Credits have **no expiration** and unused balances **carry over**, including after subscription cancellation. Signup bonus = 10 Credits; qualifying referral rewards = 4 Credits for each side; referral budget = 800 Credits. These denominations are applied in the Production financial DB. Signup and checkout are enabled; the limited 2026-11-22 check confirmed the purchased Credits and both referral rewards. Individual consent and eligibility still apply. The complete new-price purchase → new video delivery → Credit settlement sequence remains unverified. The nominal consumption order is referral → subscription → signup bonus → purchased Credits; actual availability and functionality are subject to the current launch status.

**Availability note:** FramePrime v0.0.1 publicly launched on 2026-11-22 at 11:22 JST, as confirmed by the owner. The catalog and limited payment evidence above do not establish successful purchases of every plan or completion of the new-price purchase-to-video-delivery-and-settlement sequence.

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

The 30/32-minute calculations are pricing illustrations only; the financial DB has adopted this schedule, but customer-facing generation E2E after the cutover and long-form production support are not yet established.

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → 1 Credit up to 2 minutes; 2 Credits up to 8 minutes; +2 per started 4 minutes after 8 (FINANCIAL DB APPLIED; CUSTOMER END-TO-END VERIFICATION PENDING)

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
