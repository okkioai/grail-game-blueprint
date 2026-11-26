# Wireframe plan

[← Blueprint index](../README.md)

## Purpose

The first wireframe pass should test information hierarchy, player decisions, and thumb-friendly interaction. It does not need final illustration or surface polish.

Wireframes should be inserted into the relevant system documents as they are approved. Source and export files should also live under [`docs/images/`](images/README.md) using the naming convention described there.

## Approved visual-design rollout

The implementation may advance approved Figma-designed routes beyond wireframe fidelity without implying that unresolved rules or tuning have been decided.

- Finished Figma screens establish the shared dark exchange aesthetic, typography, spacing, surfaces, yellow action accent, watch presentation, dealer presentation, and floating five-item navigation.
- Routes without a finished design adopt the shared shell and tokens while retaining their functional wireframe layouts and clearly labeled placeholder art.
- Current blueprint behavior takes precedence when a design mockup shows older copy, navigation, currency, or transaction behavior.
- Exact approved project assets should be exported from Figma. Missing watch/location art may use the closest approved watch/location image temporarily; missing character art remains a labeled styled placeholder and must not reuse another character.
- The activity feed lives inside **Your room**. The persistent dock labels are Room, Watch Box, Market, Streets, and Career. Store remains reachable from Your room and every insufficient-Gold flow.
- A completed dealer purchase goes directly to a visible **Deal sealed / It’s yours** result with the settled price, savings, remaining Cash, and watch-box occupancy.
- The rollout does not add a fake operating-system status bar and does not change economy, negotiation, progression, auction, or marketplace rules.

## WF-01 — Your room and activity feed

**Purpose:** Give the player a personal New York home screen with collection and Store entry points plus one chronological view of recent game events.

**Required elements:**

- Cash, Available Cash, Gold, and the game clock in the persistent top bar.
- Every current event in reverse chronological order as a large activity card.
- Feed cards have no read/unread status or inbox-management actions.
- Event time without exposing real-world clock time.
- Persistent bottom navigation to Room, Watch Box, Market, Streets, and Career.
- Gold-store entry from the Gold balance.
- Collection summary and Watch Box entry.
- Store entry from the room.

**States:** Empty feed, dense history, new location revealed, and marketplace notification.

## WF-02 — Location and dealer selection

**Purpose:** Show the player's markets and persistent characters.

**Required elements:**

- Location list or map.
- Reputation requirement.
- Permanent-open state.
- Dealer portraits and specialties.
- Stock refresh timer.

**States:** Visible with no progress, partially progressed, required mission completed, opened, and return to earlier location.

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
- Cash, Available Cash, and bank-clearance result after the sale.

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

**Purpose:** Make a Cash offer from a watch selected in Marketplace Browse.

**Required elements:**

- Selected watch’s model or family, condition, completeness, and major configuration.
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
- Bank-clearance result after a successful transfer.

**States:** New offer, multiple eligible watches, already accepted elsewhere, successful transfer, stale watch state, and expired offer.

## WF-11 — Watch box

**Purpose:** Make inventory pressure and every watch's commercial state easy to scan.

**Required elements:**

- Inventory and Album views under the unchanged Watch Box title.
- Six starting inventory slots.
- An Album card for every catalog model, arranged four per row with the model name always visible.
- Album artwork absent until first ownership, then permanently revealed even after sale.
- The first tap on a revealed card lifts it into a larger centered focus state above the Album; the next tap flips it to expose concise brand and model-history notes.
- Only one card may be focused or flipped at a time; tapping outside returns it to the Album, and undiscovered model pockets do not focus or flip.
- Watch image and identity.
- Acquisition cost.
- Estimated range.
- Condition, completeness, and configuration.
- No direct dealer-sell action; selling begins by visiting a dealer and choosing Sell.
- Marketplace status.
- Capacity progress or expansion.

**States:** Open slot, full box, pending offer, newly acquired watch, selected watch, capacity expansion, undiscovered Album model, newly revealed Album model, previously owned but no-longer-held model, one focused Album card, and one flipped Album card.

## WF-12 — Progression and grants

**Purpose:** Make career advancement legible through Cities and challenge-based Badges while retaining the separate seven-day Cash grant.

**Required elements:**

- Current Reputation.
- Cities above Badges.
- A row of circular City progress indicators driven by story missions.
- Automatic permanent city access when its required story mission is completed.
- A row of circular Badge indicators with visible challenge requirements and partial progress.
- Rewarded Gold where applicable.
- Cash grant countdown and amount.
- Permanent-access confirmation.

**States:** City not started, city partially progressed, city opened, Badge not started, Badge in progress, Badge earned, grant upcoming, grant available, and grant received.

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

## WF-14 — Bank clearance

**Purpose:** Explain why completed sale proceeds belong to the player but are not yet available to spend, and offer a clear Gold-based instant-clearance choice.

**Required elements:**

- Cash.
- Available Cash.
- Completed sale amount.
- Remaining bank-clearance time.
- Clearance tier based on transaction size.
- Gold cost for instant clearance.
- Normal wait and instant-clear actions.

**States:** Five-minute entry-level transfer, intermediate transfer, twelve-hour highest-tier transfer, partially elapsed timer, insufficient Gold, instantly cleared, and normally cleared.

## WF-15 — Gold storefront

**Purpose:** Let the player understand and purchase fixed packages of Gold without confusing Gold with Cash or watch inventory.

**Required elements:**

- Current Gold balance.
- Gold Clip at $1.99.
- Gold Roll at $4.99.
- Gold Case at $9.99.
- Gold Safe at $19.99.
- Gold Vault at $49.99.
- Exact Gold quantity in each package once tuned.
- Honest larger-package value comparison.
- Purchase confirmation and recovery for interrupted transactions.
- Link back to the Gold-funded action that opened the store, where applicable.
- Automatic Store routing when a Gold-funded action is attempted with an insufficient balance.

**States:** Normal store, purchase in progress, successful purchase, cancelled purchase, failed purchase, reconciled interrupted purchase, and unavailable regional product.

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

