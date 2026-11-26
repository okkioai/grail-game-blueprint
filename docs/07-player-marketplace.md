# Player marketplace

[← Blueprint index](../README.md)

## Marketplace model

The peer-to-peer marketplace is **offer driven**.

Player-owned watches are automatically discoverable. Owners do not have to create individual listings before a buyer can select a watch in Browse.

A buyer selects a specific watch instance in Browse and sends a Cash offer to its owner.

## Why offers come first

Traditional listings require every seller to price and publish every watch. GRAIL instead treats ownership as latent supply and lets demand activate it.

This supports the dealer fantasy:

- Buyers can hunt for a specific watch.
- Owners can receive unexpected opportunities.
- Every watch remains potentially liquid without constant listing management.
- The market feels connected even with a focused launch catalog.

## Offer target

Each offer identifies one selected watch instance and a Cash amount. The selected listing shows the model, condition, completeness, and configuration.

## Buyer flow

1. Open **Browse** in the Marketplace and select a watch.
2. Open the selected watch’s details and choose **Make an offer** to open that listing’s dedicated offer screen.
3. Review the model or family, condition, completeness, and configuration taken from that watch.
4. Enter the Cash offer.
5. Review the number of active offer slots and the reserved-Cash rule.
6. Post the offer.
7. Cash becomes reserved while the offer remains active.
8. Wait for the selected watch’s owner to accept, or manage the offer under the final cancellation rules.

The Offers tab manages existing offers. A buyer must select a watch before making an offer. Only the selected watch can fulfill the offer.

## Seller flow

1. The selected watch’s owner receives a notification with the watch and Cash amount.
2. The owner reviews and accepts or ignores the offer.
3. The first valid transaction for the watch wins. The watch transfers immediately, and the seller’s proceeds follow bank clearance rules.
4. Any other active offers for that watch close and their reserved Cash is released.

## Automatic discoverability

### Confirmed rule

Every player-owned watch is discoverable by default.

Automatic discoverability does not necessarily mean that every owner is publicly identified or that every watch appears in a browseable global feed. The system can match privately and reveal only the information needed for the offer.

Privacy, player identity, and whether an owner can temporarily exclude a watch remain implementation questions.

## Cash reservation

When an offer is posted, its full Cash value is reserved. That commitment reduces Available Cash and cannot be used to buy another watch or fund another offer.

Reservation prevents a buyer from posting more commitments than they can honor. Reserved Cash reduces other buying power while the offer is active.

The global interface shows only Cash and Available Cash. Cash remains the total; Available Cash falls when an offer reserves funds. Each active offer shows its own committed amount so the player can understand the difference without introducing a third balance.

## Offer capacity

### Confirmed rule

The player begins with **three free active offer slots**. Gold permanently unlocks more capacity.

Gold purchases the ability to pursue more opportunities in parallel. It does not improve an offer's Cash value or priority.

The number of slots added by each Gold purchase and the capacity ceiling remain tuning decisions.

## Matching rules

Acceptance must transfer the exact watch instance identified by the offer.

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
- Can another buyer acquire this watch first?
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
- Conflict handling when two transactions target the same watch.

The server must be authoritative for acceptance and transfer. The first valid transaction wins.

A completed watch sale uses the same two-beat **Watch Sold** result as a dealer sale: **Deal sealed!** with exact Cash proceeds and yellow confetti, followed by the animated Reputation result. It appears only after authoritative acceptance and returns the player to Marketplace Offers when complete.

## Relationship to dealer selling

The two exits should have different strengths:

| Dealer sale | Marketplace sale |
|---|---|
| Immediate and dependable offer | Potentially stronger price |
| Every dealer buys every watch | Requires a matching active buyer |
| Specialty changes the offer | The selected watch instance determines eligibility |
| Known exit before the sale | May require waiting for a matching buyer |

This gives the owner a real decision between speed and expected return.

## Gold boundary

Gold permanently unlocks more active offer slots. Gold never:

- Replaces the Cash offer.
- Forces an owner to accept.
- Improves matching priority.
- Purchases the watch directly.
- Converts into reserved Cash.

## Wireframe implications

The marketplace needs at least three core views:

1. **Offer creation from a selected watch:** watch details, Cash amount, and capacity.
2. **Active offers:** reserved Cash, match status, and management actions.
3. **Seller notification:** targeted watch, offer value, and accept/ignore decision.

Empty, full-capacity, insufficient-Available-Cash, expired, and already-accepted states must be designed deliberately.

## Open tuning

- Offer duration and cancellation timing.
- Whether buyers can edit an offer.
- Whether owners can hide a watch.
- Number of permanent slots added per Gold purchase and the maximum capacity.
- Gold cost for capacity.
- Price bounds and abuse controls.
- Fees, if any.
- How market activity contributes Reputation.

