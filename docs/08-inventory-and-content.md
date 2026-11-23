# Inventory, watches, and content

[← Blueprint index](../README.md)

## Inventory as strategy

### Confirmed rule

The player begins with **six watch slots**.

Every owned watch occupies one slot and ties up Cash. A full box prevents another acquisition until the player sells a watch or expands capacity.

The limitation is not administrative clutter. It creates the question: **does this opportunity deserve one of my slots?**

## Watch box requirements

Each occupied slot should make the watch commercially legible:

- Watch image and family.
- Acquisition cost.
- Current estimated range, if available.
- Condition.
- Completeness.
- Major configuration.
- Location or source of acquisition.
- Marketplace offer status.
- Dealer sale entry point.

The screen must also make empty slots obvious and explain how capacity expands.

## Watch album

### Confirmed rule

The Watch Box has two views: **Inventory** and **Album**.

Inventory shows the watches the player owns now. Album shows every watch model available in the current game catalog.

- Every model name and family identity is visible from the start.
- A model's watch image remains absent until the player has owned that model at least once.
- First ownership permanently reveals the image in the Album.
- Selling or transferring the last owned instance does not hide the image again.
- Album discovery does not occupy inventory slots and does not imply current ownership.
- Revealed Album cards may flip to show short brand and model-history notes; only one card is open at a time. Undiscovered model pockets are inert.

This makes acquiring a model meaningful beyond the immediate trade without changing inventory capacity or watch authority.

## Full-inventory behavior

When the box is full:

- A new purchase cannot complete.
- Cash must not leave the account.
- An auction win must not be possible unless capacity was validated before bidding.
- The player should be directed toward selling, declining, or expanding.

The warning should appear before the final commitment, not as a surprise afterward.

## Capacity progression

Reputation can unlock larger watch boxes as permanent progression. Gold can also purchase permanent watch-space expansion.

The free path must remain credible. Gold is an acceleration option, not the only practical way to continue dealing.

Expansion should be paced so that inventory remains a meaningful constraint at higher levels. Whether Gold purchases individual slots or staged box upgrades remains open.

## MVP catalog size

The launch target is approximately **six to ten recognizable watch families**.

The exact count remains flexible until art, writing, and balance costs are better understood. The MVP does not need hundreds of models if a smaller set can produce meaningful commercial variety.

## Catalog identity and watch instances

### Confirmed rule

The server catalog separates three stable identities:

- **Brand** is the maker-level identity and owns shared history.
- **Reference** is a collectible watch model. Album discovery, marketplace criteria, model history, and the current single catalog image attach here.
- **Instance** is one actual watch in the economy. Its condition, completeness, configuration, known facts, provenance, ownership, and transaction history are independent of the reference.

Multiple instances may point to the same reference without becoming the same watch. A reference may exist in the Album before any instance of it exists in the live economy.

For the initial catalog pass, each reference has one transparent product image stored in versioned object storage. Replacing an image publishes a new object version rather than overwriting the object used by an existing build or report.

## Variation axes

Each watch family can vary through three primary dimensions.

### Condition

Examples:

- Cosmetic wear.
- Damage.
- Service state.
- Originality or replacement of visible parts.

Condition changes valuation and produces facts that can support a negotiation.

### Completeness

Examples:

- Box.
- Papers.
- Accessories.
- Service documentation.
- Provenance material.

Completeness creates understandable value differences within the same family.

### Major configuration

Examples:

- Dial.
- Bezel.
- Metal.
- Bracelet.
- Size.

The MVP should select one major configuration axis per marketplace target rather than exposing an overwhelming specification builder.

## Watch facts

Facts connect authored content to mechanics. A fact may:

- Weaken a dealer's asking-price claim.
- Strengthen the player's sale argument.
- Change projected resale value.
- Affect dealer specialty.
- Determine marketplace matching.

Every fact used in a negotiation must be visible before the player chooses a rebuttal.

### Fact-writing guidelines

- Use plain language first; expert terminology can follow when helpful.
- Connect the fact to commercial meaning.
- Avoid facts that are technically true but impossible to interpret in context.
- Do not require outside research to identify the intended answer.
- Keep the sentence short enough for mobile comparison.

## Suggested watch data model

| Field | Purpose |
|---|---|
| Family/model | Primary identity and marketplace target |
| Condition tier | Valuation and negotiation input |
| Completeness | Valuation and matching input |
| Major configuration | Demand and matching input |
| Known facts | Negotiation content |
| Base value range | Economy reference |
| Dealer affinities | Specialist behavior |
| Acquisition cost | Player profit calculation |
| Ownership state | Inventory and marketplace authority |

This is a product model, not a final backend schema.

## Dealer content

Each dealer needs enough authored material to stay recognizable across repeated visits:

- Character introduction.
- Short backstory fragments.
- Specialty explanation.
- Multiple opening lines.
- Claims supporting higher prices.
- Responses to correct and incorrect rebuttals.
- Low-patience and final-price reactions.
- Purchase-offer language for specialist and non-specialist watches.

Content should be modular so the same mechanical state can support several lines without changing balance.

## Visual presentation

The established direction uses:

- Dark charcoal surfaces.
- Warm off-white typography.
- Muted secondary information.
- Restrained gold accents.
- Tactile editorial watch imagery.
- Confident display type and compact system labels.

Wireframes may remain grayscale, but they should reserve hierarchy for the final brand system.

## Content production priorities

For the MVP, depth is more valuable than breadth. A smaller catalog should still provide:

- Clear price ladders.
- Several condition outcomes.
- Different completeness levels.
- Distinct marketplace demand.
- Facts suitable for buying and selling negotiations.
- Dealer specialties that overlap without becoming identical.

## Open tuning

- Final launch families.
- Number of variations per family.
- Value ranges and rarity weights.
- Which facts appear on each watch state.
- Reputation thresholds for larger boxes.
- Gold cost of permanent capacity.
- Whether Gold purchases individual slots or staged box upgrades, and the maximum capacity.
- How additional configuration images should extend the one-image-per-reference baseline.

