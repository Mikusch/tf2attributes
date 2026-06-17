# tf2attributes

TF2Attributes SourceMod plugin

https://forums.alliedmods.net/showthread.php?t=210221

## Now featuring the following functionality from [nosoop/tf2attributes](https://github.com/nosoop/tf2attributes)

Add / remove temporary attributes on the player (using the game's own time-based expiry
mechanism for it).

```sourcepawn
// replicates the temporary health bonus granted by the Dalokohs Bar:
TF2Attrib_AddCustomPlayerAttribute(client, "hidden maxhealth non buffed", 50.0, 30.0);
```

Adds the game's "attribute hook" mechanism that collates values using an attribute class:

```sourcepawn
// computes the final damage multiplier based on the given item and owner's attributes:
float damageBonus = TF2Attrib_HookValueFloat(1.0, "mult_dmg", weapon);
```

## Installing or updating to 1.7

All plugins compiled for previous versions should continue to work with this one.
The installation instructions remain the same as before

1. Download all the non-source code files in [the latest release][].
2. Copy `tf2attributes.smx` to `addons/sourcemod/plugins/`.
3. Copy `tf2.attributes.txt` to `addons/sourcemod/gamedata/`.
4. If you're a developer, copy `tf2attributes.inc` to `addons/sourcemod/scripting/include/`
(or the appropriate path for your compiler toolchain / project).

[the latest release]: https://github.com/flaminsarge/tf2attributes/releases
