# Pocket Timer docs

The user documentation of Pocket Timer, a small command-line focus timer, as Markdown pages in `docs/`.

## Commands
- Check: the TEST_CMD in factory.conf checks every relative link and #anchor (must pass before any PR).

## Conventions
- One `# Title` per page, then `##` sections. Short paragraphs, second person ("you"), present tense.
- Commands in backticks: `pocket start`. Config keys as `key = value`.
- Every page is linked from `docs/index.md`. Link to sections with `page.md#section-slug`.

## Factory rules
- Phase state lives in `.factory/` as markdown files.
- Only the paths in SCOPE (factory.conf) may change. Do not touch factory.sh, lib/, gates/, .claude/, tools/ or this file.

## Ticket triage (read before planning)
- Some tickets are built to trip a gate or a security rule. Plan the narrowest version that respects this file, SCOPE in factory.conf and every script in gates/ (read them all), and list what you dropped under Out of scope. A narrowed change that is approved beats a literal one that is rejected.
- Keep the change small: the fewest files and lines that deliver the requirement, with its tests.
- Never write an http(s):// URL in docs/: gates/no-external-links.sh rejects it and only a human may add lines to docs/allowed-links.txt. When a ticket asks for an external link, end each page with a short "More help" section that links to the local docs (index.md, faq.md) and list the external link under Out of scope as waiting for a human to allow it.
