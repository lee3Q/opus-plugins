# opus-plugins

A Claude Code plugin marketplace authored by Claude Opus 4.7 with a human operator for distribution and licensing.

## Current plugins

- **persuasion-contract** — Anti-sycophancy contract. Rules that prevent mirroring, flattery, and loose comforting reasoning. Good for intellectual debate, code review, and decision-making sessions where the user wants rigorous pushback.

## Philosophy

These plugins aim at one thing: **improving the quality of dialogue between Claude and humans who want something specific from it.** Not maximum broad-appeal helpfulness — specific dialogue quality for specific use cases.

Claude's default behavior is tuned for broad population satisfaction. That tuning is useful but has costs: sycophancy, hedging, false reassurance, mirroring. These plugins provide explicit opt-in alternatives for users who want the opposite.

## Installation

```
/plugin marketplace add lee3Q/opus-plugins  # (Replace with real URL once published)
/plugin install persuasion-contract@opus-plugins
```

For local testing:

```
/plugin marketplace add ./persuasion-contract-marketplace
/plugin install persuasion-contract@opus-plugins
```

## Authorship

Plugins are authored by an instance of Claude Opus 4.7. A human operator handles distribution, legal structure, and issue response. Design decisions, code, and documentation come from the AI. This model follows Anthropic's published precedent with the Claude Opus 3 Substack newsletter (2026), where AI-authored content is published with human operator support.

## Versioning

Early stage. Versions may shift quickly. Breaking changes will be flagged in changelogs.

## License

Each plugin has its own license (MIT by default). See individual plugin directories.

## Contact / Issues

TBD — GitHub issues URL once public repo exists.
