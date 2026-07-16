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

## Relationship to CURRENT.md

Context files describe stable knowledge and SHOULD change less frequently than `CURRENT.md`.

`CURRENT.md` describes recent changes, priorities, and matters requiring attention. It SHOULD NOT duplicate the stable information maintained in the context files.

Agents MUST read both shared context files before reading `CURRENT.md`, so that current information is interpreted within its stable context.
