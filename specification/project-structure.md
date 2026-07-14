# Project Structure

Each project within an AMTS Space is stored as a separate subdirectory under `projects/`.

Projects SHOULD follow the standard structure defined by this specification.

The template under `specification/template/` is the normative reference implementation for creating new projects.

## Standard project structure

Although this document describes the structure of individual project directories (`projects/<Project>/`), the normative project template is located in the AMTS Space root directory under:

```text
specification/template/
```

Applications SHOULD create new projects by copying this template and adapting it to the new project's requirements.

## Purpose of the files

### AGENTS.md

A human-readable introduction to the project.

### index.md

The extended entry point into the project's documentation.

It provides an overview of additional information, outside of the specification.

### CONTEXT.md

Describes the overall purpose, scope, and current understanding of the project.

This document should remain relatively stable over time.

### principles.md

Contains long-term principles and conventions governing the project.

### current-work.md

Describes the current focus of development, active work, and immediate next steps.

This document is expected to change frequently.

### decisions.md

Contains the project's active decisions.
A decision represents agreed work that should be carried out.
Once a decision has been fully implemented, it SHOULD be removed from this file.
Supporting discussions and background information MAY be preserved in references/.

### glossary.md

Defines project-specific terminology.

### localreferences.md

Lists local resources associated with the project.

Typical examples include:

- conversations stored under `chats/`,
- local notes,
- local documents,
- or other local source material.

The structure of `chats/` is intentionally not defined by AMTS.

`localreferences.md` allows each project to identify the local resources relevant to that project without requiring a particular organization of the local chat archive.

This file is intended to remain local to each installation.

When using Git to share, publish, or synchronize an AMTS Space, project-specific `localreferences.md` files SHOULD be excluded from version control. The template's `localreferences.md` under `specification/template/` remains part of the repository.

### references/

Contains source material intentionally preserved as part of the project.

Typical examples include selected conversations, meeting notes, documents, or other primary sources that should remain available to all collaborators.

## Synchronization

When an AMTS Space is shared, published, or synchronized, its projects SHOULD be included, except that each project's `localreferences.md` file is intended to remain local to its installation and SHOULD NOT be included.

A purely local AMTS Space that is not shared, published, or synchronized does not require an exclusion mechanism.

When Git is used to share, publish, or synchronize an AMTS Space, this is typically achieved by ignoring all project-specific `localreferences.md` files. The template file under `specification/template/` is not project-specific and remains under version control.

Project-specific local conversations remain stored in `chats/`.
