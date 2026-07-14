# CURRENT.md

`CURRENT.md` describes the current state of an AMTS Space.

Its purpose is to help agents and users quickly identify what has changed since their last interaction with the Space and where attention is currently required.

Unlike the AMTS specification, `CURRENT.md` is expected to change frequently.

## Purpose

Typical information contained in `CURRENT.md` includes:

* projects that have changed since the last session,
* newly created projects,
* projects that require attention,
* short summaries of recent changes,
* recommendations about which project information should be re-read.

`CURRENT.md` is intended to help agents identify which projects require attention without re-reading the entire AMTS Space.

`CURRENT.md` should provide a concise overview rather than detailed project documentation.

## Scope

`CURRENT.md` applies to the entire AMTS Space.

Detailed project status belongs in the corresponding project directory.

`CURRENT.md` should only provide enough information to determine which projects should be revisited.

## Recommendations

`CURRENT.md` SHOULD be updated whenever significant changes occur within the AMTS Space.

Applications MAY update this file automatically if they can do so without losing user-provided information.

## Agent behavior

When entering an unfamiliar AMTS Space, an agent SHOULD:

1. Read the AMTS specification.
2. Read `CURRENT.md`.
3. Identify the relevant project(s).
4. Continue working using the project-specific information.

Agents SHOULD treat `CURRENT.md` as advisory information.

The authoritative project knowledge remains within the individual project directories.
