# MVP scope

[← Blueprint index](../README.md)

## Product goal

The MVP must prove that watch dealing is a satisfying repeatable strategy loop on mobile.

It does not need to simulate the entire watch industry. It needs to make finding, judging, negotiating, owning, and selling a watch feel connected and consequential.

## Included systems

### Player foundation

- Rookie dealer starting in a New York City bedroom.
- Cash, Gold, and permanent Reputation.
- Six-slot starting watch box.
- Location progression and return travel.
- One Game Day every three real hours.
- Cash grant every seven real days.

### Street dealing

- Persistent named dealers.
- Up to five rotating watches per dealer.
- Watch fact sheet without compulsory inspection gestures.
- Buying negotiation.
- Selling negotiation.
- Two-Game-Day dealer sourcing requests that can be fulfilled through other dealers, auctions, or the marketplace.
- Dealer specialties and patience.

### Negotiation

- Read → Rebut → Press → Decide cycle.
- Three text responses with one factually strong rebuttal.
- Press-and-hold pressure control.
- Visible dealer patience.
- Final price at the end of patience.
- Accept and walk-away choices at every appropriate stage.

### Auctions

- NPC competition.
- Two free entries per Game Day.
- Additional entries purchased with Gold.
- Bid escalation and drop-out decision.
- Projected margin feedback.

### Player marketplace

- Automatic discoverability of owned watches.
- Model/family-specific buyer offers.
- Condition, completeness, and major-configuration criteria.
- Matching-owner notifications.
- First valid acceptance wins.
- Reserved Cash.
- Three starting active offer slots.
- Gold-based capacity expansion.

### Content

- Approximately six to ten watch families.
- Meaningful condition, completeness, and configuration variation.
- Dealer character profiles and modular dialogue.
- Initial location art, room hub, and watch presentation.

## Explicit non-goals

The following are intentionally outside this design pass:

- Detailed onboarding sequence.
- Reputation loss or career regression.
- Energy, stamina, or daily action limits.
- A comprehensive real-world watch catalog.
- Direct Gold purchase of watches.
- Gold-to-Cash conversion.
- Multi-step manual inspection rituals.
- Complex live operations.
- Guilds or clans.
- Social chat.
- Competitive leaderboards.
- Deep relationship simulation beyond dealer identity and behavior.
- Player-authored watch listings.
- Real-time player-versus-player auction rooms.

Excluding these features protects the core test and limits production risk.

## Minimum playable loop

A first integrated build should allow the player to:

1. Enter the New York room hub.
2. Visit a dealer.
3. Compare several watches.
4. Review one watch's known facts.
5. Negotiate using at least two rounds and dealer patience.
6. Buy the watch with Cash.
7. See it occupy an inventory slot.
8. Sell it to a dealer through the mirrored negotiation.
9. Receive Cash and Reputation.
10. Repeat with changed stock.

Auctions and marketplace activity can follow after this vertical slice proves the core transaction.

## Validation goals

The MVP should answer:

- Do players understand why a deal is good or bad?
- Are watch facts useful rather than decorative?
- Does negotiation stay engaging across repeated watches?
- Do players sometimes walk away voluntarily?
- Does limited inventory create healthy pressure?
- Is dealer selling a satisfying liquidity option?
- Do dealer sourcing requests encourage players to compare acquisition channels and plan an exit before buying?
- Do auctions create excitement without disguising the margin decision?
- Does the offer-driven marketplace create useful connections?
- Are Cash, Gold, and Reputation understood as separate systems?
- Does Gold feel like opportunity rather than pay-to-win power?

## Product risks

### Content repetition

The negotiation structure could become predictable if claims and rebuttals repeat too quickly. Modular writing, varied facts, and dealer personality need to provide sufficient texture.

### Economy lock-up

A player may tie up Cash in watches or offers. Dealer liquidity and the seven-day grant reduce the chance of permanent stagnation, but early balance must be forgiving enough to learn.

### Marketplace manipulation

Peer pricing creates abuse and inflation risks. Server authority, bounds, reservation, and monitoring are mandatory before broad release.

### Monetization perception

Gold touches locations, entries, and capacity. The free allowance must remain genuinely usable, and the watch itself must remain a Cash decision.

### Scope expansion

Real watch dealing contains authentication, service, financing, consignment, relationships, and many other possibilities. The MVP should not absorb every authentic detail before proving its central loop.

## Definition of ready for wireframing

A system is ready for a first wireframe when:

- Its confirmed rules are identified.
- Its main player flow is complete.
- Required information is listed.
- Important empty, error, and completion states are named.
- Unresolved tuning does not change the fundamental layout.

The [wireframe plan](10-wireframe-plan.md) applies this test to thirteen core views.

