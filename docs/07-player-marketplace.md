# Player marketplace

[← Blueprint index](../README.md)

## Marketplace model

The peer-to-peer marketplace is **offer driven**.

All watches owned by players are automatically discoverable by the matching system. Owners do not have to create individual listings before another player can express interest.

A buyer describes the watch they want and commits a Cash offer. Every matching owner receives the opportunity to accept.

## Why offers come first

Traditional listings require every seller to price and publish every watch. GRAIL instead treats ownership as latent supply and lets demand activate it.

This supports the dealer fantasy:

- Buyers can hunt for a specific watch.
- Owners can receive unexpected opportunities.
- Every watch remains potentially liquid without constant listing management.
- The market feels connected even with a focused launch catalog.

## Offer criteria

A buyer offer targets:

- Watch model or family.
- Condition tier.
- Completeness requirement.
- One major configuration.
- Cash amount.

For example, a buyer may seek a Datejust with a particular condition tier, box and papers, and a selected dial category. Owners of matching Datejusts receive the offer.

The criteria should be broad enough to produce matches while still allowing meaningful preference.

## Buyer flow

1. Open the marketplace and choose **Create offer**.
2. Select a model or watch family.
3. Set condition, completeness, and one major configuration.
4. Enter the Cash offer.
5. Review the number of active offer slots and the reserved-Cash rule.
6. Post the offer.
7. Cash becomes reserved while the offer remains active.
8. Wait for a matching owner to accept, or manage the offer under the final cancellation rules.

## Seller flow

1. The matching service identifies owned watches that satisfy a buyer's criteria.
2. Matching owners receive a notification.
3. The notification identifies the targeted watch and Cash amount.
4. The owner reviews and accepts or ignores the offer.
5. The first valid acceptance wins.
6. The watch and reserved Cash transfer immediately.
7. Other matching notifications become unavailable.

The acceptance screen should clearly state that another owner may accept first.

## Automatic discoverability

### Confirmed rule

Every player-owned watch is discoverable by default.

Automatic discoverability does not necessarily mean that every owner is publicly identified or that every watch appears in a browseable global feed. The system can match privately and reveal only the information needed for the offer.

Privacy, player identity, and whether an owner can temporarily exclude a watch remain implementation questions.

## Cash reservation

When an offer is posted, its full Cash value is reserved. Reserved Cash cannot be used to buy another watch or fund another offer.

Reservation prevents a buyer from posting more commitments than they can honor. It also creates a strategic cost: a broad offer may find a watch, but the locked Cash reduces other buying power.

The interface must distinguish:

- Total Cash.
- Available Cash.
- Cash reserved in active offers.

## Offer capacity

### Confirmed rule

The player begins with **three free active offer slots**. Gold can unlock more capacity.

Gold purchases the ability to pursue more opportunities in parallel. It does not improve an offer's Cash value or priority.

Capacity may be a permanent account upgrade or another form of expansion; the exact product treatment still needs confirmation.

## Matching rules

A valid match requires every selected criterion to be satisfied when the acceptance occurs.

The system should revalidate:

- The seller still owns the watch.
- The watch has not been sold to a dealer.
- The watch state still matches the criteria.
- The buyer's Cash remains reserved.
- The offer is still active.
- The accepting owner is the first valid acceptance.

This prevents double sales and stale notifications.

## Notification design

The owner notification needs to answer:

- Which of my watches is wanted?
- How much Cash is being offered?
- How does that compare with my acquisition cost or current alternatives?
- Is there an expiry?
- Can another owner accept first?
- What happens immediately if I accept?

It should be possible to make the decision quickly without navigating through several unrelated screens.

## Marketplace safeguards

The MVP specification still needs rules for:

- Offer duration.
- Buyer cancellation.
- Cash release timing.
- Minimum and maximum price bounds.
- Repeated offer spam.
- Self-dealing and coordinated manipulation.
- Multi-account abuse.
- Notification expiration.
- Watch-state changes after matching.
- Conflict handling when two owners accept nearly simultaneously.

The server must be authoritative for acceptance and transfer. The first valid acceptance—not the first animation shown on a device—wins.

## Relationship to dealer selling

The two exits should have different strengths:

| Dealer sale | Marketplace sale |
|---|---|
| Immediate and dependable | Potentially stronger price |
| Every dealer buys every watch | Requires a matching active buyer |
| Specialty changes the offer | Exact criteria determine eligibility |
| Fast liquidity | May require waiting |

This gives the owner a real decision between speed and expected return.

## Gold boundary

Gold may unlock more active offer slots. Gold never:

- Replaces the Cash offer.
- Forces an owner to accept.
- Improves matching priority.
- Purchases the watch directly.
- Converts into reserved Cash.

## Wireframe implications

The marketplace needs at least three core views:

1. **Offer creation:** target criteria, Cash amount, and capacity.
2. **Active offers:** reserved Cash, match status, and management actions.
3. **Seller notification:** targeted watch, offer value, and accept/ignore decision.

Empty, full-capacity, insufficient-Cash, expired, and already-accepted states must be designed deliberately.

## Open tuning

- Offer duration and cancellation timing.
- Whether buyers can edit an offer.
- Whether owners can hide a watch.
- Permanent versus temporary offer-slot expansion.
- Gold cost for capacity.
- Price bounds and abuse controls.
- Fees, if any.
- How market activity contributes Reputation.

