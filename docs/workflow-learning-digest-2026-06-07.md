# Workflow Learning Digest - 2026-06-07

## Scope Reviewed

- First-parent git history for all 26 commits currently reachable on `main`, plus the current worktree diffs for workflow-learning artifacts: `AGENTS.md`, `.gitignore`, `docs/workflow-learning-digest-2026-06-06.md`, and the tracked `.DS_Store` deletion.
- Current repo guidance and user-facing surfaces: `AGENTS.md`, `docs/agent-workflow-learning.md`, `README.md`, `index.html`, `app-store-listing.md`, `privacy.html`, and `terms.html`.
- Live GitHub repo metadata for `Sedlacek-Solutions/insights-landing-page` and a recent-user-PR query; no user PRs were returned, so no PR review threads or review comments were available to inspect.
- No repo-local Codex/chat transcripts or issue export were present in this workspace.

## Findings

### `document`

- Add audit-hygiene guidance for repo-history summaries.
  Evidence: `docs/workflow-learning-digest-2026-06-06.md` said the repo had 24 commits, but `git rev-list --count --first-parent HEAD` and `git log --first-parent` show 26 commits through `9b17836`.
  Confidence: high.
  Risk: low.
  Action: updated `docs/agent-workflow-learning.md`.

- Revalidate the adjacency-sweep rule for workflow, platform, pricing, and legal-surface changes.
  Evidence: the current repo still spreads platform and workflow claims across `README.md`, `index.html`, `app-store-listing.md`, `privacy.html`, and `terms.html`, and the coordinated multi-file changes in `8c299a6`, `a54e4ee`, `c7a6546`, and `9b17836` remain the strongest lasting examples.
  Confidence: high.
  Risk: low.
  Action: no new doc change; the pending `AGENTS.md` update from the prior run still matches the evidence.

### `test`

- Keep the proposed no-dependency consistency check for product, App Store, and platform wording open.
  Evidence: `README.md` and `index.html` still describe the product as Mac-first or show iOS as coming soon, while `privacy.html` already describes Apple-platform usage more broadly.
  Confidence: medium.
  Risk: medium.
  Status: proposed only; not automated in this run.

### `component/helper`

- No durable helper extracted.
  Evidence: the static HTML still has repeated feature-tour patterns, but this run found no new maintenance bug pattern beyond the already-documented Safari/mobile verification needs.
  Confidence: medium.
  Risk: medium if over-abstracted.
  Status: ignore for now.

### `ignore`

- The current platform-positioning tension remains approval-bound rather than an automatic workflow fix.
  Evidence: `README.md` calls the site a macOS app, `app-store-listing.md` calls it Mac-first, `index.html` shows `iOS` as coming soon, and `privacy.html` already says the product runs on Apple platforms `(iOS and macOS)`.
  Confidence: high.
  Risk: high.
  Status: no direct change.

## Direct Updates Made

- Added an audit-hygiene rule to `docs/agent-workflow-learning.md` so future digests use a command-based commit count.
- Wrote `docs/workflow-learning-digest-2026-06-07.md`.
- No marketing copy, legal copy, screenshots, assets, publishing files, or browser-facing layout files were changed in this run.

## Proposed Follow-Ups

- Keep the wording-consistency check proposed; promote it only if cross-file drift repeats or if a safe read-only validator is clearly worth the maintenance cost.
- If a future run can access PRs, issues, or review comments for this repo, re-run the audit against that evidence before broadening any rules.
- Resolve the current Mac-first versus Apple-platform wording only with explicit human approval and a full sweep across `README.md`, `index.html`, `app-store-listing.md`, `privacy.html`, and `terms.html`.

## Confidence, Risk, Stale Rules, and Conflicts

- Active rules revalidated: static-site simplicity, real screenshot preservation, approval gates for positioning/pricing/legal/visual-direction changes, adjacency sweeps for workflow/platform/legal surfaces, and explicit Safari/narrow-screen verification for layout-affecting edits.
- Stale or corrected detail: the June 6 digest's manual commit count was inaccurate; the current first-parent history count is 26.
- Conflicts to watch: marketing surfaces remain Mac-first while the privacy page already uses broader Apple-platform language. That is still an approval-required cross-file decision, not a direct automation edit.
