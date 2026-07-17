# CONTEXT.md

AMTS defines shared context at two scopes:

* `CONTEXT.md` contains stable context for the entire AMTS Space.
* `projects/CONTEXT.md` contains stable context that applies across the projects in the Space.

Both files are part of the shared AMTS Space and are intended to be synchronized.

## Space context

The file at the root of the Space is located at:

```text
CONTEXT.md
```

It contains knowledge and conventions that apply to the Space as a whole.

Typical information includes:

* the purpose and scope of the Space,
* shared working conventions,
* stable information about the working environment,
* general knowledge that helps users and agents interpret the Space.

Information in this file SHOULD be relevant independently of any particular project.

## Cross-project context

The file within the projects directory is located at:

```text
projects/CONTEXT.md
```

It contains knowledge and conventions that apply across multiple or all projects but do not apply to the entire Space.

Typical information includes:

* relationships between projects,
* conventions shared by all projects,
* common repository or development practices,
* boundaries and responsibilities spanning multiple projects.

Information that applies to only one project belongs in that project's documentation.

## Team working model

A team MAY describe how it works through the existing context and project
files. AMTS does not require a particular methodology or a separate team file.

When a team follows a defined method, framework, or internal process, the
description SHOULD identify:

* the method, framework, or process,
* its applicable version when relevant,
* how the team applies it and any intentional deviations,
* responsibilities and decision practices,
* and the locations of normative and supporting resources.

Working conventions for the entire Space belong in root `CONTEXT.md`.
Conventions shared across projects belong in `projects/CONTEXT.md`.
Information specific to one project belongs in that project's `CONTEXT.md` and
`principles.md` files.

Shared source material MAY be preserved in the relevant project's
`references/` directory. Resources required by all collaborators SHOULD NOT be
recorded only in `localreferences.md`, because that file is local to one
installation and is not synchronized by default.

## Relationship to CURRENT.md

Context files describe stable knowledge and SHOULD change less frequently than `CURRENT.md`.

`CURRENT.md` describes recent changes, priorities, and matters requiring attention. It SHOULD NOT duplicate the stable information maintained in the context files.

Agents MUST read both shared context files before reading `CURRENT.md`, so that current information is interpreted within its stable context.
