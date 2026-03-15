# Repeatedly Changing Systems

This page is the guard rail for the direct port.

When the same subsystem changed in multiple intermediate versions, do not treat the earliest migration note as final. Use the latest applicable version as the source of truth, but still apply the older chapter first so the intermediate API transitions make sense.

## Rendering and graphics

Relevant chapters:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md)
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md)
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md)
- [1.21.6 -> 1.21.7](detailed-primers/1.21.7-from-1.21.6.md)
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md)
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md)
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md)

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

Relevant chapters:

- [1.21.2/3 -> 1.21.4](detailed-primers/1.21.4-from-1.21.2-3.md)
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md)
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md)
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md)
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md)

What sticks:

- `1.21.4` client items are the baseline for item rendering data.
- `1.21.5` removes more hardcoded item-class assumptions in favor of components and equipment data.
- `1.21.9`, `1.21.11`, and `26.1` further change how items participate in rendering and metadata pipelines.

Practical rule:

- First convert item assets to client items.
- Then port behavior and metadata around components.
- Finally validate them against the `26.1` rendering and item-instance model.

## Tags, registries, codecs, and validation

Relevant chapters:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md)
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md)
- [1.21.5 -> 1.21.6](detailed-primers/1.21.6-from-1.21.5.md)
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md)
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md)

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

Relevant chapters:

- [1.21.1 -> 1.21.2/3](detailed-primers/1.21.2-from-1.21.1.md)
- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md)
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md)
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md)

What sticks:

- `1.21.2/3` introduces important component-facing migrations such as consumables and recipe-related data moves.
- `1.21.5` expands component-centered behavior for tools, armor, weapons, and general data access.
- `1.21.11` adds more component types.
- `26.1` continues with initializers, dye components, and more component additions.

Practical rule:

- Expect items and recipes to get less class-driven and more component-driven as you move forward.

## Saved data and world state

Relevant chapters:

- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md)
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md)

What sticks:

- `1.21.5` moves saved data to `SavedDataType`.
- `26.1` splits primary level data further into dedicated saved-data objects.

Practical rule:

- Do the `1.21.5` migration first, then revisit every level/world persistence assumption again in `26.1`.

## Developer tooling, tests, debugging, and permissions

Relevant chapters:

- [1.21.4 -> 1.21.5](detailed-primers/1.21.5-from-1.21.4.md)
- [1.21.8 -> 1.21.9](detailed-primers/1.21.9-from-1.21.8.md)
- [1.21.10 -> 1.21.11](detailed-primers/1.21.11-from-1.21.10.md)
- [1.21.11 -> 26.1](detailed-primers/26.1-from-1.21.11.md)

What sticks:

- `1.21.5` overhauls game tests.
- `1.21.9` overhauls debugging and management-server shape.
- `1.21.11` adds a permission overhaul and gizmo-focused visualization work.
- `26.1` adds Java 25 and more minor tooling-facing changes.

Practical rule:

- Port gameplay code first.
- Then re-enable your debug, test, and operator-only tooling against the later chapters.
