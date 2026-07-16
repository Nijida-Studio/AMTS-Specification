# projects/

The `projects` directory contains all projects managed within an AMTS Space.

Each project is stored in its own subdirectory.

Projects are independent from each other while sharing the same AMTS Space and specification.

## Purpose

Projects organize all long-term knowledge related to a specific topic, application, repository, or area of work.

Typical examples include:

* software projects,
* documentation projects,
* research topics,
* specifications,
* organizational knowledge.

Each project maintains its own:

* agent instructions
* index
* context
* principles
* current work
* active decisions
* glossary
* local references
* shared references

## Project directories

Each subdirectory of `projects` represents exactly one project.

Project names SHOULD be stable and descriptive.

The structure of a project is defined separately in `project-structure.md`.

## Cross-project context

The `projects` directory also contains files that apply across projects:

```text
projects/CONTEXT.md
projects/localcontext.md (optional)
```

`projects/CONTEXT.md` contains shared cross-project knowledge and conventions.

`projects/localcontext.md` contains installation-specific cross-project knowledge and conventions. It MUST NOT be synchronized by default.

These files are not projects and do not change the rule that every subdirectory of `projects` represents one project.

## Project template

The normative reference implementation for creating new AMTS projects is located at:

```text
specification/template/
```

Applications SHOULD create new projects by copying this template into a new subdirectory of `projects/` and adapting it to the new project.

The project template SHOULD remain unchanged except when the AMTS specification itself evolves.

## Agent behavior

When working on a project, agents SHOULD:

1. read the shared cross-project context and any available local cross-project context,
2. identify the appropriate project,
3. read its project files,
4. follow the project-specific conventions,
5. update project documentation as work progresses.

Agents SHOULD avoid creating duplicate projects when an appropriate project already exists.
