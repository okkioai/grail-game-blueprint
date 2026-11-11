# Street dealers and watch discovery

[← Blueprint index](../README.md)

## System role

Street dealers are the main repeatable activity in GRAIL. They give the market a human face and provide the most direct path from seeing a watch to negotiating and buying it.

Each dealer is a persistent named character with a backstory, visual identity, specialty, and recognizable commercial behavior. The player should gradually learn how different dealers price, argue, and buy.

## Dealer stock

### Confirmed rule

A dealer shows **up to five watches** at a time. The selection changes over time and refreshes through the Game Day system.

“Up to five” allows a dealer to feel temporarily scarce or selective without making the storefront appear broken. The exact count may change from one refresh to another.

### Stock should communicate character

Dealer inventory should not feel like five random records from a global table. A dealer's specialty can influence:

- Watch families that appear more often.
- Typical price range.
- Average condition or completeness.
- Tolerance for unusual configurations.
- Opening sale prices.
- Purchase offers when the player sells.

The specialty makes character knowledge commercially useful.

## Dealer storefront flow

1. The player selects a dealer in the current location.
2. The dealer appears with a short line of dialogue and a visible specialty.
3. Up to five available watches are shown with enough information to compare them.
4. The player selects a watch.
5. The watch fact sheet opens.
6. The player chooses to negotiate, leave, or switch to selling an owned watch.

The storefront should also display when stock will refresh, but the timer should not dominate the interaction.

## Watch fact sheet

### Confirmed rule

Inspection is informational, not a ritual. The first watch screen presents the watch and every fact currently known about it. The player is not required to tap several arbitrary hotspots before the game reveals basic information.

### Required information

At minimum, the fact sheet should show:

- Watch family or model.
- A strong watch image.
- Condition tier and relevant wear.
- Completeness, such as box and papers.
- One major configuration, where applicable.
- Dealer asking price.
- Player's available Cash.
- Every fact that may become a negotiation rebuttal.
- Inventory capacity or a warning when the watch box is full.

A projected resale range may be shown if testing supports it. If used, it must be communicated as an estimate rather than a guaranteed sale price.

## Opportunity evaluation

Before negotiation, the player should be able to answer:

- What exactly is being offered?
- What does the dealer want?
- What weakens or strengthens the price?
- Can I afford it?
- Do I have room for it?
- What might my exit be?

The game may withhold advanced or uncertain information in later versions, but the MVP should not hide knowledge required to identify the correct response in the negotiation.

## Buying from a dealer

1. Review the watch and known facts.
2. Enter negotiation.
3. Respond to the dealer's price claim.
4. Improve the price if the rebuttal and pressure action succeed.
5. Accept the current price, continue, or leave.
6. Confirm the Cash purchase.
7. Move the watch into an available inventory slot.
8. Award Reputation for the meaningful transaction.

If inventory is full, the game should stop the final purchase before Cash moves and explain valid next steps.

## Selling to a dealer

### Confirmed rule

Every dealer buys every watch. A specialist gives a stronger opening offer and may show more patience for a watch in their area.

This guarantees a liquidity route. The player is never permanently trapped with an unwanted watch simply because no perfect buyer appears.

### Selling flow

1. Select an owned watch.
2. Choose an opened dealer.
3. Review the dealer's Cash offer.
4. See whether the watch matches the dealer's specialty.
5. Use favorable watch facts to argue for a stronger offer.
6. Accept the offer or leave with the watch.
7. On acceptance, transfer the watch, receive Cash, free the slot, and earn Reputation.

Selling to a dealer should be faster and more reliable than waiting for a player buyer. The likely tradeoff is a lower return.

## Dealer character model

Each dealer needs a concise content profile:

- **Name and visual hook.** Immediately recognizable in a small mobile portrait.
- **Backstory.** Why this person is in this market.
- **Specialty.** The watches they understand and value most.
- **Voice.** Sentence length, confidence, humor, and vocabulary.
- **Pricing behavior.** Aggressive, fair, erratic, or relationship-oriented.
- **Patience profile.** How many rounds they tolerate and how they react near the end.
- **Preferred arguments.** The facts they use to defend a price.
- **Buying behavior.** How specialty influences offers for the player's watches.

Backstory should emerge through short repeated interactions, not long exposition before the player can deal.

## Edge states

The dealer experience must handle:

- No affordable watches.
- A watch box with no open slot.
- Dealer stock that has refreshed while the screen is open.
- Insufficient Cash after another offer reserves funds.
- A watch that the player already owns in another configuration.
- Leaving negotiation without buying.
- Returning after the dealer has given a final price.

## Wireframe implications

The dealer storefront and watch fact sheet should be separate wireframes. The first is about comparison and character; the second is about a single commercial decision.

Dealer portrait, stock, specialty, and refresh time should be visible without competing with the watch itself. On the fact sheet, the primary action is **Negotiate** and the secondary action is **Leave**.

## Open tuning

- Number of dealers per location.
- Exact stock refresh behavior.
- Price spread by dealer personality.
- How strongly specialty affects sale and purchase prices.
- Whether relationship memory affects prices in the MVP.
- Whether projected resale ranges appear at launch.

