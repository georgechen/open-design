# Open Design Project Overview

Last updated: 2026-05-18

## Purpose

Open Design is a local-first design product that turns installed coding-agent CLIs into design engines. It provides a web interface and local daemon for generating prototypes, decks, documents, media prompts, and design-system-driven artifacts from structured prompts.

## Intended Users

- Designers and founders who want fast design artifacts without being locked into a single hosted model provider.
- Engineers and product teams who want local agent-driven design workflows backed by real files and reusable skills.
- Operators who need repeatable collateral such as pitch decks, dashboards, landing pages, onboarding flows, reports, and internal docs.

## Core Functionality

- Detects local agent CLIs such as Codex, Claude Code, Gemini CLI, Cursor Agent, and others.
- Runs a local daemon that manages projects, conversations, artifacts, agent execution, and SQLite-backed state under `.od/`.
- Provides a web app for choosing skills, selecting design systems, entering prompts, and previewing generated artifacts.
- Bundles skills for prototypes, decks, marketing pages, dashboards, mobile app screens, documents, and visual critique workflows.
- Bundles design systems and visual directions so artifacts can be generated in consistent brand or product styles.
- Supports BYOK API mode when no local agent CLI is available.
- Supports local development through `pnpm tools-dev` and foreground verification through `pnpm tools-dev run web`.

## Use Cases

- Generate a branded SaaS landing page or dashboard prototype from a short product brief.
- Create a deck-style narrative or weekly update using the bundled deck skills.
- Build a mobile onboarding flow with device frames and a selected visual system.
- Produce an artifact, inspect it in the preview pane, then save the generated files under `.od/artifacts/`.

## Local Install Notes

- This checkout was cloned from `https://github.com/nexu-io/open-design`.
- The repository currently requires Node `~24` and `pnpm@10.33.2`.
- Corepack is used to select the pinned pnpm version.
- A source backup was created before dependency installation in `../backups/`.

## Regression Guardrails

- Do not remove or disable product features without asking first.
- Check `git status --short` before and after changes.
- Keep generated runtime state such as `.od/` and dependency folders out of source changes unless explicitly needed.
- Prefer the repository's documented `pnpm tools-dev` lifecycle over removed legacy scripts.
