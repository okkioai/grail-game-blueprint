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
6. The player chooses to negotiate, leave, or open **Sell**.
7. From **Sell**, the player can select an owned watch or ask what the dealer is currently looking for.

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

Every dealer buys every watch. A specialist gives a stronger counteroffer and may show more patience for a watch in their area.

The player leads a dealer sale by setting an opening asking price. The dealer counters, and every player response argues in favor of the owned watch. After the argument, the player explicitly chooses whether to hold the ask or lower it by a chosen Cash amount. The sale completes when the player accepts the dealer's current offer or the dealer accepts the player's revised ask.

This guarantees a liquidity route while letting the player control their own selling price. The player is never permanently trapped with an unwanted watch simply because no perfect buyer appears.

### Selling flow

1. Select an owned watch.
2. Choose an opened dealer.
3. Set an opening asking price.
4. Review the dealer's Cash counteroffer and specialty fit.
5. Use favorable watch facts to defend the watch.
6. Hold the asking price or lower it by a chosen Cash amount.
7. Continue until the dealer accepts the revised ask, patience produces a final counteroffer, or the player accepts the dealer's current offer.
8. On acceptance, transfer the watch, receive Cash, free the slot, and earn Reputation.

Selling to a dealer should be faster and more reliable than waiting for a player buyer. The likely tradeoff is a lower return.

## Dealer sourcing requests

### Confirmed rule

From **Sell**, the player can ask a dealer whether they need a particular watch. The dealer can respond with:

- A specific watch model they want.
- The maximum Cash amount they are willing to pay.
- A deadline exactly **two Game Days** from the request.

For example, a dealer might say that they are looking for a Cartier Santos and will pay up to $5,000 for one during the next two Game Days.

### Design purpose

A sourcing request gives the player a potential exit before they own the watch. It turns market knowledge into a concrete short-term objective: find the requested model for less than the dealer's stated maximum, then return before the demand expires.

The feature also connects the acquisition systems. The player can search for the watch through:

- Another street dealer.
- An auction.
- The player marketplace.

The player is not given the watch or directed to a guaranteed source. The opportunity comes from recognizing a possible margin and finding supply before time runs out.

### Sourcing flow

1. Open **Sell** with a street dealer.
2. Choose between selecting an owned watch and asking what the dealer needs.
3. Receive the requested model, maximum Cash price, and two-Game-Day deadline.
4. Decide whether the potential margin is worth pursuing.
5. Search other dealers, auctions, and the marketplace for the requested watch.
6. Acquire a matching watch using Cash and an available inventory slot.
7. Return to the requesting dealer before the deadline.
8. Select the sourced watch and complete the sale under the final request and negotiation rules.

### Timing and visibility

The request remains valid through the next two Game Days. The interface must show both the remaining Game Days and the real-time expiry so the player does not have to convert the game clock mentally.

The active request should remain visible outside the original conversation. At minimum, the player needs a route from the room hub or watch box back to the requesting dealer.

### What the request does not guarantee yet

The request confirms the model, maximum price, and two-Game-Day window. The following details remain open and must not be silently assumed in implementation:

- Whether the maximum is a guaranteed purchase price or the ceiling of a new sale negotiation.
- Which condition, completeness, or configuration requirements must match.
- Whether asking creates a tracked commitment, or simply reveals temporary dealer demand.
- How many sourcing requests may be active at once.
- What happens if the dealer's normal stock refreshes while the request is active.
- Whether the player earns extra Reputation for fulfilling the request.

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
- A sourcing request with no matching watch currently available.
- Returning with the requested model after the two-Game-Day deadline.
- Returning with the correct model but unresolved condition, completeness, or configuration requirements.
- More than one dealer requesting the same model.

## Wireframe implications

The dealer storefront, watch fact sheet, and sourcing-request state should be separate wireframes. The storefront is about comparison and character; the fact sheet is about a single commercial decision; the sourcing request is about a model, target exit price, and deadline.

Dealer portrait, stock, specialty, and refresh time should be visible without competing with the watch itself. On the fact sheet, the primary action is **Negotiate** and the secondary action is **Leave**. Under **Sell**, selecting an owned watch and asking what the dealer needs must be clearly different actions.

## Open tuning

- Number of dealers per location.
- Exact stock refresh behavior.
- Price spread by dealer personality.
- How strongly specialty affects sale and purchase prices.
- Whether relationship memory affects prices in the MVP.
- Whether projected resale ranges appear at launch.
- Whether the sourcing-request maximum is guaranteed or negotiable.
- Match requirements beyond the requested model.
- Request availability, concurrency, and refresh rules.
- Reputation reward for fulfilling a request.

