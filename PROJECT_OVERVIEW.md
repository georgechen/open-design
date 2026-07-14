# Project Overview

Last updated: 2026-04-28

## Purpose

Open Design is a local-first design artifact workspace. It lets a coding agent generate design outputs from structured skills, design system files, and a local project folder, then previews and exports those outputs through a browser UI.

## Core Functionality

- Runs a Vite and React web app for prompts, previews, file workspace access, and export actions.
- Runs a local Node and Express daemon for project storage, agent detection, chat streaming, files, and exports.
- Detects installed agent CLIs, including Codex CLI, Claude Code, Cursor Agent, Gemini CLI, OpenCode, and Qwen Code.
- Stores local runtime state in `.od/`, including SQLite app data, artifacts, and per-project working folders.
- Loads bundled `SKILL.md` design workflows and Markdown `DESIGN.md` design systems.
- Renders generated artifacts in a sandboxed iframe and supports HTML, PDF, ZIP, and skill-defined export flows.

## Features

- 19 bundled skills for web prototypes, SaaS landing pages, dashboards, pricing pages, docs pages, blog posts, mobile app screens, decks, and document-style work products.
- 71 bundled product-style design systems with color, typography, spacing, layout, component, motion, voice, and brand guidance.
- Interactive discovery forms intended to lock down audience, tone, brand context, surface, scale, and constraints before generation.
- Local file-backed artifacts that can be inspected, edited, archived, or exported.
- Agent-agnostic architecture where the local daemon launches the selected CLI from the generated project folder.

## Intended Users

- Product designers who want agent-generated prototypes without using a closed design product.
- PMs and founders who need fast decks, landing pages, specs, or product visuals.
- Engineers who want generated design artifacts to live on disk and remain reviewable.
- Teams evaluating local-first agent workflows with interchangeable model or CLI backends.

## Example Use Cases

- Generate a marketing landing page using a specific product design system and export the resulting HTML.
- Create a quick dashboard prototype with dense KPI views and iterate directly in the generated files.
- Produce a simple pitch deck or magazine-style web deck from a structured brief.
- Draft operational documents such as PM specs, runbooks, weekly updates, or OKR summaries from reusable templates.

## Local Install Notes

- Installed in this workspace with `npm install` because `pnpm` was not present.
- Codex CLI is available on this Mac and can be used as an Open Design agent backend.
- A source backup archive was created in the parent workspace `backups/` folder before runtime verification.
