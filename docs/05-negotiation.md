# Negotiation and haggling

[← Blueprint index](../README.md)

## Interaction goal

Negotiation should be the signature action of GRAIL: readable, tense, repeatable, and comfortable with one thumb.

The player does not drag a price slider. They read a claim, choose evidence, and press to apply pressure while deciding how far to push a dealer whose patience is running out.

## The cycle

```text
READ → REBUT → PRESS → DEALER RESPONDS → DECIDE
  ↑                                      ↓
  └──────────── continue bargaining ─────┘
```

At any decision point, the player may accept the current price or walk away.

## Step 1: Read

The dealer states an asking price and makes a short claim about the watch.

Examples of claim types:

- The condition justifies the price.
- The configuration is unusually desirable.
- The watch is complete.
- The example is difficult to find.
- The price already reflects a visible flaw.

The sentence should be concise enough to read quickly and specific enough to answer with a fact from the watch screen.

## Step 2: Rebut

The game presents three text responses. One is the correct rebuttal because it uses a known fact that genuinely weakens the dealer's claim.

A good response set should contain:

- One factually relevant rebuttal.
- One true but commercially irrelevant observation.
- One weak, unsupported, or socially poor response.

The system tests attention and judgment, not obscure real-world trivia. Every required fact must already be visible on the fact sheet.

## Step 3: Press

After a correct rebuttal, the player presses and holds a large button. A meter fills while pressure is applied.

This action replaces a slider because pressing is more comfortable on mobile and creates a short physical beat without requiring a swipe.

The control should communicate:

- When pressure begins.
- How much has accumulated.
- Whether the player has reached a useful zone.
- When to release.
- The dealer's reaction as pressure increases.

The mechanic should not become a narrow reflex test. Knowledge remains the primary source of advantage.

## Step 4: Dealer response

When the rebuttal and press succeed, the dealer lowers the price and answers with another fact or claim about the watch.

The response serves three jobs:

1. Confirm that the player's action had an effect.
2. Present the new price.
3. Set up the next possible negotiation round.

The price movement should feel meaningful without making continued negotiation automatically correct.

## Step 5: Decide

The player can:

- **Buy now** at the current price.
- **Continue** into another round if patience remains.
- **Walk away** without buying.

The player is never forced to complete every available round. A strong dealer response or already-attractive price may make acceptance the best decision.

## Dealer patience

### Confirmed rule

The dealer has a visible patience meter. Negotiation consumes patience. At zero, the dealer becomes fed up and gives a final price.

The final price ends further bargaining. The player may still accept or walk away.

### Design purpose

Patience gives the interaction a finite shape. Without it, the player could grind toward the lowest price with no strategic cost.

It also supports dealer personality. A patient dealer can tolerate more discussion. An impatient dealer can produce a sharper, shorter exchange.

### Still to tune

- Whether patience falls every round, only after errors, or through both.
- The cost of an incorrect rebuttal.
- Whether excessive pressure consumes additional patience.
- Whether the final price is better or worse than the previous offer.
- Whether dealer patience resets when the player leaves and returns.

## Incorrect rebuttals

The exact consequence is not yet confirmed. A useful MVP prototype should test three options:

1. Lose patience but keep the current price.
2. Lose patience and skip the opportunity to press.
3. Trigger a small price hardening in addition to patience loss.

The result must be legible. The player should understand why the attempt failed and which fact would have been stronger, without the game feeling like an arbitrary quiz.

## Buying and selling symmetry

The same basic structure can support selling to a dealer:

- The dealer opens with a Cash offer.
- The dealer gives a reason for the valuation.
- The player selects a favorable fact about the owned watch.
- The player presses to push the offer upward.
- Dealer patience limits the number of rounds.
- The player accepts the current offer or keeps the watch.

The language changes, but the learned interaction remains useful.

## Screen hierarchy

The negotiation screen must keep these elements visible:

1. Watch identity and image.
2. Current price or offer.
3. Dealer claim or response.
4. Three rebuttal choices when active.
5. Press-and-hold control when active.
6. Dealer patience.
7. Buy/accept, continue, and walk-away actions.

The screen should reveal the cycle in stages rather than display every control at once.

## Feedback and tone

Feedback should come from the dealer as well as the meter:

- Expression or pose changes.
- Short voice or text reactions.
- Meter color and motion.
- Price movement.
- Patience loss.

The player should feel that they are pressuring a person, not filling an abstract bar disconnected from the conversation.

## Accessibility and mobile constraints

- Large press target suitable for one thumb.
- No required swipe.
- No essential information communicated only by color.
- Text responses short enough to compare without scrolling.
- Optional haptic feedback at useful meter thresholds.
- A forgiving release window.
- Reduced-motion behavior for animated pressure feedback.

## Success criteria for the prototype

The mechanic is working when:

- Players understand the cycle without a long tutorial.
- Watch facts influence choices.
- Players sometimes accept before patience reaches zero.
- Walking away feels like a valid decision.
- Dealers feel different without requiring entirely different rules.
- The press action adds tension but does not dominate the knowledge test.

## Open tuning

- Round count and patience values.
- Price reduction range per successful round.
- Press meter zones and consequences.
- Incorrect-response feedback.
- Dealer-specific modifiers.
- Whether a player can repeat a previously used fact.
- How negotiation difficulty scales with location and watch value.

