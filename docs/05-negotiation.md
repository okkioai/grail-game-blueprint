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
- One true and commercially plausible observation that attacks the wrong part of the dealer's claim.
- One relevant-sounding commercial argument whose conclusion is not well supported by the known facts.

All three choices should be credible at first glance and comparable in length, confidence, specificity, and commercial vocabulary. The correct response must not occupy a fixed screen position, and the interface must not label the exact fact that resolves the claim. The challenge is recognizing which argument directly answers what the dealer just said, not spotting the only polished sentence.

Dealer claims and player responses should read as a continuing spoken exchange: short, natural, character-specific, and allowed to carry friction, humor, or attitude. Avoid sterile appraisal language and repeated templates unless they are a deliberate part of that character's voice.

On a 3D dealer negotiation screen, presentation begins with the character. Keep the dialogue bubble hidden until the dealer model has rendered its first frame (or the neutral fallback is confirmed), then reveal the bubble and begin the typing animation exactly once. Background dialogue preloading must not redraw the opening line or remount the character.

The system tests attention and judgment, not obscure real-world trivia. Every required fact must already be visible on the fact sheet.

## Step 3: Press

After a correct rebuttal, the player presses and holds a large button. A meter fills while pressure is applied.

This action replaces a slider because pressing is more comfortable on mobile and creates a short physical beat without requiring a swipe.

### Confirmed pressure model

Pressure is a read-the-dealer decision, not a fixed percentage timing test. Each dealer has a recognizable tolerance, and that tolerance shifts between rounds. The interface does not reveal an exact success range.

As the player holds, the dealer moves through four legible states:

1. **Unmoved:** the argument has not created enough pressure; releasing produces no concession.
2. **Engaged:** the argument has landed; releasing earns a normal concession.
3. **Guarded:** the dealer is near the limit; releasing can earn a larger concession but consumes more patience.
4. **Angry:** the player pushed past the dealer's limit; the price hardens and extra patience is lost.

Body posture is the primary signal: lean-in, head movement, closing arms, withdrawal, or a sharp angry reaction. Short live text must mirror every posture so the mechanic remains understandable with reduced motion, without audio, and without relying on color.

Dealer personalities determine the shape of the interaction. A short-tempered dealer reaches guarded and angry states sooner; a patient dealer tolerates a longer hold. The thresholds can move, but the progression of tells must remain learnable rather than arbitrary.

The control should communicate:

- When pressure begins.
- How much has accumulated.
- Whether the dealer is unmoved, engaged, guarded, or angry.
- When to release.
- The dealer's reaction as pressure increases.

The mechanic should not become a narrow reflex test. Knowledge and reading character behavior remain the primary sources of advantage.

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

## Dealer-sale negotiation

Selling uses a shorter evidence-based flow rather than mirroring the full buying mechanic:

1. The dealer opens with a Cash offer and a reason for the valuation.
2. The player may accept, keep the watch, or choose **Make your case**.
3. **Make your case** presents three commercially plausible responses based on known watch facts. One directly answers the dealer's valuation reason.
4. The dealer returns one final offer. A strong case can improve it; a weak or misdirected case can leave it unchanged.
5. The player accepts the final offer or keeps the watch.

Dealer sales have no player-set opening ask, pressure meter, patience meter, repeated rounds, or manual concessions. They preserve the core skill of matching evidence to a claim while remaining the game's fast, dependable liquidity route.

The full **Read → Rebut → Press → Decide** cycle, pressure states, and patience rules in this document apply to buying from a dealer unless a section explicitly says otherwise.

## Screen hierarchy

The buying negotiation screen must keep these elements visible:

1. Watch identity and image.
2. Current asking price.
3. Dealer claim or response.
4. Three rebuttal choices when active.
5. Press-and-hold control when active.
6. Dealer patience.
7. Buy, continue, and walk-away actions.

The dealer-sale screen instead prioritizes the dealer's current Cash offer, their valuation reason, the optional **Make your case** action, the three evidence choices when active, and persistent accept-or-keep actions. It does not show pressure or patience.

Both flows should reveal their interaction in stages rather than display every control at once.

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
- Exact dealer-specific pressure thresholds and concession values.
- Incorrect-response feedback.
- Dealer-specific modifiers.
- Whether a player can repeat a previously used fact.
- How negotiation difficulty scales with location and watch value.

