# Agent Workflow Learning

This document defines how the nightly workflow-learning automation should improve this repository's agent instructions, docs, checklists, and automation.

## Purpose

Extract durable lessons from work history without turning one-off copy or visual choices into permanent rules. The automation should make future landing-page work faster, safer, and more consistent while preserving human approval for product positioning and design direction.

## Inputs

Inspect this repository independently from other projects.

- Codex/chat history related to the Insights landing page
- every commit
- pull requests, issues, and review comments when available
- local docs, `AGENTS.md`, `README.md`, page files, assets, and publishing notes

## Finding Types

Classify every candidate as one of these actions.

- `document`: add or refine agent guidance, workflow docs, or review checklist items
- `automate`: propose or add checks for objective rules
- `test`: propose or add lightweight validation for links, markup, accessibility, or visual regressions
- `component/helper`: propose reusable HTML/CSS patterns when repetition is real
- `ignore`: record as one-off, campaign-specific, or too subjective to preserve

## Evidence Standard

Every lasting rule needs evidence. Prefer exact references.

- user correction or explicit preference
- repeated chat pattern
- bug/regression fix
- commit hash or PR/review link
- file path and behavior changed
- task that took materially longer because the workflow was unclear

Single-example findings start as narrow candidate guidance. Broaden only after repeated evidence.

## Risk Gates

The automation may directly update low-risk materials:

- `AGENTS.md`
- this document
- static workflow notes
- review checklist docs

The automation must ask for approval or create a proposed issue for:

- product positioning or headline changes
- pricing, App Store, privacy, or terms copy
- broad visual direction changes
- replacing screenshots or App Store assets
- adding frameworks, analytics, external scripts, package managers, or build steps
- publishing or DNS changes

## Landing Page-Specific Heuristics

- Keep the page static unless the user explicitly asks for tooling.
- Treat real product screenshots and App Store assets as first-class source material.
- When copy has already broadened platform positioning, verify metadata and adjacent pages stay consistent.
- Prefer small HTML/CSS updates over introducing dependencies.
- Use browser or screenshot verification for layout-affecting changes, especially sticky feature sections and mobile breakpoints.

## Conflict Handling

If a candidate conflicts with existing guidance, do not silently overwrite either rule. Create a digest item that names the conflict and asks for a decision.

Examples:

- Mac-first positioning vs iPhone/iPad support
- static site simplicity vs richer interactive validation
- real product screenshots vs generated or illustrative imagery
- concise marketing copy vs complete App Store metadata coverage

## Revalidation

Review durable rules periodically.

- `active`: still supported by current work
- `stale`: no longer seen or no longer relevant
- `conflicted`: newer guidance disagrees
- `promote`: repeated evidence supports making the rule stronger
- `demote`: the rule was overbroad or noisy

## Nightly Output

Produce a repo-local digest with:

- new findings grouped by action type
- evidence for each finding
- risk level and confidence
- direct updates made
- proposed issues or approval-needed changes
- stale or conflicting rules to review

Low-risk docs updates may be committed directly. Larger follow-up work should be left as a proposed issue or patch.
