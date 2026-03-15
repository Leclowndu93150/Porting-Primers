# Repeatedly Changing Systems

This page is the guard rail for the direct port.

When the same subsystem changed in multiple intermediate versions, do not treat the earliest migration note as final. Use the latest applicable version as the source of truth, but still apply the older chapter first so the intermediate API transitions make sense.

## Rendering and graphics

Relevant sections:

- [Gui Render Types](detailed-primers/1.21.2-from-1.21.1.md#gui-render-types) (1.21.2)
- [Shader Rewrites](detailed-primers/1.21.2-from-1.21.1.md#shader-rewrites) (1.21.2)
- [Entity Render States](detailed-primers/1.21.2-from-1.21.1.md#entity-render-states) (1.21.2)
- [Render Pipeline Rework](detailed-primers/1.21.5-from-1.21.4.md#render-pipeline-rework) (1.21.5)
- [Model Rework](detailed-primers/1.21.5-from-1.21.4.md#model-rework) (1.21.5)
- [GUI Changes](detailed-primers/1.21.6-from-1.21.5.md#gui-changes) (1.21.6)
- [Blaze3d Changes](detailed-primers/1.21.6-from-1.21.5.md#blaze3d-changes) (1.21.6)
- [Minor Migrations](detailed-primers/1.21.7-from-1.21.6.md#minor-migrations) (1.21.7)
- [Feature Submissions: The Movie](detailed-primers/1.21.9-from-1.21.8.md#feature-submissions-the-movie) (1.21.9)
- [The Font Glyph Pipeline](detailed-primers/1.21.9-from-1.21.8.md#the-font-glyph-pipeline) (1.21.9)
- [Oh Hey, Another Rendering Rewrite](detailed-primers/1.21.11-from-1.21.10.md#oh-hey-another-rendering-rewrite) (1.21.11)
- [Even More Rendering Changes](detailed-primers/26.1-from-1.21.11.md#even-more-rendering-changes) (26.1)

How to read them:

- `1.21.2/3` changes GUI blits, shader JSON structure, and render-state assumptions.
- `1.21.5` is the first large rendering infrastructure rewrite around `RenderPipeline`, `GpuTexture`, and render passes.
- `1.21.6` changes GUI rendering flow again through prepare/render state separation.
- `1.21.9` changes how features are submitted for rendering.
- `1.21.11` changes samplers, render types, terrain split, and atlases.
- `26.1` is the final authority for block/item rendering, materials, tint sources, fluid models, particle layers, and backend-facing rendering APIs.

Practical rule:

- Treat `26.1` as the final rendering target.
- Keep `1.21.4` client items and `1.21.6` GUI flow as still-active requirements, not obsolete history.

## Item models and item metadata

Relevant sections:

- [Client Items](detailed-primers/1.21.4-from-1.21.2-3.md#client-items) (1.21.4)
- [Mob Replacing Current Items](detailed-primers/1.21.4-from-1.21.2-3.md#mob-replacing-current-items) (1.21.4)
- [Particles, rendered through Render Types](detailed-primers/1.21.4-from-1.21.2-3.md#particles-rendered-through-render-types) (1.21.4)
- [Weapons, Tools, and Armor: Removing the Redundancies](detailed-primers/1.21.5-from-1.21.4.md#weapons-tools-and-armor-removing-the-redundancies) (1.21.5)
- [Data Component Getters](detailed-primers/1.21.5-from-1.21.4.md#data-component-getters) (1.21.5)
- [Feature Submissions: The Movie](detailed-primers/1.21.9-from-1.21.8.md#feature-submissions-the-movie) (1.21.9)
- [Oh Hey, Another Rendering Rewrite](detailed-primers/1.21.11-from-1.21.10.md#oh-hey-another-rendering-rewrite) (1.21.11)
- [New Data Components](detailed-primers/1.21.11-from-1.21.10.md#new-data-components) (1.21.11)
- [Data Component Initializers](detailed-primers/26.1-from-1.21.11.md#data-component-initializers) (26.1)
- [Item Instances and Stack Templates](detailed-primers/26.1-from-1.21.11.md#item-instances-and-stack-templates) (26.1)
- [Dye Component](detailed-primers/26.1-from-1.21.11.md#dye-component) (26.1)
- [Even More Rendering Changes](detailed-primers/26.1-from-1.21.11.md#even-more-rendering-changes) (26.1)

What sticks:

- `1.21.4` client items are the baseline for item rendering data.
- `1.21.5` removes more hardcoded item-class assumptions in favor of components and equipment data.
- `1.21.9`, `1.21.11`, and `26.1` further change how items participate in rendering and metadata pipelines.

Practical rule:

- First convert item assets to client items.
- Then port behavior and metadata around components.
- Finally validate them against the `26.1` rendering and item-instance model.

## Tags, registries, codecs, and validation

Relevant sections:

- [The Holder Set Transition](detailed-primers/1.21.2-from-1.21.1.md#the-holder-set-transition) (1.21.2)
- [Registry Objcet Id, in the Properties?](detailed-primers/1.21.2-from-1.21.1.md#registry-objcet-id-in-the-properties) (1.21.2)
- [Recipes, now in Registry format](detailed-primers/1.21.2-from-1.21.1.md#recipes-now-in-registry-format) (1.21.2)
- [Tags and Parsing](detailed-primers/1.21.5-from-1.21.4.md#tags-and-parsing) (1.21.5)
- [Tag Providers: Appender Rewrite](detailed-primers/1.21.6-from-1.21.5.md#tag-providers-appender-rewrite) (1.21.6)
- [Generic Encoding and Decoding: Replacing Direct NBT Access](detailed-primers/1.21.6-from-1.21.5.md#generic-encoding-and-decoding-replacing-direct-nbt-access) (1.21.6)
- [The Rename Shuffle](detailed-primers/1.21.11-from-1.21.10.md#the-rename-shuffle) (1.21.11)
- [Loot Type Unrolling](detailed-primers/26.1-from-1.21.11.md#loot-type-unrolling) (26.1)
- [Validation Overhaul](detailed-primers/26.1-from-1.21.11.md#validation-overhaul) (26.1)
- [Serializer Records and Recipe Info](detailed-primers/26.1-from-1.21.11.md#serializer-records-and-recipe-info) (26.1)

What sticks:

- `1.21.2/3` is where `Holder` and `HolderSet` start affecting large parts of the codebase.
- `1.21.5` changes tag access, parser behavior, codec-based reads and writes, and saved-data construction.
- `1.21.6` changes tag provider building and nudges more code toward generic encoding and decoding.
- `1.21.11` contributes rename churn that affects registry and identifier-facing code.
- `26.1` finalizes more codec-driven infrastructure with loot type unrolling and validation overhaul.

Practical rule:

- The earlier chapters tell you how to get onto holder- and codec-based APIs.
- `26.1` is the final target for validation and loot registration shape.

## Data components

Relevant sections:

- [Consumables](detailed-primers/1.21.2-from-1.21.1.md#consumables) (1.21.2)
- [Equipments and Items, Models and All](detailed-primers/1.21.2-from-1.21.1.md#equipments-and-items-models-and-all) (1.21.2)
- [The Ingredient Shift](detailed-primers/1.21.2-from-1.21.1.md#the-ingredient-shift) (1.21.2)
- [Recipes, now in Registry format](detailed-primers/1.21.2-from-1.21.1.md#recipes-now-in-registry-format) (1.21.2)
- [Weapons, Tools, and Armor: Removing the Redundancies](detailed-primers/1.21.5-from-1.21.4.md#weapons-tools-and-armor-removing-the-redundancies) (1.21.5)
- [Data Component Getters](detailed-primers/1.21.5-from-1.21.4.md#data-component-getters) (1.21.5)
- [New Data Components](detailed-primers/1.21.11-from-1.21.10.md#new-data-components) (1.21.11)
- [Data Component Initializers](detailed-primers/26.1-from-1.21.11.md#data-component-initializers) (26.1)
- [Dye Component](detailed-primers/26.1-from-1.21.11.md#dye-component) (26.1)

What sticks:

- `1.21.2/3` introduces important component-facing migrations such as consumables and recipe-related data moves.
- `1.21.5` expands component-centered behavior for tools, armor, weapons, and general data access.
- `1.21.11` adds more component types.
- `26.1` continues with initializers, dye components, and more component additions.

Practical rule:

- Expect items and recipes to get less class-driven and more component-driven as you move forward.

## Saved data and world state

Relevant sections:

- [Saved Data, now with Types](detailed-primers/1.21.5-from-1.21.4.md#saved-data-now-with-types) (1.21.5)
- [Splitting the Primary Level Data into Saved Data](detailed-primers/26.1-from-1.21.11.md#splitting-the-primary-level-data-into-saved-data) (26.1)
- [World Clocks and Time Markers](detailed-primers/26.1-from-1.21.11.md#world-clocks-and-time-markers) (26.1)

What sticks:

- `1.21.5` moves saved data to `SavedDataType`.
- `26.1` splits primary level data further into dedicated saved-data objects.

Practical rule:

- Do the `1.21.5` migration first, then revisit every level/world persistence assumption again in `26.1`.

## Developer tooling, tests, debugging, and permissions

Relevant sections:

- [The Game Test Overhaul](detailed-primers/1.21.5-from-1.21.4.md#the-game-test-overhaul) (1.21.5)
- [The Debugging Overhaul](detailed-primers/1.21.9-from-1.21.8.md#the-debugging-overhaul) (1.21.9)
- [Debug Screens](detailed-primers/1.21.9-from-1.21.8.md#debug-screens) (1.21.9)
- [The JSON-RPC Management Servers](detailed-primers/1.21.9-from-1.21.8.md#the-json-rpc-management-servers) (1.21.9)
- [Permission Overhaul](detailed-primers/1.21.11-from-1.21.10.md#permission-overhaul) (1.21.11)
- [Gizmos](detailed-primers/1.21.11-from-1.21.10.md#gizmos) (1.21.11)
- [Java 25 and Deobfuscation](detailed-primers/26.1-from-1.21.11.md#java-25-and-deobfuscation) (26.1)

What sticks:

- `1.21.5` overhauls game tests.
- `1.21.9` overhauls debugging and management-server shape.
- `1.21.11` adds a permission overhaul and gizmo-focused visualization work.
- `26.1` adds Java 25 and more minor tooling-facing changes.

Practical rule:

- Port gameplay code first.
- Then re-enable your debug, test, and operator-only tooling against the later chapters.
