# Workflow Learning Digest - 2026-06-06

## Scope Reviewed

- Git history for all 24 commits in this repo, with extra review of commits tied to Safari/mobile fixes, legal and metadata expansion, branding, pricing, CNAME churn, and the latest subscriptions/GitHub workflow launch.
- Current local docs and page surfaces: `AGENTS.md`, `docs/agent-workflow-learning.md`, `README.md`, `index.html`, `app-store-listing.md`, `privacy.html`, `terms.html`, and `CNAME`.
- GitHub connector metadata for `Sedlacek-Solutions/insights-landing-page`; no recent user PRs were returned, so no PR review threads or review comments were available to inspect.
- No relevant repo-local Codex/chat transcripts were present in this workspace.

## Findings

### `document`

- Add an adjacency-sweep rule for workflow and platform changes.
  Evidence: `8c299a6`, `a54e4ee`, `9b17836`, and `c7a6546` each changed `README.md`, `app-store-listing.md`, `index.html`, `privacy.html`, and `terms.html` together or in tight coordination.
  Confidence: high.
  Risk: low.
  Action: added to `AGENTS.md`.

- Promote Safari and narrow-screen verification from a generic visual check to an explicit recurring checklist.
  Evidence: `5423c0c`, `52837e8`, `d47ae67`, and `c1a0780` were all follow-up fixes for mobile navigation, screenshot expansion, cursor fallback, or card stacking.
  Confidence: high.
  Risk: low.
  Action: added to `AGENTS.md`.

### `automate`

- Ignore Finder metadata in git and remove the tracked Finder artifact already in the repo.
  Evidence: `9bb70d3` accidentally introduced a tracked `.DS_Store` while only intending a hero subtitle edit.
  Confidence: high.
  Risk: low.
  Action: added `.gitignore` with `.DS_Store` and removed the tracked `.DS_Store`.

### `test`

- Proposed: add a no-dependency consistency check for the App Store ID, product name, and platform wording across `README.md`, `index.html`, `app-store-listing.md`, `privacy.html`, and `terms.html`.
  Evidence: the same surfaces moved together during branding and workflow expansions in `8c299a6`, `a54e4ee`, `c7a6546`, and `9b17836`.
  Confidence: medium.
  Risk: medium.
  Status: proposed only; not added in this run.

- Proposed: add a lightweight manual smoke checklist for sticky header, `details` menus, feature screenshot expansion, and narrow-width card stacking.
  Evidence: the Safari/mobile follow-up sequence in `5423c0c`, `52837e8`, `d47ae67`, and `c1a0780`.
  Confidence: high.
  Risk: low.
  Status: covered in `AGENTS.md` guidance, but no separate checklist file or browser automation was added in this run.

### `component/helper`

- No durable helper extracted.
  Evidence: repeated feature-tour markup exists in `index.html`, but the repo intentionally stays static and dependency-free, and the repetition has not yet produced a clear maintenance bug pattern on its own.
  Confidence: medium.
  Risk: medium if over-abstracted.
  Status: ignore for now.

### `ignore`

- Hero messaging broadening and product-positioning changes remain approval-bound.
  Evidence: `1de01c5` and `9bb70d3` changed headline or subtitle direction, and current repo guidance already requires human approval for positioning or launch-copy updates.
  Confidence: high.
  Risk: high.
  Status: no direct change.

- Pricing, subscriptions, credits, privacy, and terms copy remain approval-bound despite repeated edits.
  Evidence: `4af024c`, `7d78761`, and `9b17836` changed pricing, credits, privacy, or terms scope.
  Confidence: high.
  Risk: high.
  Status: no direct change.

- Publishing and DNS changes remain approval-bound and should stay out of automatic direct edits.
  Evidence: `60850a7`, `5050de4`, `2e6bd04`, and `86e6488` show same-night CNAME churn without broader workflow context.
  Confidence: medium.
  Risk: high.
  Status: existing rule in `docs/agent-workflow-learning.md` already covers this; no new instruction added.

## Direct Updates Made

- Updated `AGENTS.md` with an explicit adjacency sweep for workflow/platform/legal metadata changes.
- Updated `AGENTS.md` with Safari and narrow-screen verification targets for layout-affecting edits.
- Added `.gitignore` to ignore `.DS_Store`.
- Removed the tracked `.DS_Store` file so the ignore rule takes effect for future work.

## Proposed Follow-Ups

- Add a small local validation script or documented command that checks App Store link and product-name consistency across the landing page, legal pages, and App Store copy.
- If future Safari/mobile fixes continue, promote the manual smoke list into a dedicated checklist document or browser automation.
- If a future run can access PRs or issues, re-check whether review comments reveal additional durable rules beyond commit history.

## Confidence, Risk, and Rule Status

- Active rules strengthened this run: adjacency sweep for workflow/legal surfaces; explicit Safari/mobile verification targets.
- Active rules unchanged: static-site simplicity, real screenshot preservation, approval gates for positioning, pricing, App Store metadata, legal copy, publishing, DNS, and visual direction.
- Stale rules: none found.
- Conflicts to watch: current repo copy is still Mac-first in `README.md`, `app-store-listing.md`, schema metadata, and CTAs, while `privacy.html` already describes Apple-platform usage more broadly. That is not a direct contradiction yet, but any future iPhone or iPad launch positioning should be treated as an approval-required cross-file sweep.
