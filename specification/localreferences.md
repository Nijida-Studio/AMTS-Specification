# localreferences.md

Each project contains a `localreferences.md` file.

This file identifies local resources that are relevant to the project but are not synchronized as part of the AMTS Space repository.

## Purpose

`localreferences.md` connects a project with locally available source material.

Typical local references include:

* conversations stored under `chats/`,
* local notes,
* local documents,
* application-specific resources,
* other material available only on the current installation.

AMTS does not define the internal structure of `chats/`.

For this reason, `localreferences.md` provides the project-specific association between a project and its relevant local conversations or other resources.

## Location

The file is located directly inside the corresponding project directory:

```text
projects/<Project>/localreferences.md
```

Each project maintains its own local references independently.

## Relationship to local context

`localcontext.md` and `projects/localcontext.md` contain structured local knowledge and conventions at Space and cross-project scope.

`projects/<Project>/localreferences.md` identifies local source material associated with one project.

Local path conventions that apply across projects SHOULD be recorded in `projects/localcontext.md` instead of being duplicated in each project's `localreferences.md`.

## Synchronization

When an AMTS Space is shared, published, or synchronized, project-specific `localreferences.md` files MUST NOT be included by default.

A purely local AMTS Space that is not shared, published, or synchronized does not require an exclusion mechanism.

When Git is used to share, publish, or synchronize an AMTS Space, project-specific `localreferences.md` files are typically excluded using:

```gitignore
/projects/*/localreferences.md
```

The template's `localreferences.md` under `specification/template/` remains versioned so that it is included when creating a new project.

After the template is copied, the resulting project's `localreferences.md` remains local.

## Content

The specification does not require a strict format for entries in `localreferences.md`.

Entries SHOULD be understandable to both users and agents.

A reference SHOULD identify:

* the local resource,
* its location or identifier,
* and, when useful, why it is relevant to the project.

Example:

```markdown
# Local References

- `../../chats/akari-ce/storage-discussion.md`
  Discussion about storing chats in an AMTS Space.

- `/Users/example/Documents/local-notes/akari-import.md`
  Local notes about the Akari CE import process.
```

Relative paths SHOULD be preferred when they remain valid within the local AMTS Space.

Absolute paths MAY be used when the referenced resource is located outside the Space.

## Agent behavior

Agents SHOULD consult `localreferences.md` when working on a project and when local resources are available.

Agents MUST NOT assume that a listed resource is synchronized or accessible to other users.

Agents MUST NOT copy, summarize, or transfer local reference material into synchronized project files unless the user requests or authorizes this action.

When a local resource should be preserved for all users of the project, it MAY be explicitly copied or exported into the project's `references/` directory.
