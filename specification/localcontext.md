# localcontext.md

AMTS supports optional local context at two scopes:

* `localcontext.md` contains local context for the entire AMTS Space.
* `projects/localcontext.md` contains local context that applies across the projects in the Space.

These files describe the current installation and are not part of the shared AMTS knowledge.

## Space-local context

The optional file at the root of the Space is located at:

```text
localcontext.md
```

Typical information includes:

* local storage and synchronization locations,
* symbolic links to external directories,
* machine-specific tools or environment conventions,
* local resources relevant to the Space as a whole.

## Cross-project local context

The optional file within the projects directory is located at:

```text
projects/localcontext.md
```

Typical information includes:

* a common local root directory for repositories,
* symbolic links or equivalent paths used by all projects,
* machine-specific conventions shared across projects,
* local knowledge that prevents duplicate or incorrect project paths.

Information that applies to only one project belongs in that project's `localreferences.md` or other project documentation, as appropriate.

## Synchronization

When an AMTS Space is shared, published, or synchronized, local context files MUST NOT be included by default.

For Git-based repositories, this is typically achieved using:

```gitignore
/localcontext.md
/projects/localcontext.md
```

A purely local AMTS Space that is not shared, published, or synchronized does not require an exclusion mechanism.

## Agent behavior

Agents MUST read each local context file when it exists and MUST NOT assume that it is available to other installations.

Local context MUST be read after the corresponding shared context and before `CURRENT.md`.

Agents MUST NOT copy local context into synchronized files unless the user requests or authorizes that action.
