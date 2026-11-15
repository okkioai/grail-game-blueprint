# Core loop, time, and economy

[← Blueprint index](../README.md)

## The commercial loop

The MVP is built around one repeatable cycle:

1. **Maintain buying power.** Preserve Cash through good exits, earn profit, or receive the periodic game grant.
2. **Find an opportunity.** Visit a street dealer, discover a dealer sourcing request, preview an auction, or create/respond to a marketplace offer.
3. **Read the watch.** Understand condition, completeness, configuration, known facts, and current price.
4. **Make the deal.** Negotiate, bid, accept, decline, or walk away.
5. **Commit Cash and space.** An acquired watch occupies inventory and ties up capital.
6. **Choose an exit.** Sell to a dealer for liquidity or wait for a suitable player offer.
7. **Reinvest.** Use the proceeds to pursue the next opportunity while Reputation advances the career.

The loop is intentionally circular. There is no separate combat game or unrelated resource layer. The deal itself generates the next deal.

## Game Days

### Confirmed rule

One Game Day lasts **three real hours**. There are eight Game Days in a normal 24-hour day.

### Purpose

The Game Day is a market refresh clock. It gives the world rhythm and creates reasons to return without restricting how much the player can do.

At a Game Day boundary, the game can:

- Refresh dealer stock.
- Advance and expire two-Game-Day dealer sourcing requests.
- Present new auction opportunities.
- Advance or refresh marketplace activity.
- Update selected timers and notifications.
- Restore the player's two free auction entries.

### No action cap

Players may act as much as they want during a Game Day. There is no energy bar, stamina, or limited number of dealer visits.

Scarcity comes from Cash, inventory space, patience, entries, and opportunities—not from a universal permission-to-play meter.

## The seven-day Cash grant

### Confirmed rule

The game grants the player Cash every **seven real days**.

This cadence is separate from the three-hour Game Day. A player experiences 56 Game Days during one seven-day grant interval.

### Purpose

The grant is a recovery and re-engagement mechanism. It ensures that a player who made poor early deals, tied up capital, or returned after an absence can eventually pursue another watch opportunity.

It should reopen play without making successful dealing irrelevant.

### Design boundaries

- The grant is Cash, not Gold.
- It enters the watch economy directly.
- It should be clearly presented as support from the game, not revenue from a sale.
- Its amount must not erase the importance of profit.
- Claim behavior and accumulation are still unresolved.

## Three-resource economy

### Cash: the watch economy

The interface exposes two Cash figures:

- **Cash** is the player's total money, including proceeds from completed sales that are still clearing at the bank.
- **Available Cash** is the portion currently cleared and usable for purchases, bids, and marketplace offers.

Cash is used to:

- Buy watches from dealers.
- Pay for auction wins.
- Fund marketplace buyer offers.

Cash is received from:

- Selling watches to dealers.
- Selling watches through the player marketplace.
- The seven-day game grant.

Cash should be legible as working capital. When it is tied up in watches or reserved for offers, the player has fewer available opportunities.

### Bank clearance

Every completed sale increases Cash immediately. The sale proceeds increase Available Cash only after the bank clears the transfer.

Clearance time is based on transaction size. The larger the sale, the longer the wait. The current target curve begins at **five minutes** for an entry-level transfer and reaches **twelve hours** for the largest tier. Exact Cash thresholds and intermediate durations remain economy-simulation questions.

The sale transaction displays its remaining clearance time. The global economy does not introduce separate Pending Cash or Reserved Cash balances. Instead, Cash shows the total, Available Cash shows what can be used now, and the relevant transaction or marketplace offer explains the difference.

Gold can clear an earned sale immediately. This accelerates access to existing Cash; it does not create Cash, increase the sale price, or purchase a watch.

### Gold: access and acceleration

Gold is earned through progression and can also be purchased. It may be used to:

- Open a location after its Reputation requirement is met.
- Enter more than two auctions in a Game Day.
- Permanently unlock more active marketplace offer slots.
- Permanently purchase more watch space.
- Clear an earned sale immediately instead of waiting for the bank.

Gold never:

- Buys a watch.
- Pays a dealer's asking price.
- Funds an auction bid.
- Funds a marketplace offer.
- Converts directly into Cash.

This is the central fairness boundary for monetization.

### Gold storefront

Players can purchase packages of Gold from a dedicated storefront reached by tapping the Gold balance.

If the player attempts any Gold-funded action without enough Gold, the interface opens this storefront with the attempted action and shortage explained. The player must be able to return directly to that action afterward.

The initial package ladder is:

| Package | Price |
|---|---:|
| Gold Clip | $1.99 |
| Gold Roll | $4.99 |
| Gold Case | $9.99 |
| Gold Safe | $19.99 |
| Gold Vault | $49.99 |

Exact Gold quantities and larger-package bonuses remain open until the Gold costs of locations, watch space, offer slots, auction entries, and bank clearance are simulated together. The launch storefront does not require a $99.99 package.

The store shows the current Gold balance, exact package contents, local purchase price, and honest value comparison. Standard packages do not contain Cash, watches, randomized rewards, or mystery contents.

### Reputation: permanent progress

Reputation is earned through meaningful play and used as a requirement for progression. It is not spent and does not decrease in the MVP.

## Why the separation matters

Each resource answers a different question:

- **Cash:** Can I afford this watch?
- **Gold:** Can I access more opportunity or get there sooner?
- **Reputation:** Has my career progressed far enough?

Combining these roles would weaken the strategy. If Gold bought watches, spending could bypass the core judgment loop. If Reputation were spendable, career progress would become harder to read. If Cash opened every system, a weak trading streak could lock the player out of the broader game.

## Economy pressure points

The economy should produce several understandable tensions:

- A watch may be profitable but consume too much available Cash.
- A dealer request may reveal a profitable exit, but the player still has to source the right watch before the two-Game-Day window closes.
- A full watch box may force a sale before the player can acquire another opportunity.
- A marketplace offer reserves Cash that could otherwise fund a dealer purchase.
- A completed sale may increase total Cash while the player waits for the proceeds to become Available Cash.
- An auction can remain attractive while each bid narrows the expected margin.
- Gold may unlock more opportunity, but the player still needs Cash to act on it.

## Failure and recovery

The MVP avoids hard career failure. A poor deal can reduce liquidity, but:

- Reputation remains intact.
- Opened locations remain accessible.
- Owned watches can always be offered to dealers.
- The seven-day Cash grant eventually adds new working capital.

Recovery should take a player back to meaningful decisions, not remove the consequences of weak judgment immediately.

## Wireframe implications

Every purchase screen should distinguish:

- Cash.
- Available Cash.
- Inventory capacity.
- The exact amount that will leave or enter the account.

Individual sale and marketplace-offer screens must explain why Cash is not currently available without creating additional top-level balances.

Timers should name their cadence explicitly. “Next Game Day” and “Next Cash grant” cannot look like the same system.

## Open tuning

- Starting Cash and early price ladder.
- Weekly grant amount, scaling, and accumulation.
- Which actions earn Gold through progress.
- Gold price ladder for access and capacity.
- Cash thresholds and intermediate durations between the five-minute and twelve-hour bank-clearance endpoints.
- Gold cost of instant clearance and whether it scales with remaining time.
- Whether every sale channel uses the same clearance curve.
- Exact Gold quantities and package bonuses in the storefront.
- Cash reservation and cancellation behavior.
- Inflation controls for the player marketplace.
- Whether dealer refreshes are identical at every Game Day boundary.

