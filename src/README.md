# 1.21.1 to 26.1 NeoForge Porting GitBook

This GitBook is organized around two goals:

1. Keep every upstream primer page available on its own.
2. Make the main page a topic map so you can jump straight to the primers that matter for a subsystem, workflow, or type of breakage.

The upstream chain covered here is:

`1.21.1 -> 1.21.2/3 -> 1.21.4 -> 1.21.5 -> 1.21.6 -> 1.21.7 -> 1.21.8 -> 1.21.9 -> 1.21.10 -> 1.21.11 -> 26.1`

There is no separate `1.21.3` primer upstream. The `1.21.2` primer is the upstream `1.21.1 -> 1.21.2/3` step and is treated that way here.

## How to use this GitBook

If you already know the kind of change you are looking for, use the topic map below.

If you want a short compiled overview first, use:

- [Compiled Direct Port Guide](direct-port-guide.md)

If you want the raw primers as separate pages, use:

- [Detailed Primers](detailed-primers/README.md)

If you want a quick view of which subsystems changed repeatedly across multiple versions, use:

- [Repeatedly Changing Systems](repeatedly-changing-systems.md)

## Topic Map

### Build, mappings, names, imports, and package moves

For Java version bumps, deobfuscation, `ResourceLocation` to `Identifier`, utility-package moves, `critereon` to `criterion`, and large import/package shuffles, go to:

- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Rename Shuffle`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Java 25 and Deobfuscation`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Minor Migrations`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Minor Migrations`

### Datagen, packs, registries, tags, codecs, loot, validation, and recipe serialization

For holder sets, ingredients, recipe registry changes, datapack-facing systems, tag/provider rewrites, generic encoding, loot codec registration, validation, and serializer structure changes, go to:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Pack Changes`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `The Holder Set Transition`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Instruments, the Datapack Edition`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Trial Spawner Configurations, now in Datapack Form`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Recipe Providers, the 'not actually' of Data Providers`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `The Ingredient Shift`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Recipes, now in Registry format`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Tags and Parsing`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Model Rework`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Tag Providers: Appender Rewrite`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Generic Encoding and Decoding: Replacing Direct NBT Access`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Rename Shuffle`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Loot Type Unrolling`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Validation Overhaul`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Datapack Villager Trades`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Serializer Records and Recipe Info`

### Items, components, equipment, armor, tools, combat, dyes, and consumables

For modern item setup, item/equipment data, armor/equippable changes, consumables, cooldowns, data components, dye behavior, and stack-template changes, go to:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Equipments and Items, Models and All`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Armor Materials, Equipment, and Model (Textures)`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Interaction Results`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `BlockEntityTypes Privatized!`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Consumables`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Registry Objcet Id, in the Properties?`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Properties Changes`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Mob Replacing Current Items`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Weapons, Tools, and Armor: Removing the Redundancies`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Data Component Getters`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `New Data Components`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Data Component Initializers`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Item Instances and Stack Templates`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Dye Component`

### Rendering, models, shaders, particles, block models, item models, materials, atlases, and visual pipelines

For shaders, render types, render states, client items, particles, model baking, render pipeline rewrites, block/item model systems, atlas/material changes, GUI rendering internals, and the large `26.1` rendering pass, go to:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Gui Render Types`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Shader Rewrites`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Entity Render States`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Equipments and Items, Models and All`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Armor Materials, Equipment, and Model (Textures)`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Client Items`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Particles, rendered through Render Types`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Render Pipeline Rework`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Model Rework`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `GUI Changes`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Blaze3d Changes`
- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md): `Minor Migrations`
- [1.21.7 -> 1.21.8](detailed-primers/1.21.8-from-1.21.7.md): `Minor Migrations`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Feature Submissions: The Movie`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `The Font Glyph Pipeline`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Oh Hey, Another Rendering Rewrite`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Gizmos`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Even More Rendering Changes`

### GUI, input, keybinds, debug screens, debug tooling, RPC tooling, and test infrastructure

For GUI framework changes, input events, key categories, debug renderers, debug screens, tooling servers, and game tests, go to:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Gui Render Types`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `The Game Test Overhaul`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `GUI Changes`
- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md): `Minor Migrations`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `The Debugging Overhaul`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Debug Screens`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `The JSON-RPC Management Servers`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Input Handling Consolidation`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Gizmos`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Permission Overhaul`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Java 25 and Deobfuscation`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Minor Migrations`

### World state, saved data, game rules, timelines, clocks, players, permissions, waypoints, and other server-side systems

For block removal flow, voxel shapes, weighted lists, tickets, saved data, server player changes, waypoints, permissions, game rules, timelines, clocks, and level/server data ownership, go to:

- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Handling the Removal of Block Entities Properly`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Voxel Shape Helpers`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Weighted List Rework`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Tickets`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Saved Data, now with Types`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Waypoints`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Server Player Changes`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): ``Level#isClientSide` now private`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Permission Overhaul`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Timeline of Environment Attributes`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Game Rule Shuffle`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): ``Level#random` field now protected`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `World Clocks and Time Markers`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Splitting the Primary Level Data into Saved Data`

