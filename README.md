# MUME modules for Mudlet

## Installation

1) Save a module's .xml file somewhere.
2) Open Mudlet's Module Manager
3) Click "Install", choose the saved .xml file
4) (Optional) Set the priority and sync settings

## Overview

### Autoride, Autoassist and Autobash

- `leader <name>` Set the leader's name
- `aa` toggle Autoassist on/off
- `ar` toggle Autoride on/off
- `ab` toggle Autobas on/off

When toggled on, __Autoride__ will monitor when the leader dismounts/starts riding and mimicks them.

Similarly, __Autoassist__ will `assist` whenever your leader deals damage.

__Autobash__ monitors failed bashes and opponents recovering and bashes again. Doesn't handle multiple
opponents or anyone else bashing, but somewhat helpful while exping.

_NB! Triggers like these are not allowed in PK!_

Note that all of these modules add a `leader` alias, so you can remove the one you don't want

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

### MMapper door command aliases
- `op` = `_open`
- `cl` = `_close`
- `bl` = `_block`
- `ba` = `_bash`
- `br` = `_break`
- `ul` = `_unlock`
- `lo` = `_lock`
- `pi` = `_pick`
- `kn` = `_knock`
- `ro` = `_rock`

### Quick alias

The __quickalias__ system allows you to make single-character aliases on the fly.
Supported keys: `1..0` (above the letters) and all capital letters, e.g. `A`, but not `a`. You can use the pipe character (`|`) to separate commands. Also, the commands can themselves be other aliases, so you can do pretty much whatever you want.

- `A kill orc` sets the alias `A` as `kill orc`
- `qa` lists all defined quick aliases
- `qa clear` removes all defined quick aliases

### Modal input

Inspired from Vim's insert/normal mode, the __Modal__ system toggles between `INSERT` and `NORMAL` modes.

Toggling between modes: `CTRL + SPACE`.

The prompt is also prefixed with the current mode: `[INS] *# cW>` or `[NRM] *# cW>`

The __INSERT__ mode acts as a direct text input mode, just like you're used to.

The __NORMAL__ mode, however, takes over many letter keys and also supports quickaliases directly:
Obviously, these are my personal preferences and you can customize it however you want. Also, it uses the door aliases defined in the __mmapper__ module.

- `h, j, k, l, u, n` are the direction keys: `west, south, north, east, up, down`, respectively.
- `r` -> ride
- `d` -> lead
- Door management uses letter sequences instead of using modifier keys.
  - First you press the command key, followed by a direction key (same ones as defined above).
  - `q` -> `op`
  - `w` -> `cl`
  - `a` -> `ul`
  - `s` -> `lo`
  - `z` -> `pi`
  - `e` -> `scout`
  - `c` -> `ba`

  Examples:
  - `q h` -> `op west`
  - `e u` -> `scout up`
  - `z j` -> `pick south`
  - etc.
