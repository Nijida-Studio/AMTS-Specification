# AMTS Version

The AMTS version implemented by this specification is **1.10**.

## Purpose

This file identifies the version implemented by all files in the current
`specification/` directory.

Agents and applications MUST read this file before the remaining specification
files. They MUST NOT infer the installed AMTS version from remembered behavior,
individual directory elements, or the version of an application using the
Space.

## Authoritative source

The public AMTS specification is maintained at:

<https://github.com/Nijida-Studio/AMTS-Specification>

The version published by that repository is declared in its
`specification/VERSION.md` file.

The specification embedded in the current AMTS Space remains authoritative for
that Space until an update has been explicitly requested and fully applied. The
existence of a newer published version does not by itself modify the Space.

## Updating an AMTS Space

When a user requests an update to the latest AMTS version, an agent or
application SHOULD:

1. read the installed version from this file,
2. consult the public AMTS specification and determine its declared version,
3. review the changes between the installed and published versions,
4. update the embedded specification and every affected Space or project
   structure without discarding Space-specific content,
5. verify that all required migrations have been completed,
6. and update this file to the new version only after the migration succeeds.

An update MUST preserve local context, conversations, project knowledge, and
application-specific additions unless the newer specification explicitly
requires a conflicting element to be migrated.

## Version 1.10

AMTS 1.10 introduces `specification/VERSION.md` as the explicit declaration of
the specification version embedded in an AMTS Space and documents how that
version is compared with the public AMTS specification during an explicitly
requested update.
