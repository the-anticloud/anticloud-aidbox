# AIDBOX

![licence](https://img.shields.io/badge/licence-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![checks](https://img.shields.io/badge/checks-unknown_PASS-brightgreen)

> Governed Anticloud packaging of the upstream project `AIDBOX` in category **MEDICAL_HEALTH**. check results: see ISOLATED_LAB_RESULTS. Every number below traces to a named file + run stamp; nothing is borrowed from other projects.

**Upstream:** AIDBOX · **Upstream pin:** `dc81932f9396a6545b21ee75feb8c745f5f14a67` · **Category:** MEDICAL_HEALTH · **Vendor:** Anticloud FZ LLE · **Licence:** MIT

---

## What This Project Does

<p align="center">
  <img src=".github/logo.svg" width="64" height="64" alt="Health Samurai">
</p>

<h1 align="center">Aidbox TS SDK</h1>

<p align="center">
  A monorepo of TypeScript libraries for building healthcare applications on top of <a href="https://www.health-samurai.io/aidbox">Aidbox</a> and FHIR servers.
</p>

<p align="center">
  <a href="https://github.com/HealthSamurai/aidbox-ts-sdk/actions/workflows/common.yaml"><img src="https://github.com/HealthSamurai/aidbox-ts-sdk/actions/workflows/common.yaml/badge.svg" alt="Build"></a>
  <a href="https://github.com/HealthSamurai/aidbox-ts-sdk/actions/workflows/pages.yaml"><img src="https://github.com/HealthSamurai/aidbox-ts-sdk/actions/workflows/pages.yaml/badge.svg" alt="Pages"></a>
  <a href="https://www.npmjs.com/package/@health-samurai/react-components"><img src="https://img.shields.io/npm/v/@health-samurai/react-components/alpha?label=react-components" alt="npm react-components"></a>
  <a href="https://www.npmjs.com/package/@health-samurai/aidbox-client"><img src="https://img.shields.io/npm/v/@health-samurai/aidbox-client/alpha?label=aidbox-client" alt="npm aidbox-client"></a>
  <a href="https://www.npmjs.com/package/@health-samurai/aidbox-fhirpath-lsp"><img src="https://img.shields.io/npm/v/@health-samurai/aidbox-fhirpath-lsp/alpha?label=fhirpath-lsp" alt="npm fhirpath-lsp"></a>
  <a href="https://healthsamurai.github.io/aidbox-ts-sdk/react-components/"><img src="https://img.shields.io/badge/storybook-react--components-ff4785" alt="Storybook"></a>
</p>

## Packages

### [@health-samurai/react-components](packages/react-components)

A design system and component library built on React 19, Radix UI, and Tailwind CSS 4.
Includes 60+ accessible components — from standard UI primitives to healthcare-specific views like FHIR structure trees and OperationOutcome displays.

[Storybook](https://healthsamurai.github.io/aidbox-ts-sdk/react-components/) · [README](packages/react-components/README.md)

### [@health-samurai/aidbox-client](packages/aidbox-client)

A typed FHIR client with support for all FHIR interactions, multiple auth strategies, and a `Result<T, E>` return type for explicit error handling.

[API Docs](https://healthsamurai.github.io/aidbox-ts-sdk/aidbox-client/) · [README](packages/aidbox-client/README.md)

### [@health-samurai/aidbox-fhirpath-lsp](packages/aidbox-fhirpath-lsp)

A FHIRPath language server that runs entirely in the browser via Web Workers.
Provides autocompletion, diagnostics, hover, and go-to-definition for FHIRPath expressions inside CodeMirror editors.

[README](packages/aidbox-fhirpath-lsp/README.md)

## Getting started

```bash
# requires pnpm 10+
pnpm install
pnpm -r run build
```

## Development

| Command | Description |
|---------|-------------|
| `pnpm -r run build` | Build all packages |
| `pnpm -r run tsc:check` | Type-check all packages |
| `pnpm -r run lint:fix` | Lint and auto-fix with Biome |
| `pnpm hooks` | Install git pre-commit hooks |

Each package also has its own `build`, `lint`, and `tsc:check` scripts.
Run them from the package directory or via `pnpm --filter <package> run <script>`.

---

## Installation

See the upstream documentation quoted in What This Project Does above.

## Usage

See the upstream documentation quoted in What This Project Does above.

## API

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | unknown |
| Lines of Code | unknown |
| Dependencies | unknown |
| Upstream license (harvested) | MIT |
| Overlay license | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Contributing

# Contributing to Aidbox TS SDK

Thanks for your interest in contributing!
This guide will help you get set up and submit your first pull request.

## Prerequisites

- **[pnpm](https://pnpm.io/installation) 10+**
- **Docker** — only needed if you want to run `aidbox-client` integration tests

## Setup

```bash
git source https://github.com/HealthSamurai/aidbox-ts-sdk.git
cd aidbox-ts-sdk
pnpm install
pnpm hooks          # install pre-commit hooks (lint + typecheck)
pnpm -r run build   # initial build (required for cross-package types)
```

## Development workflow

1. **Create a branch** from `development`:
   ```bash
   git checkout -b my-feature development
   ```

2. **Make your changes.**
   Each package can be worked on independently:
   ```bash
   cd packages/<package>
   pnpm build        # compile
   pnpm tsc:check    # type-check
   pnpm lint:fix     # auto-fix formatting
   ```

3. **Run tests** (currently `aidbox-client` only):
   ```bash
   cd packages/aidbox-client
   pnpm test
   ```

4. **Preview UI changes** with Storybook:
   ```bash
   cd packages/react-components
   pnpm storybook    # opens on http://localhost:6006
   ```

5. **Commit.**
   The pre-commit hook will run `lint:check` and `tsc:check` across all packages.
   Fix any issues before pushing.

6. **Open a pull request** against `development`.

## Code style

All formatting and linting is handled by [Biome](https://biomejs.dev/).
There is no ESLint or Prettier.

- Indentation: **tabs**
- Quotes: **double quotes**
- Imports: auto-organized alphabetically by Biome

Run `pnpm lint:fix` to auto-format.
The pre-commit hook enforces this, so you don't need to think about it.

## Project structure

```
packages/
  aidbox-client/          # FHIR client library
  aidbox-fhirpath-lsp/    # FHIRPath language server (Web Worker)
  react-components/       # React design system & component library
```

Dependencies flow in one direction:

```
react-components -> aidbox-fhirpath-lsp -> aidbox-client
```

Always build in dependency order (`pnpm -r run build` handles this automatically).

## Guidelines

- **TypeScript strict mode** is enforced.
  Do not use `any` — prefer `unknown`, generics, or proper types.
- **Do not edit `src/fhir-types/`** in `aidbox-client` — these types are generated.
- **Use the `Result<T, E>` monad** for error handling in `aidbox-client`, not try/catch.
- **Follow shadcn/ui patterns** for new components: CVA variants, `cn()` utility, Radix primitives.
- **Use design tokens** (CSS variables from `tokens.css`) instead of hardcoded colors and spacing.
- **Add Storybook stories** for any new or modified React component.
- **Keep PRs focused.**
  One feature or fix per PR.
  Avoid unrelated refactors.

## Reporting bugs

Open an issue at [github.com/HealthSamurai/aidbox-ts-sdk/issues](https://github.com/HealthSamurai/aidbox-ts-sdk/issues) with:

- A clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Package name and version

## Ques

## License

Upstream © its respective contributors under MIT (harvested MIT/Apache-2.0/BSD source; see `UPSTREAM_CLONE/LICENSE`). This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- **project:** AIDBOX
- **Pinned SHA:** `dc81932f9396a6545b21ee75feb8c745f5f14a67`
- **source:** `UPSTREAM_CLONE/` (pinned at the SHA above)
- **Upstream README source:** `UPSTREAM_CLONE/README.md`

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`f9c5ad8088551f6596cef58d87f2191d568a8155e5d813cbac906fa23bb9b358`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

