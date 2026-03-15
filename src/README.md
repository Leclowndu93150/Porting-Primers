# 1.21.1 to 26.1 NeoForge Porting Guide

This site indexes the upstream NeoForge porting primers so you can jump straight to the section that matters.

The upstream chain covered here is:

`1.21.1 -> 1.21.2/3 -> 1.21.4 -> 1.21.5 -> 1.21.6 -> 1.21.7 -> 1.21.8 -> 1.21.9 -> 1.21.10 -> 1.21.11 -> 26.1`

There is no separate `1.21.3` primer upstream. The `1.21.2` primer covers the `1.21.1 -> 1.21.2/3` step.

## How to use this site

**If you know what subsystem changed**, use the [Topic Map](#topic-map) below. Every link goes directly to the relevant section.

**If the same subsystem changed across multiple versions**, see [Repeatedly Changing Systems](repeatedly-changing-systems.md) for the reading order.

**If you want the raw primers**, see [Detailed Primers](detailed-primers/README.md) for a full table of contents with anchor links to every section.

**If you have a compile error**, use the [Class and Method Index](#class-and-method-index) to find where it changed.

---

## Topic Map

**Build, mappings, names, imports, and package moves**

- [The Rename Shuffle](detailed-primers/1.21.11-from-1.21.10.md#the-rename-shuffle) (1.21.11)
- [ResourceLocation to Identifier](detailed-primers/1.21.11-from-1.21.10.md#resourcelocation-to-identifier) (1.21.11)
- [The util Package](detailed-primers/1.21.11-from-1.21.10.md#the-util-package) (1.21.11)
- [critereon to criterion](detailed-primers/1.21.11-from-1.21.10.md#critereon-to-criterion) (1.21.11)
- [Entity and Object Subpackages](detailed-primers/1.21.11-from-1.21.10.md#entity-and-object-subpackages) (1.21.11)
- [Java 25 and Deobfuscation](detailed-primers/26.1-from-1.21.11.md#java-25-and-deobfuscation) (26.1)
- [JSpecify Annotations](detailed-primers/1.21.11-from-1.21.10.md#jspecify-annotations) (1.21.11)
- [Usage Annotations](detailed-primers/1.21.11-from-1.21.10.md#usage-annotations) (1.21.11)

**Datagen, packs, registries, tags, codecs, loot, validation, and recipe serialization**

- [The Holder Set Transition](detailed-primers/1.21.2-from-1.21.1.md#the-holder-set-transition) (1.21.2)
- [The Ingredient Shift](detailed-primers/1.21.2-from-1.21.1.md#the-ingredient-shift) (1.21.2)
- [Recipes, now in Registry format](detailed-primers/1.21.2-from-1.21.1.md#recipes-now-in-registry-format) (1.21.2)
- [Recipe Providers, the 'not actually' of Data Providers](detailed-primers/1.21.2-from-1.21.1.md#recipe-providers-the-not-actually-of-data-providers) (1.21.2)
- [Instruments, the Datapack Edition](detailed-primers/1.21.2-from-1.21.1.md#instruments-the-datapack-edition) (1.21.2)
- [Trial Spawner Configurations, now in Datapack Form](detailed-primers/1.21.2-from-1.21.1.md#trial-spawner-configurations-now-in-datapack-form) (1.21.2)
- [Critereons, Supplied with HolderGetters](detailed-primers/1.21.2-from-1.21.1.md#critereons-supplied-with-holdergetters) (1.21.2 minor)
- [Codecable Json Reload Listener](detailed-primers/1.21.2-from-1.21.1.md#codecable-json-reload-listener) (1.21.2 minor)
- [Context Keys](detailed-primers/1.21.2-from-1.21.1.md#context-keys) (1.21.2 minor)
- [SimpleJsonResourceReloadListener](detailed-primers/1.21.4-from-1.21.2-3.md#simplejsonresourcereloadlistener) (1.21.4 minor)
- [MetadataSectionSerializer, replaced by Codecs](detailed-primers/1.21.4-from-1.21.2-3.md#metadatasectionserializer-replaced-by-codecs) (1.21.4 minor)
- [Tags and Parsing](detailed-primers/1.21.5-from-1.21.4.md#tags-and-parsing) (1.21.5)
- [Model Rework](detailed-primers/1.21.5-from-1.21.4.md#model-rework) (1.21.5)
- [Registry Context Swapper](detailed-primers/1.21.5-from-1.21.4.md#registry-context-swapper) (1.21.5 minor)
- [Timer Callbacks, joining the codec club!](detailed-primers/1.21.5-from-1.21.4.md#timer-callbacks-joining-the-codec-club) (1.21.5 minor)
- [Tag Providers: Appender Rewrite](detailed-primers/1.21.6-from-1.21.5.md#tag-providers-appender-rewrite) (1.21.6)
- [Generic Encoding and Decoding: Replacing Direct NBT Access](detailed-primers/1.21.6-from-1.21.5.md#generic-encoding-and-decoding-replacing-direct-nbt-access) (1.21.6)
- [Loot Type Unrolling](detailed-primers/26.1-from-1.21.11.md#loot-type-unrolling) (26.1)
- [Validation Overhaul](detailed-primers/26.1-from-1.21.11.md#validation-overhaul) (26.1)
- [Datapack Villager Trades](detailed-primers/26.1-from-1.21.11.md#datapack-villager-trades) (26.1)
- [Serializer Records and Recipe Info](detailed-primers/26.1-from-1.21.11.md#serializer-records-and-recipe-info) (26.1)
- [New Tag Providers](detailed-primers/26.1-from-1.21.11.md#new-tag-providers) (26.1 minor)
- [Plantable Tags](detailed-primers/26.1-from-1.21.11.md#plantable-tags) (26.1 minor)

**Items, components, equipment, armor, tools, combat, dyes, and consumables**

- [Equipments and Items, Models and All](detailed-primers/1.21.2-from-1.21.1.md#equipments-and-items-models-and-all) (1.21.2)
- [Armor Materials, Equipment, and Model (Textures)](detailed-primers/1.21.2-from-1.21.1.md#armor-materials-equipment-and-model-textures) (1.21.2)
- [Consumables](detailed-primers/1.21.2-from-1.21.1.md#consumables) (1.21.2)
- [Interaction Results](detailed-primers/1.21.2-from-1.21.1.md#interaction-results) (1.21.2)
- [BlockEntityTypes Privatized!](detailed-primers/1.21.2-from-1.21.1.md#blockentitytypes-privatized) (1.21.2)
- [Registry Objcet Id, in the Properties?](detailed-primers/1.21.2-from-1.21.1.md#registry-objcet-id-in-the-properties) (1.21.2)
- [Properties Changes](detailed-primers/1.21.2-from-1.21.1.md#properties-changes) (1.21.2)
- [Fuel Values](detailed-primers/1.21.2-from-1.21.1.md#fuel-values) (1.21.2 minor)
- [Mob Replacing Current Items](detailed-primers/1.21.4-from-1.21.2-3.md#mob-replacing-current-items) (1.21.4)
- [Weapons, Tools, and Armor: Removing the Redundancies](detailed-primers/1.21.5-from-1.21.4.md#weapons-tools-and-armor-removing-the-redundancies) (1.21.5)
- [Data Component Getters](detailed-primers/1.21.5-from-1.21.4.md#data-component-getters) (1.21.5)
- [Component Interaction Events](detailed-primers/1.21.5-from-1.21.4.md#component-interaction-events) (1.21.5 minor)
- [Item Owner](detailed-primers/1.21.9-from-1.21.8.md#item-owner) (1.21.9 minor)
- [Container User](detailed-primers/1.21.9-from-1.21.8.md#container-user) (1.21.9 minor)
- [Slot Sources](detailed-primers/1.21.11-from-1.21.10.md#slot-sources) (1.21.11 minor)
- [New Data Components](detailed-primers/1.21.11-from-1.21.10.md#new-data-components) (1.21.11)
- [Data Component Initializers](detailed-primers/26.1-from-1.21.11.md#data-component-initializers) (26.1)
- [Item Instances and Stack Templates](detailed-primers/26.1-from-1.21.11.md#item-instances-and-stack-templates) (26.1)
- [Dye Component](detailed-primers/26.1-from-1.21.11.md#dye-component) (26.1)
- [Data Component Additions](detailed-primers/26.1-from-1.21.11.md#data-component-additions) (26.1 minor)

**Rendering, models, shaders, particles, block models, item models, materials, atlases, and visual pipelines**

- [Gui Render Types](detailed-primers/1.21.2-from-1.21.1.md#gui-render-types) (1.21.2)
- [Shader Rewrites](detailed-primers/1.21.2-from-1.21.1.md#shader-rewrites) (1.21.2)
- [Entity Render States](detailed-primers/1.21.2-from-1.21.1.md#entity-render-states) (1.21.2)
- [Fog Parameters](detailed-primers/1.21.2-from-1.21.1.md#fog-parameters) (1.21.2 minor)
- [Light Emissions](detailed-primers/1.21.2-from-1.21.1.md#light-emissions) (1.21.2 minor)
- [Map Textures](detailed-primers/1.21.2-from-1.21.1.md#map-textures) (1.21.2 minor)
- [Client Items](detailed-primers/1.21.4-from-1.21.2-3.md#client-items) (1.21.4)
- [Particles, rendered through Render Types](detailed-primers/1.21.4-from-1.21.2-3.md#particles-rendered-through-render-types) (1.21.4)
- [Render Pipeline Rework](detailed-primers/1.21.5-from-1.21.4.md#render-pipeline-rework) (1.21.5)
- [Model Rework](detailed-primers/1.21.5-from-1.21.4.md#model-rework) (1.21.5)
- [Texture Atlas Reworks](detailed-primers/1.21.5-from-1.21.4.md#texture-atlas-reworks) (1.21.5 minor)
- [GUI Changes](detailed-primers/1.21.6-from-1.21.5.md#gui-changes) (1.21.6)
- [Blaze3d Changes](detailed-primers/1.21.6-from-1.21.5.md#blaze3d-changes) (1.21.6)
- [Removal of Mob Effects Atlas](detailed-primers/1.21.6-from-1.21.5.md#removal-of-mob-effects-atlas) (1.21.6 minor)
- [Animation Baking](detailed-primers/1.21.6-from-1.21.5.md#animation-baking) (1.21.6 minor)
- [ChunkSectionLayers](detailed-primers/1.21.6-from-1.21.5.md#chunksectionlayers) (1.21.6 minor)
- [Minor Migrations](detailed-primers/1.21.7-from-1.21.6.md#minor-migrations) (1.21.7 -- GUI render follow-ups)
- [Minor Migrations](detailed-primers/1.21.8-from-1.21.7.md#minor-migrations) (1.21.8 -- GraphicsWorkarounds)
- [Feature Submissions: The Movie](detailed-primers/1.21.9-from-1.21.8.md#feature-submissions-the-movie) (1.21.9)
- [The Font Glyph Pipeline](detailed-primers/1.21.9-from-1.21.8.md#the-font-glyph-pipeline) (1.21.9)
- [Client Asset Split](detailed-primers/1.21.9-from-1.21.8.md#client-asset-split) (1.21.9 minor)
- [Oh Hey, Another Rendering Rewrite](detailed-primers/1.21.11-from-1.21.10.md#oh-hey-another-rendering-rewrite) (1.21.11)
- [Gizmos](detailed-primers/1.21.11-from-1.21.10.md#gizmos) (1.21.11)
- [Even More Rendering Changes](detailed-primers/26.1-from-1.21.11.md#even-more-rendering-changes) (26.1)
- [Entity Textures and Adult/Baby Models](detailed-primers/26.1-from-1.21.11.md#entity-textures-and-adultbaby-models) (26.1 minor)
- [Audio Changes](detailed-primers/26.1-from-1.21.11.md#audio-changes) (26.1 minor)

**Entities, mobs, mob AI, conversions, spawning, and entity data**

- [Interaction Results](detailed-primers/1.21.2-from-1.21.1.md#interaction-results) (1.21.2)
- [EXPLOOOOSSSION!](detailed-primers/1.21.2-from-1.21.1.md#exploooosssion) (1.21.2 minor -- `Explosion` is now an interface)
- [Mob Conversions](detailed-primers/1.21.2-from-1.21.1.md#mob-conversions) (1.21.2 minor -- `Mob#convertTo` changed)
- [Minecart Behavior](detailed-primers/1.21.2-from-1.21.1.md#minecart-behavior) (1.21.2 minor)
- [Ender Pearl Chunk Loading](detailed-primers/1.21.2-from-1.21.1.md#ender-pearl-chunk-loading) (1.21.2 minor)
- [Entity References](detailed-primers/1.21.5-from-1.21.4.md#entity-references) (1.21.5 minor -- UUID replaced by `EntityReference`)
- [Leashes](detailed-primers/1.21.6-from-1.21.5.md#leashes) (1.21.6 minor)
- [Typed Entity Data](detailed-primers/1.21.9-from-1.21.8.md#typed-entity-data) (1.21.9 minor)
- [Name And Id](detailed-primers/1.21.9-from-1.21.8.md#name-and-id) (1.21.9 minor)
- [The Removal of interactAt](detailed-primers/26.1-from-1.21.11.md#the-removal-of-interactat) (26.1 minor -- `Entity#interactAt` removed)
- [Activities and Brains](detailed-primers/26.1-from-1.21.11.md#activities-and-brains) (26.1 minor -- AI brain system changes)
- [More Entity Sound Variant Registries](detailed-primers/26.1-from-1.21.11.md#more-entity-sound-variant-registries) (26.1 minor)
- [Zombie Nautilus Variant](detailed-primers/1.21.11-from-1.21.10.md#zombie-nautilus-variant) (1.21.11 minor)

**GUI, input, keybinds, debug screens, debug tooling, RPC tooling, and test infrastructure**

- [Gui Render Types](detailed-primers/1.21.2-from-1.21.1.md#gui-render-types) (1.21.2)
- [The Game Test Overhaul](detailed-primers/1.21.5-from-1.21.4.md#the-game-test-overhaul) (1.21.5)
- [GUI Changes](detailed-primers/1.21.6-from-1.21.5.md#gui-changes) (1.21.6)
- [Minor Migrations](detailed-primers/1.21.7-from-1.21.6.md#minor-migrations) (1.21.7)
- [The Debugging Overhaul](detailed-primers/1.21.9-from-1.21.8.md#the-debugging-overhaul) (1.21.9)
- [Debug Screens](detailed-primers/1.21.9-from-1.21.8.md#debug-screens) (1.21.9)
- [The JSON-RPC Management Servers](detailed-primers/1.21.9-from-1.21.8.md#the-json-rpc-management-servers) (1.21.9)
- [Input Handling Consolidation](detailed-primers/1.21.9-from-1.21.8.md#input-handling-consolidation) (1.21.9)
- [Cursor Types](detailed-primers/1.21.9-from-1.21.8.md#cursor-types) (1.21.9 minor)
- [Gizmos](detailed-primers/1.21.11-from-1.21.10.md#gizmos) (1.21.11)
- [Text Collectors](detailed-primers/1.21.11-from-1.21.10.md#text-collectors) (1.21.11 minor)
- [OptionEnum Removal](detailed-primers/1.21.11-from-1.21.10.md#optionenum-removal) (1.21.11 minor)
- [Container Screen Changes](detailed-primers/26.1-from-1.21.11.md#container-screen-changes) (26.1 minor)
- [Input Message Editor Support](detailed-primers/26.1-from-1.21.11.md#input-message-editor-support) (26.1 minor)
- [Test Environment State Tracking](detailed-primers/26.1-from-1.21.11.md#test-environment-state-tracking) (26.1 minor)

**World state, saved data, game rules, timelines, clocks, players, permissions, waypoints, and other server-side systems**

- [Handling the Removal of Block Entities Properly](detailed-primers/1.21.5-from-1.21.4.md#handling-the-removal-of-block-entities-properly) (1.21.5)
- [Voxel Shape Helpers](detailed-primers/1.21.5-from-1.21.4.md#voxel-shape-helpers) (1.21.5)
- [Weighted List Rework](detailed-primers/1.21.5-from-1.21.4.md#weighted-list-rework) (1.21.5)
- [Tickets](detailed-primers/1.21.5-from-1.21.4.md#tickets) (1.21.5)
- [Saved Data, now with Types](detailed-primers/1.21.5-from-1.21.4.md#saved-data-now-with-types) (1.21.5)
- [Block Effect Appliers](detailed-primers/1.21.5-from-1.21.4.md#block-effect-appliers) (1.21.5 minor)
- [Waypoints](detailed-primers/1.21.6-from-1.21.5.md#waypoints) (1.21.6)
- [Server Player Changes](detailed-primers/1.21.6-from-1.21.5.md#server-player-changes) (1.21.6)
- [Permission Sources](detailed-primers/1.21.6-from-1.21.5.md#permission-sources) (1.21.6 minor)
- [Level#isClientSide now private](detailed-primers/1.21.9-from-1.21.8.md#levelisclientside-now-private) (1.21.9)
- [Ticket Flags](detailed-primers/1.21.9-from-1.21.8.md#ticket-flags) (1.21.9 minor)
- [Respawn Data](detailed-primers/1.21.9-from-1.21.8.md#respawn-data) (1.21.9 minor)
- [Permission Overhaul](detailed-primers/1.21.11-from-1.21.10.md#permission-overhaul) (1.21.11)
- [The Timeline of Environment Attributes](detailed-primers/1.21.11-from-1.21.10.md#the-timeline-of-environment-attributes) (1.21.11)
- [The Game Rule Shuffle](detailed-primers/1.21.11-from-1.21.10.md#the-game-rule-shuffle) (1.21.11)
- [Level#random field now protected](detailed-primers/26.1-from-1.21.11.md#levelrandom-field-now-protected) (26.1)
- [World Clocks and Time Markers](detailed-primers/26.1-from-1.21.11.md#world-clocks-and-time-markers) (26.1)
- [Splitting the Primary Level Data into Saved Data](detailed-primers/26.1-from-1.21.11.md#splitting-the-primary-level-data-into-saved-data) (26.1)
- [Chat Permissions](detailed-primers/26.1-from-1.21.11.md#chat-permissions) (26.1 minor)
- [ChunkPos, now a record](detailed-primers/26.1-from-1.21.11.md#chunkpos-now-a-record) (26.1 minor)
- [Cauldron Interaction Dispatchers](detailed-primers/26.1-from-1.21.11.md#cauldron-interaction-dispatchers) (26.1 minor)
- [Fluid Logic Reorganization](detailed-primers/26.1-from-1.21.11.md#fluid-logic-reorganization) (26.1 minor)
- [Removal of Random Patch Feature](detailed-primers/26.1-from-1.21.11.md#removal-of-random-patch-feature) (26.1 minor)
- [Rule-Based Block State Providers](detailed-primers/26.1-from-1.21.11.md#rule-based-block-state-providers) (26.1 minor)
- [File Fixer Upper](detailed-primers/26.1-from-1.21.11.md#file-fixer-upper) (26.1 minor)

**Remaining minor migrations**

- [Language File Removals and Renames](detailed-primers/1.21.2-from-1.21.1.md#language-file-removals-and-renames) (1.21.2)
- [MacosUtil#IS_MACOS](detailed-primers/1.21.2-from-1.21.1.md#macosutilis_macos) (1.21.2)
- [Smarter Framerate Limiting](detailed-primers/1.21.2-from-1.21.1.md#smarter-framerate-limiting) (1.21.2)
- [Orientations](detailed-primers/1.21.2-from-1.21.1.md#orientations) (1.21.2)
- [The Removal of the Carving Generation Step](detailed-primers/1.21.2-from-1.21.1.md#the-removal-of-the-carving-generation-step) (1.21.2)
- [Consecutive Executors](detailed-primers/1.21.2-from-1.21.1.md#consecutive-executors) (1.21.2)
- [Profilers and the Tracy Client](detailed-primers/1.21.2-from-1.21.1.md#profilers-and-the-tracy-client) (1.21.2)
- [Tick Throttler](detailed-primers/1.21.2-from-1.21.1.md#tick-throttler) (1.21.2)
- [Music, now with Volume Controls](detailed-primers/1.21.4-from-1.21.2-3.md#music-now-with-volume-controls) (1.21.4)
- [Descoping Player Arguments](detailed-primers/1.21.5-from-1.21.4.md#descoping-player-arguments) (1.21.5)
- [Reload Instance Creation](detailed-primers/1.21.5-from-1.21.4.md#reload-instance-creation) (1.21.5)
- [The JOML Backing Interfaces](detailed-primers/1.21.5-from-1.21.4.md#the-joml-backing-interfaces) (1.21.5)
- [Mob Effects Field Renames](detailed-primers/1.21.5-from-1.21.4.md#mob-effects-field-renames) (1.21.5)
- [Reload Listener Shared State](detailed-primers/1.21.9-from-1.21.8.md#reload-listener-shared-state) (1.21.9)
- [The 'On Shelf' Transform](detailed-primers/1.21.9-from-1.21.8.md#the-on-shelf-transform) (1.21.9)
- [Shared Text Areas Debugger](detailed-primers/1.21.11-from-1.21.10.md#shared-text-areas-debugger) (1.21.11)
- [Specific Logic Changes](detailed-primers/1.21.11-from-1.21.10.md#specific-logic-changes) (1.21.11)
- [Typed Instance](detailed-primers/26.1-from-1.21.11.md#typed-instance) (26.1)
- [No More Tripwire Pipelines](detailed-primers/26.1-from-1.21.11.md#no-more-tripwire-pipelines) (26.1)
- [Environment Attribute Additions](detailed-primers/26.1-from-1.21.11.md#environment-attribute-additions) (26.1)
- [Specific Logic Changes](detailed-primers/26.1-from-1.21.11.md#specific-logic-changes) (26.1)

Every primer also contains `New Tags`, `Tag Changes`, `List of Additions`, `List of Changes`, and `List of Removals` subsections within their Minor Migrations. For those, go to the full primer pages in [Detailed Primers](detailed-primers/README.md).

---

## Class and Method Index

If you have a compile error or need to find where a specific class/method changed, search this table.

| Class / Method | Version | Section |
|---|---|---|
| `AbstractFurnaceBlockEntity` fuel | 1.21.2 | [Fuel Values](detailed-primers/1.21.2-from-1.21.1.md#fuel-values) |
| `AbstractMinecart` | 1.21.2 | [Minecart Behavior](detailed-primers/1.21.2-from-1.21.1.md#minecart-behavior) |
| `Activities` / `Brain` | 26.1 | [Activities and Brains](detailed-primers/26.1-from-1.21.11.md#activities-and-brains) |
| `AnimationDefinition#bake` | 1.21.6 | [Animation Baking](detailed-primers/1.21.6-from-1.21.5.md#animation-baking) |
| `ArmorItem` / `ArmorMaterial` | 1.21.2 | [Armor Materials, Equipment, and Model (Textures)](detailed-primers/1.21.2-from-1.21.1.md#armor-materials-equipment-and-model-textures) |
| `BakedModel` / `BakedQuad` | 1.21.5 | [Model Rework](detailed-primers/1.21.5-from-1.21.4.md#model-rework) |
| `BlockBehaviour#neighborChanged` | 1.21.2 | [Orientations](detailed-primers/1.21.2-from-1.21.1.md#orientations) |
| `BlockEntityType` constructors | 1.21.2 | [BlockEntityTypes Privatized!](detailed-primers/1.21.2-from-1.21.1.md#blockentitytypes-privatized) |
| `CauldronInteraction` | 26.1 | [Cauldron Interaction Dispatchers](detailed-primers/26.1-from-1.21.11.md#cauldron-interaction-dispatchers) |
| `ChunkPos` (now record) | 26.1 | [ChunkPos, now a record](detailed-primers/26.1-from-1.21.11.md#chunkpos-now-a-record) |
| `ChunkSectionLayer` | 1.21.6 | [ChunkSectionLayers](detailed-primers/1.21.6-from-1.21.5.md#chunksectionlayers) |
| Client item JSONs | 1.21.4 | [Client Items](detailed-primers/1.21.4-from-1.21.2-3.md#client-items) |
| `Consumable` / `ConsumableListener` | 1.21.2 | [Consumables](detailed-primers/1.21.2-from-1.21.1.md#consumables) |
| `DataComponents` getters | 1.21.5 | [Data Component Getters](detailed-primers/1.21.5-from-1.21.4.md#data-component-getters) |
| `DataComponents` new types | 1.21.11 | [New Data Components](detailed-primers/1.21.11-from-1.21.10.md#new-data-components) |
| `DataComponents` initializers | 26.1 | [Data Component Initializers](detailed-primers/26.1-from-1.21.11.md#data-component-initializers) |
| `DiggerItem` / `SwordItem` removal | 1.21.5 | [Weapons, Tools, and Armor: Removing the Redundancies](detailed-primers/1.21.5-from-1.21.4.md#weapons-tools-and-armor-removing-the-redundancies) |
| `DyeRecipe` / `DyeItem` | 26.1 | [Dye Component](detailed-primers/26.1-from-1.21.11.md#dye-component) |
| `Entity#interactAt` removal | 26.1 | [The Removal of interactAt](detailed-primers/26.1-from-1.21.11.md#the-removal-of-interactat) |
| `EntityReference` (replaces UUID) | 1.21.5 | [Entity References](detailed-primers/1.21.5-from-1.21.4.md#entity-references) |
| `EntityRenderState` | 1.21.2 | [Entity Render States](detailed-primers/1.21.2-from-1.21.1.md#entity-render-states) |
| `Explosion` (now interface) | 1.21.2 | [EXPLOOOOSSSION!](detailed-primers/1.21.2-from-1.21.1.md#exploooosssion) |
| `GameRules` | 1.21.11 | [The Game Rule Shuffle](detailed-primers/1.21.11-from-1.21.10.md#the-game-rule-shuffle) |
| `GameTest` framework | 1.21.5 | [The Game Test Overhaul](detailed-primers/1.21.5-from-1.21.4.md#the-game-test-overhaul) |
| `GenerationStep$Carving` removal | 1.21.2 | [The Removal of the Carving Generation Step](detailed-primers/1.21.2-from-1.21.1.md#the-removal-of-the-carving-generation-step) |
| `GpuTexture` / `RenderPipeline` | 1.21.5 | [Render Pipeline Rework](detailed-primers/1.21.5-from-1.21.4.md#render-pipeline-rework) |
| `GuiGraphics` / GUI rendering | 1.21.6 | [GUI Changes](detailed-primers/1.21.6-from-1.21.5.md#gui-changes) |
| `Holder` / `HolderSet` / `HolderGetter` | 1.21.2 | [The Holder Set Transition](detailed-primers/1.21.2-from-1.21.1.md#the-holder-set-transition) |
| `Identifier` (was `ResourceLocation`) | 1.21.11 | [ResourceLocation to Identifier](detailed-primers/1.21.11-from-1.21.10.md#resourcelocation-to-identifier) |
| `Ingredient` | 1.21.2 | [The Ingredient Shift](detailed-primers/1.21.2-from-1.21.1.md#the-ingredient-shift) |
| `InteractionResult` | 1.21.2 | [Interaction Results](detailed-primers/1.21.2-from-1.21.1.md#interaction-results) |
| `ItemInstance` / `StackTemplate` | 26.1 | [Item Instances and Stack Templates](detailed-primers/26.1-from-1.21.11.md#item-instances-and-stack-templates) |
| `KeyMapping` / input events | 1.21.9 | [Input Handling Consolidation](detailed-primers/1.21.9-from-1.21.8.md#input-handling-consolidation) |
| `Leashable` | 1.21.6 | [Leashes](detailed-primers/1.21.6-from-1.21.5.md#leashes) |
| `Level#isClientSide` | 1.21.9 | [Level#isClientSide now private](detailed-primers/1.21.9-from-1.21.8.md#levelisclientside-now-private) |
| `Level#random` | 26.1 | [Level#random field now protected](detailed-primers/26.1-from-1.21.11.md#levelrandom-field-now-protected) |
| `LootContextParam` / `LootContextParamSet` | 1.21.2 | [Context Keys](detailed-primers/1.21.2-from-1.21.1.md#context-keys) |
| `LootPoolEntry` / loot codecs | 26.1 | [Loot Type Unrolling](detailed-primers/26.1-from-1.21.11.md#loot-type-unrolling) |
| `Mob#convertTo` | 1.21.2 | [Mob Conversions](detailed-primers/1.21.2-from-1.21.1.md#mob-conversions) |
| `OptionEnum` removal | 1.21.11 | [OptionEnum Removal](detailed-primers/1.21.11-from-1.21.10.md#optionenum-removal) |
| `Permission` / `PermissionSet` | 1.21.11 | [Permission Overhaul](detailed-primers/1.21.11-from-1.21.10.md#permission-overhaul) |
| `Profiler#get` (replaces `getProfiler`) | 1.21.2 | [Profilers and the Tracy Client](detailed-primers/1.21.2-from-1.21.1.md#profilers-and-the-tracy-client) |
| `Recipe` registry format | 1.21.2 | [Recipes, now in Registry format](detailed-primers/1.21.2-from-1.21.1.md#recipes-now-in-registry-format) |
| `RecipeDisplay` / `SlotDisplay` | 1.21.2 | [Recipes, now in Registry format](detailed-primers/1.21.2-from-1.21.1.md#recipes-now-in-registry-format) |
| `RenderType` shuffle | 1.21.11 | [Oh Hey, Another Rendering Rewrite](detailed-primers/1.21.11-from-1.21.10.md#oh-hey-another-rendering-rewrite) |
| `SavedData` / `SavedDataType` | 1.21.5 | [Saved Data, now with Types](detailed-primers/1.21.5-from-1.21.4.md#saved-data-now-with-types) |
| `ServerExplosion` | 1.21.2 | [EXPLOOOOSSSION!](detailed-primers/1.21.2-from-1.21.1.md#exploooosssion) |
| Shader JSON / `.vsh` / `.fsh` | 1.21.2 | [Shader Rewrites](detailed-primers/1.21.2-from-1.21.1.md#shader-rewrites) |
| `SimpleJsonResourceReloadListener` | 1.21.4 | [SimpleJsonResourceReloadListener](detailed-primers/1.21.4-from-1.21.2-3.md#simplejsonresourcereloadlistener) |
| `TagProvider` appender | 1.21.6 | [Tag Providers: Appender Rewrite](detailed-primers/1.21.6-from-1.21.5.md#tag-providers-appender-rewrite) |
| `Validatable` / `ValidationContext` | 26.1 | [Validation Overhaul](detailed-primers/26.1-from-1.21.11.md#validation-overhaul) |
| Villager trades (datapack) | 26.1 | [Datapack Villager Trades](detailed-primers/26.1-from-1.21.11.md#datapack-villager-trades) |
| `VoxelShape` helpers | 1.21.5 | [Voxel Shape Helpers](detailed-primers/1.21.5-from-1.21.4.md#voxel-shape-helpers) |
| `Waypoint` system | 1.21.6 | [Waypoints](detailed-primers/1.21.6-from-1.21.5.md#waypoints) |
| World clocks / time markers | 26.1 | [World Clocks and Time Markers](detailed-primers/26.1-from-1.21.11.md#world-clocks-and-time-markers) |
| World data split | 26.1 | [Splitting the Primary Level Data into Saved Data](detailed-primers/26.1-from-1.21.11.md#splitting-the-primary-level-data-into-saved-data) |

---

## Source and attribution

The split primer pages are copied from `ChampionAsh5357/neoforged-github`, branch `update/26.1`. See [Source And Attribution](source-and-attribution.md).
