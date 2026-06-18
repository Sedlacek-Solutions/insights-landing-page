# AGENTS.md

## Task Completion Requirements

1. Keep the landing page static: no framework, package manager, build step, or tracking script unless explicitly requested.
2. Preserve the product positioning and App Store links in `README.md`, `index.html`, `app-store-listing.md`, `privacy.html`, and `terms.html`.
3. For visual changes, verify the page in a browser-sized viewport and confirm text does not overlap or hide important screenshots.
4. Do not replace real product screenshots with generic stock-like imagery.
5. Record skipped visual or browser verification in the final task summary.
6. When adding or removing workflows, integrations, pricing or credit surfaces, or platform availability, sweep `README.md`, `app-store-listing.md`, `privacy.html`, and `terms.html` in the same pass, or explicitly note why a file did not need changes.
7. Treat Safari and narrow-screen behavior as required visual checks for layout-affecting updates, especially sticky header states, `details` menus, screenshot expansion, and card stacking.

## Workflow Learning

- Use `docs/agent-workflow-learning.md` when extracting durable lessons from chats, commits, PRs, issues, review comments, or repeated task friction.
- Low-risk documentation/checklist updates may be applied directly when supported by concrete evidence.
- Product positioning, launch copy, pricing, App Store metadata, and visual direction must remain proposed changes unless the user explicitly approves the update.
