# references/

The `references` directory contains source material intentionally preserved as part of a project.

Unlike `localreferences.md`, the contents of `references/` are part of the shared project knowledge and are synchronized with the AMTS Space repository.

## Purpose

The purpose of `references/` is to preserve original source material that provides important context for the project.

Typical examples include:

* selected conversations,
* meeting notes,
* design discussions,
* specifications,
* research documents,
* external documentation,
* or other primary sources.

These references complement the structured project documentation but do not replace it.

## Relationship to local references

Projects distinguish between two kinds of references:

* `localreferences.md` identifies local resources available only on the current installation.
* `references/` contains resources intentionally preserved as part of the project.

Material SHOULD only be moved or copied from local resources into `references/` when there is a conscious decision to make that information part of the project's long-term knowledge.

## Synchronization

The contents of `references/` are intended to be synchronized as part of the AMTS Space.

Applications SHOULD preserve the original files whenever practical.

## Organization

AMTS does not require a specific internal structure for the `references` directory.

Projects MAY organize references in whatever manner best suits their needs.

## Agent behavior

Agents MAY consult material contained in `references/` when additional context is required.

The authoritative project documentation remains the project's structured files, such as:

* `CONTEXT.md`
* `principles.md`
* `decisions.md`
* `current-work.md`

References provide supporting evidence and historical context but SHOULD NOT replace structured project documentation.

When creating or updating project documentation, agents SHOULD derive concise, structured information from relevant references rather than duplicating their contents.
