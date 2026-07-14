# chats/

The `chats` directory contains locally stored conversations.

Its primary purpose is to preserve conversation history for the local user.

The contents of this directory are considered local working data.

## Purpose

Applications such as Akari CE MAY store complete conversations in this directory.

The specification does not require a particular internal structure or file format for `chats/`.

Applications MAY organize the directory according to their own requirements, provided that the stored conversations remain accessible to the local user.

## Synchronization

The `chats` directory is part of the AMTS Space.

When an AMTS Space is shared, published, or synchronized, the contents of `chats/` MUST NOT be included by default.

A purely local AMTS Space that is not shared, published, or synchronized does not require an exclusion mechanism.

For Git-based repositories, this is typically achieved using:

```gitignore
/chats/*
!/chats/.keep
```

The `.keep` file preserves the directory in the repository while all locally stored conversations remain excluded.

## Project association

Because the internal structure of `chats/` is not defined by AMTS, projects MUST NOT depend on a particular directory layout within `chats/`.

A project MAY associate local conversations or other local sources with itself through its `localreferences.md` file.

`localreferences.md` identifies the local resources relevant to a project without imposing any particular organization on the `chats/` directory.

## Shared references

If a conversation should become part of the synchronized project knowledge, it MAY be explicitly copied or exported into the corresponding project's `references/` directory.

Applications MUST NOT perform this action without explicit user intent.

The original locally stored conversation MAY remain in `chats/`.

## Agent behavior

Agents MAY use conversations stored in `chats/` as local context when access is available.

Agents MUST treat the contents of `chats/` as local working material.

Agents SHOULD use a project's `localreferences.md` file to identify locally stored conversations relevant to that project.

Agents MUST NOT copy content from `chats/` into a project's synchronized files or `references/` directory without explicit user instruction.
