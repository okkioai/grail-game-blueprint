# Open questions and decision log

[← Blueprint index](../README.md)

## How this page is used

The decision log records product direction that should not be reopened casually. The open-question list contains balance values, edge cases, or implementation choices that still need prototypes or explicit decisions.

An open question does not make the entire system unconfirmed.

## Decision log

| Area | Confirmed decision | Consequence |
|---|---|---|
| Player role | Rookie dealer in a New York City bedroom | Progress begins from a modest, personal headquarters |
| Reputation | Permanent and never decreases in the MVP | Poor deals cost liquidity, not career progress |
| Locations | Reputation reveals; Gold opens | Qualification and monetized access have separate roles |
| Travel | Earlier opened locations remain accessible | New markets broaden rather than replace the game |
| Time | One Game Day equals three real hours | Eight opportunity-refresh cycles occur per real day |
| Player actions | No energy system or action limit | The market refreshes, but the game does not stop play |
| Cash support | Game grants Cash every seven real days | Recovery is predictable and separate from Game Days |
| Bank clearance | A completed sale increases Cash immediately; Available Cash increases after an amount-based wait from five minutes to twelve hours | Gold can accelerate access to earned proceeds without creating Cash |
| Cash display | The global economy shows Cash and Available Cash only | Sale transactions and offers explain why part of Cash is unavailable without adding more balances |
| Dealer stock | Up to five watches, rotating over time | Storefronts stay readable and refreshable |
| Inspection | Known facts appear on the first watch screen | No compulsory multi-tap ritual |
| Negotiation | Three rebuttals, one strong answer | Visible watch knowledge becomes playable |
| Negotiation input | Press and hold rather than slider/swipe | The signature action is one-thumb friendly |
| Dealer patience | Runs down and ends in a final price | Haggling has a finite cost and shape |
| Dealer selling | Every dealer buys every watch | The player always has a liquidity route |
| Dealer-sale entry | Selling begins at a dealer storefront; Watch Box does not expose a direct sell action | The player chooses the buyer before entering the mirrored negotiation |
| Dealer sourcing | From Sell, a dealer may request a model and quote a maximum Cash price for the next two Game Days | The player can identify an exit, source across channels, and attempt an arbitrage deal before demand expires |
| Auction allowance | Two free entries per Game Day | Gold sells additional opportunity after a usable free allowance |
| Marketplace supply | Owned watches are automatically discoverable | Buyers create demand; sellers need not maintain listings |
| Marketplace trade | Buyer posts Cash offer; matching owners are notified | First valid owner acceptance completes the transfer |
| Offer capacity | Three active slots initially; Gold permanently adds more | Paid capacity expands parallel demand, not watch purchasing power |
| Starting inventory | Six watch slots | Ownership has a clear opportunity cost |
| Watch capacity | Gold purchases permanent watch-space expansion; Reputation also provides a progression path | Paid capacity accelerates growth without making the free route impossible |
| Gold storefront | Five fixed package price points from $1.99 to $49.99 | Players can purchase Gold directly without Cash, watches, or randomized contents in standard packages |
| Home and navigation | The activity feed lives in Your room; the dock is Room, Watch Box, Market, Streets, and Career | Collection and Store access are anchored at home while persistent navigation stays compact |
| Visual rollout | Approved Figma screens may advance beyond wireframes; unfinished routes inherit the shared shell and retain placeholders | Visual maturity can progress without deciding open game rules |
| Catalog | Roughly six to ten families | MVP favors depth and variation over breadth |
| Currency boundary | Cash buys watches; Gold buys access and speed | Real-money currency cannot directly purchase inventory |

## Priority open questions

### Starting state

- How much Cash does the player receive?
- How much Gold, if any, is available immediately?
- How many starter watches are owned?
- Which watch families teach the first decisions best?
- How much empty inventory space remains?

**Why it matters:** These values determine first-session freedom, failure tolerance, and how quickly the player encounters inventory pressure.

### Cash grant

- How large is the seven-day grant?
- Is the amount fixed or scaled by Reputation?
- Must it be claimed?
- Do missed grants accumulate?
- Is there a maximum accumulation?

**Why it matters:** Too much Cash makes profit irrelevant; too little fails to recover a stuck player.

### Bank clearance

- Which Cash thresholds map to the clearance-time tiers?
- What are the intermediate durations between five minutes and twelve hours?
- Does every sale channel use the same curve?
- Does the seven-day Cash grant become Available Cash immediately?
- How much Gold clears a transfer?
- Does the Gold cost depend on original duration, remaining duration, or a fixed tier?
- Can more than one completed sale clear simultaneously?