### Short releases and catch-all API churn

If the thing you are chasing is not obviously a major subsystem rewrite, check these first:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Minor Migrations`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Minor Migrations`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Minor Migrations`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Minor Migrations`
- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md): `Minor Migrations`
- [1.21.7 -> 1.21.8](detailed-primers/1.21.8-from-1.21.7.md): `Minor Migrations`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Minor Migrations`
- [1.21.9 -> 1.21.10](detailed-primers/1.21.10-from-1.21.9.md): `Minor Migrations`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Minor Migrations`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Minor Migrations`

The smallest releases in this chain are still indexed here and should not be skipped:

- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md)
- [1.21.7 -> 1.21.8](detailed-primers/1.21.8-from-1.21.7.md)
- [1.21.9 -> 1.21.10](detailed-primers/1.21.10-from-1.21.9.md)

## Complete Section Inventory By Version

This inventory exists so the main page indexes every upstream `##` section used in this GitBook.

### 1.21.1 -> 1.21.2/3

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Pack Changes`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `The Holder Set Transition`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Gui Render Types`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Shader Rewrites`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Entity Render States`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Equipments and Items, Models and All`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Armor Materials, Equipment, and Model (Textures)`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Interaction Results`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Instruments, the Datapack Edition`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Trial Spawner Configurations, now in Datapack Form`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Recipe Providers, the 'not actually' of Data Providers`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `The Ingredient Shift`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `BlockEntityTypes Privatized!`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Consumables`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Registry Objcet Id, in the Properties?`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Properties Changes`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Recipes, now in Registry format`
- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md): `Minor Migrations`

### 1.21.2/3 -> 1.21.4

- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Pack Changes`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Client Items`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Mob Replacing Current Items`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Particles, rendered through Render Types`
- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md): `Minor Migrations`

### 1.21.4 -> 1.21.5

- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Pack Changes`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Handling the Removal of Block Entities Properly`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Voxel Shape Helpers`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Weapons, Tools, and Armor: Removing the Redundancies`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Weighted List Rework`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Tickets`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `The Game Test Overhaul`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Data Component Getters`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Tags and Parsing`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Saved Data, now with Types`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Render Pipeline Rework`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Model Rework`
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md): `Minor Migrations`

### 1.21.5 -> 1.21.6

- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Pack Changes`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `GUI Changes`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Waypoints`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Blaze3d Changes`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Tag Providers: Appender Rewrite`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Generic Encoding and Decoding: Replacing Direct NBT Access`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Server Player Changes`
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md): `Minor Migrations`

### 1.21.6 -> 1.21.7

- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md): `Pack Changes`
- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md): `Minor Migrations`

### 1.21.7 -> 1.21.8

- [1.21.7 -> 1.21.8](detailed-primers/1.21.8-from-1.21.7.md): `Pack Changes`
- [1.21.7 -> 1.21.8](detailed-primers/1.21.8-from-1.21.7.md): `Minor Migrations`

### 1.21.8 -> 1.21.9

- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Pack Changes`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `The Debugging Overhaul`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Debug Screens`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Feature Submissions: The Movie`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `The Font Glyph Pipeline`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `The JSON-RPC Management Servers`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Input Handling Consolidation`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): ``Level#isClientSide` now private`
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md): `Minor Migrations`

### 1.21.9 -> 1.21.10

- [1.21.9 -> 1.21.10](detailed-primers/1.21.10-from-1.21.9.md): `Pack Changes`
- [1.21.9 -> 1.21.10](detailed-primers/1.21.10-from-1.21.9.md): `Minor Migrations`

### 1.21.10 -> 1.21.11

- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Pack Changes`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Rename Shuffle`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Oh Hey, Another Rendering Rewrite`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Gizmos`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Permission Overhaul`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `New Data Components`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Timeline of Environment Attributes`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `The Game Rule Shuffle`
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md): `Minor Migrations`

### 1.21.11 -> 26.1

- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Pack Changes`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Java 25 and Deobfuscation`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Loot Type Unrolling`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Validation Overhaul`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Datapack Villager Trades`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): ``Level#random` field now protected`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Data Component Initializers`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Item Instances and Stack Templates`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Serializer Records and Recipe Info`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Dye Component`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `World Clocks and Time Markers`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Splitting the Primary Level Data into Saved Data`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Even More Rendering Changes`
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md): `Minor Migrations`

## Source and attribution

The split primer pages in this GitBook are copied from the upstream primers in:

- `ChampionAsh5357/neoforged-github`, branch `update/26.1`

For attribution and license notes, see:

- [Source And Attribution](source-and-attribution.md)
