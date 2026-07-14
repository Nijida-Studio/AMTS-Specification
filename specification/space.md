# AMTS Space

An AMTS Space is a structured workspace for organizing projects, preserving knowledge, and storing conversations.

An AMTS Space is independent of any specific application. Applications such as Akari CE may use an AMTS Space, but do not define it.

## Root structure

An AMTS Space consists of the following top-level elements:

```text
AGENTS.md
CURRENT.md

chats/
projects/
specification/
```

Additional files and directories MAY be added when required by an application or project, provided they do not conflict with this specification.

## Purpose of the root elements

### AGENTS.md

The bootstrap entry point for agents and applications.

This file identifies the directory as an AMTS Space and instructs agents where to find the AMTS specification.

### CURRENT.md

Describes the current state of the AMTS Space.

It informs an agent about newly created projects, current priorities, or other information that should be considered before beginning work.

`CURRENT.md` is expected to change frequently.

### specification/

Contains the normative AMTS specification.

Agents MUST read this specification before working within an unknown AMTS Space.

### projects/

Contains all projects managed by this AMTS Space.

Each project is stored in its own subdirectory and follows the project structure defined by this specification.

### chats/

Contains locally stored conversations.

This directory is intended for personal conversation archives.

Applications SHOULD preserve the directory. When an AMTS Space is shared, published, or synchronized, its contents SHOULD be excluded as specified in `chats.md`.

## Synchronization control

When an AMTS Space is shared, published, or synchronized, the system used for that purpose SHOULD provide a mechanism for excluding local content as required by this specification.

The mechanism depends on the system. For example, a Git-based AMTS Space typically uses a `.gitignore` file to exclude local conversations under `chats/` and project-specific `localreferences.md` files.

A purely local AMTS Space that is not shared, published, or synchronized does not require a synchronization control file.

System-specific control files implement the synchronization requirements for local content. They do not define or modify the other requirements of an AMTS Space.

## Portability

An AMTS Space SHOULD remain portable between different operating systems and applications.

The specification defines the logical structure of the Space, but does not require a specific installation location or transport mechanism.

Examples include:

* local directories
* Git repositories
* archive files
* network storage
* cloud synchronization

## Compatibility

Applications MAY store additional application-specific data, provided that:

* the standard AMTS structure remains intact,
* project data remains accessible,
* and compatibility with other AMTS-compatible applications is preserved.
