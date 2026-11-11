# Wireframe plan

[← Blueprint index](../README.md)

## Purpose

The first wireframe pass should test information hierarchy, player decisions, and thumb-friendly interaction. It does not need final illustration or surface polish.

Wireframes should be inserted into the relevant system documents as they are approved. Source and export files should also live under [`docs/images/`](images/README.md) using the naming convention described there.

## WF-01 — Room hub

**Purpose:** Establish the headquarters and provide clear routes into the game.

**Required elements:**

- Cash, Gold, and Reputation.
- Game Day timer.
- Watch box and capacity.
- Location/street access.
- Auctions.
- Marketplace.
- Current notifications.
- Cash grant state.

**States:** Normal, Cash grant available, inventory full, new location revealed, and marketplace notification.

## WF-02 — Location and dealer selection

**Purpose:** Show the player's markets and persistent characters.

**Required elements:**

- Location list or map.
- Reputation requirement.
- Gold opening cost.
- Permanent-open state.
- Dealer portraits and specialties.
- Stock refresh timer.

**States:** Unrevealed, Reputation-gated, qualified but unopened, opened, and return to earlier location.

## WF-03 — Dealer storefront

**Purpose:** Browse up to five rotating watches while understanding the dealer.

**Required elements:**

- Dealer portrait, name, and dialogue.
- Specialty and patience tendency.
- Watch grid or carousel.
- Asking prices.
- Refresh timer.
- Buy and sell entry points.

**States:** Fresh stock, previously viewed stock, no affordable option, fewer than five watches, and full inventory.

## WF-04 — Watch fact sheet

**Purpose:** Present the watch and known commercial facts without an inspection ritual.

**Required elements:**

- Large watch image.
- Family/model.
- Condition.
- Completeness.
- Major configuration.
- Asking price.
- Available Cash.
- Known facts.
- Inventory warning.
- Negotiate and leave actions.

**States:** Normal, insufficient Cash, full inventory, and incomplete information if later used.

## WF-05 — Buying negotiation

**Purpose:** Represent the complete Read → Rebut → Press → Decide cycle.

**Required elements:**

- Dealer claim.
- Three rebuttals.
- Known-fact references.
- Press-and-hold meter.
- Current price.
- Dealer patience.
- Buy, continue, and walk away.

**States:** Choosing rebuttal, correct response, incorrect response, pressing, improved price, low patience, final price, accepted deal, and walk-away.

## WF-06 — Sell to dealer

**Purpose:** Provide a fast, dependable exit from an owned watch.

**Required elements:**

- Selected watch.
- Acquisition cost.
- Dealer specialty fit.
- Opening Cash offer.
- Value-supporting facts.
- Selling pressure control.
- Accept and leave actions.

**States:** Specialist offer, generalist offer, improved offer, final offer, sold, and declined.

## WF-07 — Auction

**Purpose:** Keep lot quality, bid escalation, and margin readable at the same time.

**Required elements:**

- Lot image and facts.
- Entry allowance or Gold cost.
- Current bid.
- Next increment.
- Available Cash.
- Projected resale range and margin.
- NPC bidder presence.
- Bid and drop-out actions.

**States:** Preview, active bidding, leading, outbid, thin-margin warning, win, drop-out, no free entries, and insufficient Cash.

## WF-08 — Marketplace offer creation

**Purpose:** Express demand without browsing individual player listings.

**Required elements:**

- Model/family selector.
- Condition tier.
- Completeness.
- Major configuration.
- Cash offer.
- Reserved-Cash explanation.
- Active slot count.
- Post action.

**States:** Valid offer, insufficient Cash, no free slot, Gold expansion prompt, and posted offer.

## WF-09 — Active marketplace offers

**Purpose:** Show ongoing demand and the cost of reserved Cash.

**Required elements:**

- Offer criteria.
- Cash reserved per offer.
- Match/activity state.
- Duration or expiry.
- Management action under final cancellation rules.

**States:** Waiting, match found, completed, expired, cancelled, and capacity full.

## WF-10 — Seller offer notification

**Purpose:** Let an owner understand and accept a matching offer quickly.

**Required elements:**

- Targeted owned watch.
- Offered Cash.
- Acquisition cost or alternative-value context.
- First-acceptance warning.
- Accept and ignore.

**States:** New offer, multiple eligible watches, already accepted elsewhere, successful transfer, stale watch state, and expired offer.

## WF-11 — Watch box

**Purpose:** Make inventory pressure and every watch's commercial state easy to scan.

**Required elements:**

- Six starting slots.
- Watch image and identity.
- Acquisition cost.
- Estimated range.
- Condition, completeness, and configuration.
- Dealer sell action.
- Marketplace status.
- Capacity progress or expansion.

**States:** Open slot, full box, pending offer, newly acquired watch, selected watch, and capacity expansion.

## WF-12 — Progression and grants

**Purpose:** Explain permanent Reputation progress, location opening, and the separate seven-day Cash grant.

**Required elements:**

- Current Reputation.
- Next threshold.
- Revealed location.
- Gold opening cost.
- Rewarded Gold where applicable.
- Cash grant countdown and amount.
- Permanent-access confirmation.

**States:** Progressing, threshold reached, insufficient Gold, location opened, grant upcoming, grant available, and grant received.

## WF-13 — Dealer sourcing request

**Purpose:** Let the player discover temporary dealer demand, understand the potential margin, and return with a sourced watch before the opportunity expires.

**Required elements:**

- Requesting dealer.
- Requested watch model.
- Maximum Cash price.
- Two-Game-Day deadline.
- Real-time expiry.
- Current ownership or matching-watch status.
- Routes to other dealers, auctions, and the marketplace.
- Return-to-dealer action after acquisition.

**States:** No current request, new request, active request, matching watch owned, non-matching variant, fulfilled request, and expired request.

## Review checklist

Every wireframe review should ask:

- What is the single decision on this screen?
- Does the player have the facts required to make it?
- Are Cash, Gold, and Reputation visually distinct?
- Is the primary action reachable with one thumb?
- Can the player understand the consequence before committing?
- Are empty, failure, and stale-data states represented?
- Does the screen avoid unnecessary ritual?
- Does it remain readable on a small phone?

