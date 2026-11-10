# Architecture Overview

This document describes the intended architecture. It is a design direction, not a claim that these systems are already implemented.

## Design goals

- Keep geometry generation modular and reusable.
- Separate botanical parameters from mesh-building algorithms.
- Support both Editor-time asset creation and, where practical, runtime generation.
- Make generation deterministic when the same profile, settings, and seed are used.
- Allow generated parts to be assembled into larger botanical structures.

## Proposed layers

### 1. Geometry primitives

Low-level utilities for building meshes, calculating normals and tangents, generating UVs, validating bounds, and managing mesh index limits.

### 2. Organ generators

Independent generators for botanical parts:

- Petals
- Leaves
- Stems
- Stamens and pistils
- Receptacles
- Buds
- Branch segments

Each generator should accept validated settings and return a predictable geometry result.

### 3. Assembly systems

Assembly systems position and combine generated organs into flowers, plants, shrubs, and trees. Placement rules should be separate from the geometry algorithms themselves.

### 4. Profiles and parameters

ScriptableObject profiles will store reusable settings for organ shapes, flower arrangements, plant structures, and style presets. Profiles should distinguish botanical observations from artistic controls and approximations.

### 5. Editor tools

Custom EditorWindows and inspectors will help users configure profiles, preview generation, manage seeds, and save generated assets. Editor-only code must remain outside runtime assemblies.

### 6. Output and optimization

The output layer will address materials, UVs, mesh validation, LODs, batching considerations, wind data, and asset export.

## Proposed module flow

`Profile + Settings + Seed → Organ Generators → Assembly → Validation → Game-ready Output`

## Key technical decisions to validate

- Mesh topology and winding conventions
- Normal and tangent generation
- UV layout strategy
- Mesh combination and index format limits
- Deterministic random-number handling
- Editor-time versus runtime generation boundaries
- Performance for dense vegetation
- Compatibility across Unity versions and render pipelines

## Initial implementation order

1. Petal mesh generation
2. Petal validation and tests
3. Petal presets
4. Flower assembly
5. Leaves and stems
6. Plant and branching systems
7. Bushes and trees
8. Optimization and export
