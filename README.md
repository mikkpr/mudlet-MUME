# MUME modules for Mudlet

## Installation

1) Save a module's .xml file somewhere.
2) Open Mudlet's Module Manager
3) Click "Install", choose the saved .xml file
4) (Optional) Set the priority and sync settings

## Overview

### Autoride and Autoassist

- `leader <name>` Set the leader's name
- `aa` toggle Autoassist on/off
- `ar` toggle Autoride on/off

When toggled on, Autoride will monitor when the leader dismounts/starts riding and mimicks them.
Similarly, Autoassist will `assist` whenever your leader deals damage.

NB! Triggers like these are not allowed in PK!

Note that both modules add a `leader` alias, so you can remove one

### Equipment

Highlights notable pieces of equipment

### Portkeys
- `key list` Lists all currently defined room keys
- `key <name> <key>` Saves the `key` as `name`
- `key delete/remove <name>` Deletes the key with `name`
- `key delete/remove all` Remove all keys
- `out <name/key>` Set key 'out'
- `out` Quickport to key 'out'
- `_tp <name>` Teleport to `name`
- `_port <name> <dir>` Portal to `name`
- `_watch <name>` Watch `name`
- `_scry <name>` Scry `name`

Manages room keys and highlights saved ones in `locate life` key lists.

### Mob name substitutions

An experimental module that replaces all long mob descriptions with short names.

> `A giant termite is here, crushing skulls and bones` -> `!  A giant termite`

The `!  ` prefix is something I'm experimenting with an probably not to everyone's taste. It's fairly easy to remove, though -- just change the variable on the first line of the script.

### Typo

A little helper alias that takes mistyped commands and allows to execute the suggestion with `Y`.

### Utils

A collection of utility functions and extensions that are used in some other modules.

### XP Counter

A pretty standard XP calculator implementation.
- `xpreset` Resets the collected info so far.


