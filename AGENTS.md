# Agent instructions for APES Digital Software

Cursor's user rules and skills set how work is done here (branches, issues, pull requests, merge, release, deploy, ship gate, decisions and safety). This file describes this repository and fills the named slots below. If anything here disagrees with them, Cursor's rules win and this file is corrected in the same milestone.

Cursor/agent layout standard: https://github.com/apescic-director/Cursor/blob/main/docs/cursor-agent-standards.md

The owner is Bambie Murphy. Write UK English (organisation, behaviour, colour, licence) in the product, docs, issues and pull requests. Never print, paste or commit secrets.

## About the app

APES Digital Software is the planned license and entitlement engine for APES CIC software products. The public NPO Software storefront (`APESCIC/APES-NPO-Software-Website`) is expected to call this service for entitlements and license keys after paid orders (see issue #1).

- Repository: `APESCIC/APES.Digital.Software`. Work only in this repository.
- Current tree: placeholder only (`README.md`). There is no application code, `composer.json`, `package.json`, CI workflows, or Cloudron app yet.

## Stack and architecture

Not implemented yet. When the app is scaffolded, record the real stack here (likely PHP/Laravel on Cloudron LAMP to match sibling APES apps, unless Bambie decides otherwise). Keep durable folder and API facts in this file as they land.

## Local development and preview

| Item | Value |
| --- | --- |
| Clone | `C:\Users\BambieMurphy\Documents\GitHub\APES.Digital.Software` |
| Herd site | None yet (create and link when app code exists) |
| Preview URL | None — live preview gate is skipped until a local site exists |
| Preview command | None |
| HMR port | None |
| Env file | None yet (use `.env.example` with key names only when added) |
| Database | None |
| Mail | None |

Laravel Herd is the only supported local stack for PHP, Laravel or static sites once this repo has them. Use Herd's PHP, Composer and Node for the site. Use fake demo data only — never real personal, customer, license or production data. Do not document Laragon as current practice.

### Local development with Laravel Herd

When a Herd site exists: run `herd site:info` for the URL, PHP version and services; use `herd php` and `herd composer` so commands use this site's PHP; use `herd status` if something does not respond.

## Tests and checks

| Check | Command |
| --- | --- |
| Tests | None yet |
| Lint / format | None yet |
| CI workflows | None yet (`.github/workflows/` when added) |

## Workflow slots

Shipping follows Cursor's `github-milestone-completion` and `ship-gate` skills. This repo fills these slots:

| Slot | Value |
| --- | --- |
| Milestone branch pattern | `milestone/vX-Y-Z-<slug>` (confirm when first versioned milestone opens) |
| Version files | None yet |
| Release tooling | None yet |
| Area labels | None; use type prefixes in titles |
| Issue title prefix | `[Type] Short title` |

Development is tracked only in GitHub issues, sub-issues and `vMAJOR.MINOR.PATCH` milestones — never Linear.

### Milestone shipping

1. Complete **all** of a milestone's issues on its milestone branch before the next stage.
2. One merge into `main` as a merge commit (never squash).
3. One release (tag and GitHub Release) for that version.
4. One deploy of that release tag (when a deploy target exists).

Nothing reaches `main`, and nothing is tagged, released or deployed, before stage 2. Hotfixes only with Bambie's written approval on the issue.

An issue is done when its acceptance criteria are met and committed on the milestone branch; it closes when the milestone PR merges. A milestone is done only after the merge, release and a verified deploy (or after merge alone while this repo has no deploy target).

## Deploy and health

| Item | Value |
| --- | --- |
| Target | Not deployed yet |
| Cloudron app ID | None |
| Domain | None |
| Deploy command | None |
| Deploys | The release tag (never a branch), once deploy exists |
| Auto-deploy couplings | none |
| Health URL | None |
| Version field | None |
| Secrets live in | APES Vault (Bitwarden) — never commit secrets |

## Decisions and gotchas

- 2026-11-16: Repository is still a placeholder. Agent config scaffolded to the APES Cursor/agent standard before application code exists.
- Planned ownership: license/entitlement API for the NPO Software storefront (issue #1). Fill Herd, Cloudron and version slots when the first app milestone lands.

## Where to find things

- README: [README.md](README.md)
- Related storefront: `APESCIC/APES-NPO-Software-Website`
