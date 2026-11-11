# Auctions

[← Blueprint index](../README.md)

## System role

Auctions are the second major acquisition route. They replace a conversational price negotiation with escalating competition and time pressure.

The strategic question is not simply whether the player can win. It is whether the watch remains a good opportunity after the next bid.

## Access rule

### Confirmed rule

The player receives **two free auction entries per Game Day**. Additional auction participation during the same Game Day costs Gold.

The player is never required to use the free entries. Whether unused entries accumulate is still unresolved; the default assumption is that they reset rather than stack.

## Auction preview

Before entering, the player should see:

- Watch image and family.
- Known condition, completeness, and configuration.
- Current or opening price.
- Expected bid increment.
- Projected resale range, when available.
- Available Cash.
- Remaining free entries.
- The Gold cost if free entries are exhausted.

The player should be able to decline without consuming an entry.

## Entry consumption

The exact consumption moment remains a tuning question. The clearest default is to consume the entry when the player confirms participation and the active bidding scene begins.

If the auction becomes unavailable before the player can bid, the entry should be restored.

## Bidding flow

1. Preview the lot and decide whether it deserves an entry.
2. Confirm participation.
3. Watch NPC bidders accept the current increments.
4. Press to accept the next bid when another bidder raises the price.
5. See the projected margin update after every increase.
6. Continue or drop out.
7. Win when no competing bidder accepts the next increment.
8. Pay Cash and move the watch into inventory.

The bid control should be press-based and deliberate. A confirmation treatment may be needed for unusually large or margin-destroying bids.

## Projected profit

Projected profit should remain visible during the auction. It is calculated from an estimated resale range minus the current purchase price and any modeled fees.

It is a decision aid, not a promise. The eventual return depends on the player's exit, dealer specialty, marketplace demand, and the watch's exact state.

The display should become more cautionary as margin narrows:

- Healthy expected range.
- Thin margin.
- Break-even risk.
- Expected loss.

The player may still bid for strategic reasons, but the cost should be clear.

## NPC bidders

NPCs create the competitive rhythm. They should appear to have preferences and stopping points rather than bidding randomly forever.

Possible bidder parameters:

- Watch-family interest.
- Maximum valuation.
- Aggressiveness.
- Response delay.
- Chance of dropping before maximum value.

The player does not need to see these numbers. They should experience plausible competition and learn that some lots attract stronger demand.

## Outcomes

### Win

- Cash leaves the account.
- The watch occupies a free inventory slot.
- Reputation is awarded.
- The result shows final price and updated expected margin.

### Drop out

- No Cash is spent on the watch.
- The consumed auction entry remains used.
- The player sees the final or current outcome without being shamed for protecting margin.

### Insufficient Cash or inventory

The game should prevent entry when the player cannot complete a plausible purchase or has no available watch slot, unless the design explicitly supports arranging an exit first.

## Gold boundary

Gold buys another opportunity to participate after the two free entries. It does not:

- Place a bid.
- Improve the player's priority.
- weaken NPC bidders.
- Guarantee a win.
- Pay the final Cash price.

## Wireframe implications

The auction interface needs two screens or states:

1. **Lot preview:** facts, price context, entry cost, and decision to participate.
2. **Active bidding:** current bid, next increment, projected margin, Cash, NPC presence, and a large bid/drop-out decision.

The active screen must make accidental bids difficult while remaining fast enough to feel live.

## Open tuning

- Auction duration and bid timing.
- Number and behavior of NPC bidders.
- Bid increment curve.
- Entry consumption moment.
- Whether entries ever accumulate.
- Gold cost for additional entries.
- Resale estimate confidence and fees.
- Whether lots are shared globally or generated per player in the MVP.

