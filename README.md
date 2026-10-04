# Documentation add-in (`rulebook-docs`)

An Effortless **add-in seed** (kind `child`). It is mounted into an existing
Effortless project at `reference/` (not `docs/`: the root seeds already write their own `docs/`) and has no rulebook of its own: every step reads
the project's `../../effortless-rulebook/effortless-rulebook.json`.

## What the build produces

| Folder | From | What it is |
|---|---|---|
| `markdown/` | rulebook-to-markdown | Documentation of every table, field and rule |
| `rulespeak/` | rulebook-to-rulespeak | Business-readable RuleSpeak statements (Markdown + HTML) |
| `explainer-dag/` | rulebook-to-explainer-dag | Interactive dependency graph of every derived value (open `explainer-dag/rulebook-explainer-dag/pages/index.html`) |

All three are generated; change the rulebook and rebuild, never edit them.

## How it is used

Add it to a project from the Effortless catalog, or by hand:

```bash
effortless cloneSeed effortlessapi/erb-seed-rulebook-docs reference
rm -rf reference/.git
cd reference && effortless build
```

No questions, no credentials.