**Why it matters:** Bank clearance is the primary repeatable time-skip purchase. It must create a meaningful choice without leaving a player unable to continue dealing.

### Reputation

- Which actions grant Reputation?
- How much does each action grant?
- Are failed negotiations or auction drop-outs rewarded?
- How are repetitive low-value actions prevented from becoming the best progression strategy?
- What are the location and inventory thresholds?

**Why it matters:** The reward table defines the pace and tells players what the game values.

### Negotiation

- What happens after an incorrect rebuttal?
- How does the press meter determine success?
- Can pressure be too weak or too strong?
- Does patience fall every round, every error, or both?
- Can a fact be reused?
- How does difficulty scale by dealer and location?
- Does the final price improve, hold, or harden?

**Why it matters:** These rules determine whether negotiation feels strategic, readable, and replayable.

### Dealer economy

- How much stronger is a specialist's offer?
- How large is the buy/sell spread?
- Do dealer prices change across Game Days?
- Does leaving a negotiation preserve its state?
- Can the same watch return after a refresh?
- Is a sourcing request's stated maximum a guaranteed purchase price or the ceiling of a new negotiation?
- Which condition, completeness, and configuration requirements must a sourced watch satisfy?
- How often does a dealer have a sourcing request?
- How many requests can the player track at once?
- Does a request survive the dealer's normal stock refresh?
- Does fulfilling a request award additional Reputation?

**Why it matters:** Dealers define the dependable floor of liquidity and the baseline economy. Sourcing requests also create temporary demand and cross-system arbitrage, so their price certainty and matching rules must be explicit.

### Auctions

- How long does an auction last?
- How many NPC bidders participate?
- How are their valuations generated?
- When is an entry consumed?
- Do unused entries expire each Game Day?
- What is the Gold cost of additional entries?
- Is inventory capacity validated before entry?

**Why it matters:** These decisions affect session length, fairness, tension, and monetization pressure.

### Marketplace

- How long does an offer remain active?
- When may a buyer cancel or edit it?
- When is reserved Cash released?
- Can an owner hide a watch from matching?
- What price bounds prevent extreme offers?
- Are there marketplace fees?
- How are spam, collusion, and self-dealing detected?
- What happens if watch state changes after notification?

**Why it matters:** Peer-to-peer pricing requires authoritative, abuse-resistant rules before release.

### Inventory

- At which Reputation thresholds do larger boxes unlock?
- How many slots does each expansion add?
- Is Gold expansion permanent?
- How early can a player buy capacity?
- How does the game handle an auction when the final slot disappears?
- Does Gold buy individual watch spaces or staged box upgrades?
- What is the maximum Gold-purchased capacity?

**Why it matters:** Capacity must create strategy without becoming a constant frustration or disappearing too early.

### Catalog and locations

- Which six to ten watch families ship?
- How many variations per family are required?
- How many locations ship in the MVP?
- How many dealers live in each location?
- What commercial difference defines each location?
- Which art and writing costs constrain the plan?

**Why it matters:** This is the primary content-production scope.

### Gold and monetization

- Which progression beats award free Gold?
- What are location, entry, offer-slot, and inventory prices?
- Which expedited processes exist at launch?
- Are convenience purchases permanent or consumable?
- What free allowance makes every system genuinely usable?
- How much Gold is included in each $1.99, $4.99, $9.99, $19.99, and $49.99 package?
- What transparent value bonus does each larger package receive?
- How are package prices localized by platform and region?

**Why it matters:** Gold must support the business without undermining the core watch economy.

## Recommended prototype order

1. **Dealer transaction vertical slice** — fact sheet, buying negotiation, inventory, and dealer sale.
2. **Negotiation tuning prototype** — rebuttal consequences, pressure meter, and patience curves.
3. **Economy simulation** — Cash flow, dealer spreads, inventory lock-up, bank-clearance tiers, Gold costs, storefront quantities, and seven-day recovery.
4. **Auction prototype** — bid rhythm, NPC ceilings, and projected margin.
5. **Marketplace service model** — matching, reservation, server-authoritative acceptance, and abuse cases.
6. **Progression model** — Reputation cadence, location thresholds, Gold rewards, and expansion timing.

## Change protocol

When a question is resolved:

1. Update the relevant system document.
2. Move the result into the decision log above.
3. Remove or rewrite the open question.
4. Update any affected wireframe states.
5. Record the change in the commit message.

