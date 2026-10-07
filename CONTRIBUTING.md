<!--
SPDX-FileCopyrightText: 2026 SAP SE or an SAP affiliate company and Operational Context Graph contributors

SPDX-License-Identifier: Apache-2.0
-->

# Contributing

## Code of Conduct

All members of the project community must abide by the [SAP Open Source Code of Conduct](CODE_OF_CONDUCT.md).
Only by respecting each other we can develop a productive, collaborative community.
Instances of abusive, harassing, or otherwise unacceptable behavior may be reported by contacting [a project maintainer](REUSE.toml).

## Engaging in Our Project

We use GitHub to manage reviews of pull requests.

* If you are a new contributor, see: [Steps to Contribute](#steps-to-contribute)

* Before implementing your change, create an issue that describes the problem you would like to solve or the code that should be enhanced. Please note that you are willing to work on that issue.

* The team will review the issue and decide whether it should be implemented as a pull request. In that case, they will assign the issue to you. If the team decides against picking up the issue, the team will post a comment with an explanation.

## Steps to Contribute

Should you wish to work on an issue, please claim it first by commenting on the GitHub issue that you want to work on. This is to prevent duplicated efforts from other contributors on the same issue.

If you have questions about one of the issues, please comment on them, and one of the maintainers will clarify.

## Contributing Code or Documentation

You are welcome to contribute code in order to fix a bug or to implement a new feature that is logged as an issue.

The following rule governs code contributions:

* Contributions must be licensed under the [Apache 2.0 License](./LICENSE).
* Due to legal reasons, contributors will be asked to accept a Developer Certificate of Origin (DCO) when they create the first pull request to this project. This happens in an automated fashion during the submission process. This project uses [the standard DCO text of the Linux Foundation](https://developercertificate.org/).
* Contributions must follow our [guidelines on AI-generated code](CONTRIBUTING_USING_GENAI.md) in case you are using such tools. If you are using AI coding agents (e.g. Claude Code, OpenCode, Codex,), you must additionally follow the rules defined in `AGENTS.md` of the respective repository.

## Spec-Driven Development with OpenSpec

For non-trivial new components, this project uses [OpenSpec](https://github.com/Fission-AI/OpenSpec) to drive the work from a written spec: propose, then apply, then verify. The repositories ship a `/sdd-propose` skill that runs a failure-mode elicitation before the spec is generated, so edge cases surface before implementation starts.

**When to use.** Reach for spec-driven development when any one of these holds:

* Boundary conditions are non-obvious, such as concurrency, retry, partial failure, or ordering.
* The spec will be read as a design document, because it has multiple consumers, is security-relevant, or must be traceable.
* The contract is long-lived, because it will be extended, versioned, or depended on.
* Team standards must apply consistently across the component.

**When to avoid.** Skip it when all of these hold: the work is simple and well-bounded, it is short-lived or throwaway, and no downstream consumer needs the spec. A plain prompt plus a design review is enough, and the overhead of spec-driven development returns nothing here.

**How to store artifacts.** Commit `openspec/specs/` and `openspec/config.yaml`. Usage documentation, such as README and godoc, is still written by hand.

See [`repository-template`](https://github.com/operational-context-graph/repository-template) for the reference setup.

## Issues and Planning

* We use GitHub issues to track bugs and enhancement requests.

* Please provide as much context as possible when you open an issue. The information you provide must be comprehensive enough to reproduce that issue for the assignee.

## Verification

Run applicable project validation before requesting review.
Projects created from this template SHOULD document build, test, lint, security, and license commands.

Pull requests MUST report commands run, results, and checks not run.
