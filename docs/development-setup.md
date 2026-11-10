# Development Setup

## Current status

The repository is in the documentation and planning stage. A complete Unity project/package and verified setup instructions will be added with the first implementation.

## Intended baseline

- Unity 6 as the initial development target
- C#
- Procedural mesh generation using Unity mesh APIs
- ScriptableObjects for reusable profiles and presets
- Custom EditorWindow tools for authoring and preview

Compatibility with other Unity versions and render pipelines will be tested and documented rather than assumed.

## Planned repository layout

```text
FlowerForYou/
├── Assets/
│   ├── FlowerForYou/
│   │   ├── Runtime/
│   │   │   ├── Core/
│   │   │   ├── Geometry/
│   │   │   ├── Generators/
│   │   │   ├── Profiles/
│   │   │   └── Assembly/
│   │   ├── Editor/
│   │   ├── Tests/
│   │   ├── Samples/
│   │   └── Documentation/
├── Packages/
├── ProjectSettings/
├── README.md
├── ROADMAP.md
└── LICENSE
```

This is a proposed structure and may change as implementation needs become clearer.

## Before implementation begins

- Install a supported Unity 6 Editor version.
- Use version control and keep generated Library/Temp folders out of commits.
- Record the Unity version and render pipeline used for each test.
- Keep experimental scenes separate from reusable runtime code.

## Reporting setup problems

When opening an Issue, include the Unity version, operating system, render pipeline, Console output, and steps needed to reproduce the problem.
