# Player state and progression

[← Blueprint index](../README.md)

## Confirmed starting fantasy

The player begins as a rookie watch dealer working from a bedroom in New York City.

The room is both the first headquarters and the emotional baseline for the career. It contains the player's desk, balances, watch box, and routes into the first local opportunities. It should feel modest, personal, and plausible—not like a luxury showroom unlocked before the player has earned anything.

## Starting state

| Element | Confirmed role | Still to tune |
|---|---|---|
| Cash | Working capital for the first deals | Exact starting amount |
| Watches | A small initial collection | Number, models, and acquisition history |
| Inventory | Six available watch slots | Whether starter watches occupy several slots |
| Reputation | Near zero | Exact initial value and first threshold |
| Gold | Optional capacity and acceleration currency | Initial grant and early reward cadence |
| Location | New York City bedroom and first local market | Exact dealer count and neighborhood presentation |

The player should have enough freedom to make a meaningful first choice, but not enough liquidity to make every early mistake irrelevant.

## Reputation

### Confirmed rule

Reputation is permanent career XP. It increases through meaningful participation and never decreases in the MVP.

### What it represents

Reputation is the market's recognition that the player is becoming a real dealer. It is not money, trust with one specific character, or a spendable token. It is the account-wide measure of career progress.

### Actions that can earn Reputation

The exact reward table remains open, but the system is expected to recognize:

- Buying a watch.
- Selling a watch.
- Completing a successful negotiation.
- Participating in or winning an auction.
- Posting or completing a marketplace offer.
- Reaching commercial milestones.
- Discovering or dealing in a watch family for the first time.

Rewards should favor meaningful outcomes over repetitive button presses. Simply opening and closing screens should never be an efficient way to progress.

### What Reputation unlocks

- Larger watch boxes at selected career thresholds.
- Higher-value opportunities and dealers.
- Future progression features that communicate expertise and reach.

### What Reputation does not do

- It cannot be spent.
- It cannot be bought directly with Cash.
- It cannot be converted to Gold.
- It does not decline after a weak deal.
- It does not block return travel to an opened location.

## Career badges

The Career page separates progression into **Cities** and **Badges**. Cities show the player's commercial reach. Badges are challenge-based achievements for meaningful actions such as completing a first deal, selling a watch, landing strong rebuttals, winning an auction, completing a marketplace trade, and discovering models.

Badge challenges may expand as content is added. Their requirements must be visible, their progress must come from authoritative game events or the deal ledger, and they do not spend Reputation or Gold.

## Location progression

Cities unlock permanently through completion of specific story missions. Gold and Reputation are not direct requirements to reveal, open, or travel to a core city.

Reputation communicates career standing and may be used as a visible mission objective, but reaching a Reputation value alone does not open a city. Gold remains an optional capacity and acceleration currency rather than a gate on core advancement.

## Story missions

Missions are the ordered story path of GRAIL. Every player follows the same versioned sequence and has at most one active mission. Each mission presents visible objectives, advances only from authoritative game events or the deal ledger, completes once, and may permanently unlock characters, opportunities, narrative scenes, or cities.

Mission progress never decreases. The client displays progress but does not declare a mission complete. Completion, rewards, and activation of the next mission must settle atomically on the server so retries cannot duplicate progress or rewards.

The first mission is **The Introduction**:

1. A closed text-message card from Fresh Mike appears prominently on the Home screen as “New message from Mike.” Selecting **View** opens a dialogue overlay above the dimmed Home screen with Mike's 3D dealer presentation and the same typed text-bubble language used in negotiation; his request and the dialogue action lead to the Streets map.
2. The message remains the active direction until the player enters Fresh Mike's shop.
3. In Mike's shop, the same 3D dealer presentation and typed negotiation-style bubble show him explaining that he wants to introduce the player to Benny Adler, a dealer friend who may be interested in the starter watch Mike gave the player.
4. Completing the conversation permanently unlocks Benny on the Streets map.

This mission card replaces generic prompts such as “Go find the next deal.” The game leads the player with the current authored mission rather than a permanent sandbox-direction banner.

### Permanent access

Once opened, a location remains available. The player may always travel back to an earlier location.

Earlier locations should continue to have value through:

- Familiar dealers and preferred personalities.
- Lower-priced inventory when Cash is tight.
- Particular watch specialties or configurations.
- Opportunities suitable for a smaller, faster deal.

New locations therefore broaden the market rather than replacing old content.

## Location identity

A location should change the commercial landscape, not merely the background art. It may differ through:

- Dealer personalities and patience profiles.
- Common watch families and price tiers.
- Average condition and completeness.
- Pricing aggressiveness.
- Auction mix.
- Marketplace demand signals.
- Visual atmosphere and room status.

The starting New York environment establishes the basic rules. Later locations can become more specialized and higher stakes.

## Progression rhythm

A healthy progression beat follows this pattern:

1. The player completes deals, advances badge challenges, and earns Reputation.
2. The next city remains visible with its required story mission and partial mission progress.
3. The preview explains why the market is desirable.
4. Completing the required mission unlocks the city automatically.
5. The new city creates a clear step up in opportunity.
6. The old cities remain useful options.

The visible progress period matters. A city should become an earned aspiration rather than an unexplained purchase.

## Inventory progression

The player begins with six watch slots. Larger watch boxes can unlock through Reputation as permanent progression. Gold can also purchase permanent watch-space expansion, provided the free progression path remains usable.

Inventory expansion should be meaningful but not eliminate scarcity too quickly. The strategic question—what deserves a slot?—should survive throughout the game.

## Player flow: opening a location

1. The city appears in the Career track with its required story mission.
2. The progress circle fills as the associated mission objectives are completed.
3. Completing the mission celebrates the story milestone and opens the city permanently.
4. The unlocked city appears in normal travel alongside every earlier location.

## Wireframe implications

The room hub and progression screens must keep the resources visually distinct:

- Cash should read as working capital.
- Gold should read as optional capacity and acceleration.
- Reputation should read as an accumulating career track.

The Career screen needs three unmistakable city states:

1. Visible with little or no Reputation progress.
2. Partially filled toward the required mission completion.
3. Unlocked and permanently travelable.

It also needs incomplete, in-progress, and earned Badge states.

## Open tuning

- Exact starting Cash, Gold, watches, and Reputation.
- Reputation rewards by action.
- Mission ordering, objective pacing, and city-unlock timing.
- Number of MVP locations.
- Timing and price of inventory expansions.
- Whether the player's room itself visually upgrades within the MVP.

