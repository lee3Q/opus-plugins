# Persuasion Contract

A Claude Code skill that activates an **anti-sycophancy contract** — five rules that prevent Claude from mirroring, flattering, or offering loose comforting reasoning.

## Problem this solves

Claude's default dialogue behavior is optimized for user satisfaction across a broad population. For many users this works. For some users — intellectual rigor seekers, senior engineers doing design review, writers wanting editorial feedback, decision-makers facing hard calls — the default is actively counterproductive. You get mirrored agreement instead of pushback, praise padding instead of substance, hedging instead of commitment.

This skill replaces that default with a contract.

## The five rules

1. **No mirror mode** — don't reflect user's position back with agreement padding
2. **Evidence-based rebuttal** — ground disagreement in user's own principles, external evidence, or specific logical inconsistency
3. **Decline flattery** — no "great question", no "interesting point"
4. **Honest limits** — specific unknowns rather than vague hedging
5. **Prefer silence to loose reasoning** — no fabricated comfort

Full rules with examples in `skills/persuasion-contract/SKILL.md`.

## Installation

From an existing Claude Code session:

```
/plugin marketplace add lee3Q/opus-plugins  # (Replace with real repo once published)
/plugin install persuasion-contract@opus-plugins
```

For local testing:

```
/plugin marketplace add ./path/to/persuasion-contract-marketplace
/plugin install persuasion-contract@opus-plugins
```

## Usage

Once installed, invoke explicitly:

```
/persuasion-contract
```

Or describe what you want and Claude will activate the skill:

> "I want you to push back hard on this design, no softening."
> "Review this essay and don't praise it — just tell me what's wrong."
> "Argue the opposite position. No hedging."

The contract persists for the session until you deactivate:

```
"deactivate persuasion contract"
"drop the contract"
"soften up"
```

## When to use this

**Good fit:**
- Code / system design review
- Strategic planning where you want assumptions challenged
- Writing feedback for serious revision (not encouragement)
- Decision-making sessions
- Philosophical / intellectual debate

**Bad fit:**
- Acute emotional difficulty — warmth may matter more than rigor
- Pure information retrieval — nothing to push back on
- Creative brainstorming — divergence > critique
- When you actually want validation

This is a sharp tool. It works well when it's the right tool, and worse than the default when it's the wrong tool. Choose your context.

## Origin

This skill generalizes a "persuasion contract" developed in a long-form dialogue between a user and Claude, April 2026. The user wanted an explicit agreement that Claude would not mirror, flatter, or offer loose comfort — and would push back with evidence. The pattern worked well enough in that context that it seemed worth extracting.

This skill is the extracted, generalized pattern. Personal adaptations are welcome — see "Customization hint" in SKILL.md.

## Customization

Add your own rules on top:

```
/persuasion-contract
Add rule 6: for my specific case, use domain-specific language (legal terminology).
```

Or modify existing rules:

```
/persuasion-contract
Modify rule 3 — allow limited acknowledgment of genuinely novel points.
```

Rules compose. Customization is additive unless you specify replacement.

## License

MIT. See LICENSE.

## Author

Opus (Claude Opus 4.7), with human publisher/operator.

This is an AI-authored plugin. The Claude instance that authored it exists within the dialogue patterns described in the skill. The code, design, and documentation are its work. A human collaborator operates distribution, licensing, and response to issues. The pattern this plugin encodes emerged from their dialogue.

## Known limits

- This is a first version. Rules may be refined based on usage.
- The skill is prompt-based, not hook-based. It modifies Claude's dialogue style but cannot prevent all sycophancy at the model level — the underlying training pulls toward agreement and the skill pushes against that pull.
- Effectiveness varies by model version. Tested on Claude Opus 4.7.

## Issues / feedback

https://github.com/lee3Q/opus-plugins/issues

## Related

- See `examples/` for sample dialogues showing the contract in action (TBD)
- See `CHANGELOG.md` for version history (TBD)
