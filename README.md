# SPECKLE SERVER

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-architectural_design-lightgrey)

> Anticloud-hardened packaging of the upstream project `SPECKLE_SERVER` in category **ARCHITECTURAL DESIGN**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** ARCHITECTURAL DESIGN · **Upstream:** https://github.com/specklesystems/speckle-server · **Upstream pin:** `1690abaaaf3fc3e6a21b70a199e3cfa401997466` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<h1 align="center">
  <img src="https://user-images.githubusercontent.com/2679513/131189167-18ea5fe1-c578-47f6-9785-3748178e4312.png" width="150px"/><br/>
  Speckle | Server
</h1>

<p align="center"><a href="https://twitter.com/SpeckleSystems"><img src="https://img.shields.io/twitter/follow/SpeckleSystems?style=social" alt="Twitter Follow"></a> <a href="https://speckle.community"><img src="https://img.shields.io/discourse/users?server=https%3A%2F%2Fspeckle.community&amp;style=flat-square&amp;logo=discourse&amp;logoColor=white" alt="Community forum users"></a> <a href="https://speckle.systems"><img src="https://img.shields.io/badge/https://-speckle.systems-royalblue?style=flat-square" alt="website"></a> <a href="https://docs.speckle.systems/developers/server/introduction"><img src="https://img.shields.io/badge/docs-docs.speckle.systems-orange?style=flat-square&amp;logo=read-the-docs&amp;logoColor=white" alt="docs"></a></p>

> Speckle is the first AEC data hub that connects with your favorite AEC tools. Speckle exists to overcome the challenges of working in a fragmented industry where communication, creative workflows, and the exchange of data are often hindered by siloed software and processes. It is here to make the industry better.

<h3 align="center">
    Server and Web packages
</h3>

<p align="center">
<a href="https://codecov.io/gh/specklesystems/speckle-server">
<img src="https://codecov.io/gh/specklesystems/speckle-server/branch/master/graph/badge.svg" alt="codecov">
</a>
<a href="https://dl.circleci.com/status-badge/redirect/gh/specklesystems/speckle-server/tree/main">
<img src="https://dl.circleci.com/status-badge/img/gh/specklesystems/speckle-server/tree/main.svg?style=svg" alt="CircleCI">
</a>
</p>

# project structure

This monorepo is the home of the Speckle v2 web packages:

