# GRAIL

> **The first watch-dealing strategy game.**
>
> Start in a New York bedroom. Learn the market. Make the deal. Build a name.

GRAIL is a mobile strategy game about becoming a watch dealer. The player begins with a desk, a small collection, limited Cash, and almost no Reputation. Every watch is both an object of desire and a commercial decision: inspect it, understand the opportunity, negotiate the price, commit capital, and find the right exit.

This repository is the living design blueprint for the MVP. It records the rules we have agreed on, separates confirmed direction from unresolved tuning, and provides the briefs that will guide wireframes and prototypes.

## The fantasy

You are not opening loot boxes or collecting static cards. You are building a dealing career.

At first, every purchase matters. Six inventory slots make space scarce. A poor deal can tie up most of your Cash. A sharp rebuttal can improve a price. A specialist dealer may offer the fastest exit. An auction may tempt you past your margin. A player on the other side of the market may be looking for exactly what you own.

Over time, profitable decisions create buying power. Meaningful actions earn permanent Reputation. Reputation reveals better locations, and Gold opens them. The rooms become more impressive, the characters more connected, and the watches more consequential—but the heart of the game remains the same: **is this a good deal?**

## The MVP loop

```text
Find an opportunity
        ↓
Read the watch and the price
        ↓
Negotiate or bid
        ↓
Buy with Cash
        ↓
Manage scarce inventory
        ↓
Sell to a dealer or player
        ↓
Reinvest profit and build Reputation
        ↺
```

## Three resources, three jobs

| Resource | Meaning | Used for |
|---|---|---|
| **Cash** | Working capital | Buying and selling watches; funding marketplace offers |
| **Gold** | Access and acceleration | Opening locations, extra auction entries, capacity, and convenience |
| **Reputation** | Permanent career progress | Revealing locations and unlocking long-term progression |

The separation is fundamental. **Gold never buys watches and never converts directly to Cash.** Real-money spending may increase access and opportunity, but the watch economy remains a Cash economy.

## Confirmed foundations

- The player starts as a rookie dealer in a bedroom in New York City.
- One Game Day lasts three real hours. There is no energy system or action limit.
- The game grants Cash every seven real days to reopen opportunity.
- Reputation never decreases in the MVP.
- Reputation reveals locations; Gold opens them permanently.
- Players can always travel back to previously opened locations.
- Street dealers show up to five rotating watches.
- Watch facts appear immediately; inspection is not a compulsory tapping ritual.
- Negotiation uses contextual rebuttals, a press-and-hold action, and dealer patience.
- Every dealer buys every watch, with stronger offers from specialists.
- Two auction entries are free each Game Day; additional entries cost Gold.
- All player-owned watches are automatically discoverable in the marketplace.
- Buyers post model-specific Cash offers; matching owners receive notifications.
- The player begins with six watch slots and three active marketplace offer slots.
- The MVP targets roughly six to ten recognizable watch families.

## Blueprint index

### Product foundation

1. [Vision and design principles](docs/01-vision-and-principles.md)

   Product promise, player fantasy, experience principles, and session texture.

2. [Player state and progression](docs/02-player-and-progression.md)

   Rookie starting state, Reputation, locations, travel, and long-term growth.

3. [Time, economy, and core loop](docs/03-loop-time-and-economy.md)

   Game Days, recurring Cash, resource boundaries, and the complete commercial loop.

### Deal activities

4. [Street dealers and watch discovery](docs/04-street-dealers.md)

   Dealer characters, rotating stock, watch fact sheets, buying, and selling.

5. [Negotiation and haggling](docs/05-negotiation.md)

   The Read → Rebut → Press → Decide cycle, patience, outcomes, and mobile input.

6. [Auctions](docs/06-auctions.md)

   Entry rules, bidding flow, projected margin, NPC competition, and Gold use.

7. [Player marketplace](docs/07-player-marketplace.md)

   Automatic discoverability, buyer offers, seller notifications, reserved Cash, and safeguards.

### Supporting systems

8. [Inventory, watches, and content](docs/08-inventory-and-content.md)

   Six-slot watch box, catalog structure, variation axes, facts, and dealer writing.

9. [MVP scope](docs/09-mvp-scope.md)

   What ships, what does not, and the boundaries that protect the first version.

10. [Wireframe plan](docs/10-wireframe-plan.md)

    Twelve screen briefs, required information, interaction states, and image conventions.

11. [Open questions and decision log](docs/11-open-questions.md)

    Balance questions still requiring answers and a concise record of settled decisions.

## How to read this repository

Each system document follows the same pattern:

- **Confirmed rule** — direction already agreed upon.
- **Player flow** — what the player sees and does.
- **Design intent** — why the rule exists.
- **Open tuning** — numbers or edge cases still to resolve.
- **Wireframe implications** — what the interface must communicate.

That distinction matters. The blueprint should be specific enough to build from without pretending that untested balance values are final.

## Current status

**Phase:** MVP definition and wireframing

**Document version:** 0.2

**Last updated:** November 2026

The next production pass is to insert wireframes beside the relevant system flows, then use the open-question list to plan focused prototypes and economy tests.

---

GRAIL is a working title and an evolving game design. This repository documents product direction; it is not a promise of final features or balance.