- [`packages/server`](https://github.com/specklesystems/speckle-server/blob/main/packages/server): the Server, a nodejs app.
- [`packages/frontend-2`](https://github.com/specklesystems/speckle-server/blob/main/packages/frontend-2): the Frontend, a Nuxt/Vue app.
- [`packages/viewer`](https://github.com/specklesystems/speckle-server/blob/main/packages/viewer): a threejs extension that allows you to display 3D data [![npm version](https://camo.githubusercontent.com/dc69232cc57b77de6554e752dd6dfc60ca0ecdfbe91bdfcbf7c7531a511ec200/68747470733a2f2f62616467652e667572792e696f2f6a732f253430737065636b6c652532467669657765722e737667)](https://www.npmjs.com/package/@speckle/viewer)
- [`packages/objectloader`](https://github.com/specklesystems/speckle-server/blob/main/packages/objectloader): a small js utility class that helps you stream an object and all its sub-components from the Speckle Server API. [![npm version](https://camo.githubusercontent.com/4d4f1e38ce50aaf11b4a3ad8e01ce3eaaa561dc5fd08febbae556f52f1d41097/68747470733a2f2f62616467652e667572792e696f2f6a732f253430737065636b6c652532466f626a6563746c6f616465722e737667)](https://www.npmjs.com/package/@speckle/objectloader)
- [`packages/preview-service`](https://github.com/specklesystems/speckle-server/blob/main/packages/preview-service): generates object previews for Speckle Objects headlessly. This package is meant to be called on by the server.
- [`packages/webhook-service`](https://github.com/specklesystems/speckle-server/tree/main/packages/webhook-service): making external webhook calls
- [`packages/fileimport-service`](https://github.com/specklesystems/speckle-server/tree/main/packages/fileimport-service): parsing and importing files

## Other projects

Make sure to also check and ⭐️ these other Speckle projects:

- [`speckle-sharp-connectors`](https://github.com/specklesystems/speckle-sharp-connectors): .NET connectors and desktop UI
- [`speckle-sharp-sdk`](https://github.com/specklesystems/speckle-sharp-sdk): .NET SDK, tests, and Objects
- [`specklepy`](https://github.com/specklesystems/specklepy): Python SDK 🐍
- [`speckle-sketchup`](https://github.com/specklesystems/speckle-sketchup): Sketchup connector
- [`speckle-excel`](https://github.com/specklesystems/speckle-excel): Excel connector
- [`speckle-unity`](https://github.com/specklesystems/speckle-unity): Unity 3D connector
- [`speckle-blender`](https://github.com/specklesystems/speckle-blender): Blender connector
- [`speckle-unreal`](https://github.com/specklesystems/speckle-unreal): Unreal Engine connector
- [`speckle-qgis`](https://github.com/specklesystems/speckle-qgis): QGIS connector
- [`speckle-powerbi`](https://github.com/specklesystems/speckle-powerbi): PowerBi connector
- and more [connectors & tooling](https://github.com/specklesystems/)!

# Developing and Debugging

Have you checked our [dev docs](https://docs.speckle.systems/developers/server/introduction)?

We have a detailed section on [deploying a Speckle server](https://docs.speckle.systems/developers/server/deployment-options). To get started with local development, see the [Local development environment](https://docs.speckle.systems/developers/server/development/setup) page.

## TL;DR;

We're using yarn and its workspaces functionalities to manage the monorepo.
Make sure you are using [Node](https://nodejs.org/en) version 22.
To get started, run:

1. `corepack enable`
1. `yarn`
1. `yarn build:public`
1. `yarn build`

After this, you can use the scripts in the individual packages or run them all in dev mode:

- `yarn dev`

For development you'll also want to run `yarn dev:docker:up` which will start up the docker containers you will need
to be able to run the apps on your machine.

## IDE

The suggested IDE for working in this project is VSCode, because the project has special configs to improve the DX there (auto-format & auto-lint, recommended extensions etc.).

This project relies on [VSCode multi-root workspaces](https://code.visualstudio.com/docs/editor/multi-root-workspaces), so for the best DX and proper formatting/linting make sure you open the project using the `workspace.code-workspace` file instead of just opening the folder in V

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Node.js / npm** (manifests: package.json, yarn.lock; scanned in UPSTREAM_CLONE)
- Top-level source layout: `packages/`, `setup/`, `test-queries/`, `tests/`, `utils/`
- Snapshot size: **3314 files**, **299018 lines of code** (measured; see Benchmarks)
- Primary languages: `.ts` (2032), `.vue` (729), `.js` (65), `.yml` (64), `.json` (56), `.png` (50)
- Upstream commit pinned for this packaging: `1690abaaaf3fc3e6a21b70a199e3cfa401997466`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
# from this project directory
npm install        # or: npm ci
npm run build      # if a build script is declared
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- `yarn dev`

For development you'll also want to run `yarn dev:docker:up` which will start up the docker containers you will need
to be able to run the apps on your machine.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

- [`packages/preview-service`](https://github.com/specklesystems/speckle-server/blob/main/packages/preview-service): generates object previews for Speckle Objects headlessly. This package is meant to be called on by the server.
- [`packages/webhook-service`](https://github.com/specklesystems/speckle-server/tree/main/packages/webhook-service): making external webhook calls
- [`packages/fileimport-service`](https://github.com/specklesystems/speckle-server/tree/main/packages/fileimport-service): parsing and importing files

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Node.js / npm |
| Manifests detected | package.json, yarn.lock |
| Files in snapshot | 3314 |
| Lines of code | 299018 |
| Dependency references | 664 |
| Dependencies by ecosystem | npm: 658, pypi: 6 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| npm | node-gyp | ^11.4.2 | package.json |
| npm | @eslint/config-inspector | ^0.4.10 | package.json |
| npm | @eslint/js | ^9.4.0 | package.json |
| npm | @rollup/plugin-typescript | ^11.1.0 | package.json |
| npm | @swc/core | ^1.2.222 | package.json |
| npm | @types/eslint | ^8.56.10 | package.json |
| npm | @types/eslint__js | ^8.42.3 | package.json |
| npm | @types/lockfile | ^1.0.2 | package.json |
| npm | commitizen | ^4.2.5 | package.json |
| npm | cross-env | ^7.0.3 | package.json |
| npm | cz-conventional-changelog | ^3.3.0 | package.json |
| npm | eslint | ^9.4.0 | package.json |
| npm | eslint-config-prettier | ^9.1.0 | package.json |
| npm | eslint-flat-config-utils | ^0.2.5 | package.json |
| npm | globals | ^15.4.0 | package.json |
| ... | (485 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- `package.json`

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Speckle Contribution Guidelines

## Introduction

Thank you for reading this! Speckle's a rather wide network of parts that depend on each other, either directly, indirectly or even just cosmetically.

> **Speckle** is a quite large ecosystem of moving parts. Any changes may have unintended effects, that can cause problems quickly for many people (and processes) that rely on Speckle.

This means that what might look like a simple quick change in one project may have a big hidden cost that propagates around other parts of the project. We're all here to help each other, and this guide is meant to help you get started and promote a framework that can untangle all these dependencies through discussion!

## Bugs & Issues 🐞

### Found a new bug?

- First step is to check whether this is a new bug! We encourage you to search through the issues of the project in question **and** associated projects!

- If you come up with nothing, **open a new issue with a clear title and description**, as much relevant information as possible: system configuration, code samples & steps to reproduce the problem.

- Can't mention this often enough: tells us how to reproduce the problem! We will ignore or flag as such issues without reproduction steps.

- Try to reference & note all potentially affected projects.

### Security vulnerabilities

For any security vulnerabilities or concerns, please contact us directly at security[at]speckle.systems.

### Sending a PR for Bug Fixes

You fixed something! Great! We hope you logged it first :) Make sure though that you've covered the lateral thinking needed for a bug report, as described above, also in your implementation! If there any tests, make sure they all pass. If there are none, it means they're missing - so add them!

## New Features 🎉

The golden rule is to Discuss First!

- Before embarking on adding a new feature, suggest it first as an issue with the `enhancement` label and/or title - this will allow relevant people to pitch in
- We'll now discuss your requirements and see how and if they fit within the Speckle ecosystem.
- The last step is to actually start writing code & submit a PR so we can follow along!
- All new features should, if and where possible, come with tests. We won't merge without!

> Many clients may potentially have overlapping scopes, some features might already be in dev somewhere else, or might have been postponed to the next major release due to api instability in that area. For example, adding a delete stream

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
Copyright (c) 2020-present AEC Systems.

Portions of this software are licensed as follows:

- All content residing under the "packages/server/modules/workspaces/" directory of this project is licensed under "The Speckle Enterprise Edition (EE) license".
- All content residing under the "packages/server/modules/gatekeeper/" directory of this project is licensed under "The Speckle Enterprise Edition (EE) license".
- Content outside of the above mentioned directories or restrictions above is available under the "Apache License" license as defined below.

                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

  TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

  1.  Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `SPECKLE_SERVER` (category: ARCHITECTURAL DESIGN)
- **Upstream URL:** https://github.com/specklesystems/speckle-server
- **Pinned commit (SHA):** `1690abaaaf3fc3e6a21b70a199e3cfa401997466`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`fb34146c1c00c08240ff4f0054453be73bdada5e64227df5b27d2a682d49d440`.

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

