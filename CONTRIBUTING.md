# Contributing to Flower For You

Thank you for helping make botanical generation tools and assets freely available to game creators.

Contributions are welcome from programmers, technical artists, 3D artists, botanical researchers, writers, translators, and testers.

## Project governance

Flower For You is owner-led. The project owner makes final decisions about direction, architecture, scope, releases, and pull-request acceptance. Maintainers may be appointed by the owner.

## Before contributing

1. Read the README and Code of Conduct.
2. Search existing Issues and Discussions.
3. For significant changes, open an Issue or Discussion first.
4. Submit only work you created or are permitted to contribute under the applicable license.

## Contribution areas

- **Code:** procedural geometry, mesh utilities, editor tools, optimization, tests, and export support.
- **Botanical research:** species anatomy, petal and leaf morphology, branching, growth habits, and cited references.
- **Art and examples:** reference renders, material studies, test scenes, and style presets.
- **Documentation:** setup guides, tutorials, API explanations, translations, and examples.
- **Testing:** Unity compatibility, reproducible bug reports, performance measurements, and usability feedback.

## Pull requests

1. Fork the repository and create a focused branch.
2. Keep changes small and clearly scoped.
3. Follow existing C# style and folder conventions.
4. Test in the Unity Editor and describe the test environment.
5. Update documentation when behaviour or public APIs change.
6. Include screenshots or renders for visual changes where useful.
7. Link related Issues.

Large architectural changes should be discussed before implementation. Pull requests are reviewed and are not automatically accepted.

## Unity and C# guidelines

- Keep runtime generation logic separate from Editor-only UI.
- Validate parameters and handle invalid values safely.
- Prefer deterministic generation when a seed is supplied.
- Avoid unnecessary allocations in frequently executed paths.
- Do not silently overwrite user scenes or assets.
- Test mesh topology, normals, UVs, bounds, and index limits.
- Explain new package dependencies.
- Document public APIs and non-obvious geometry calculations.

## Botanical research

Species-profile contributions should include common and scientific names where known, reliable citations, a distinction between verified traits and procedural approximations, and notes about variation across cultivars or growing conditions.

## Licensing

- Source-code contributions are submitted under the MIT License.
- Original assets accepted into the official project asset collection are submitted under CC0 1.0 Universal.
- Contributors retain copyright ownership of their original contributions while granting the public the rights described by the applicable license.
- Do not submit third-party material unless its license permits the intended redistribution. Include required attribution and license details.

By submitting a contribution, you confirm that you have the rights needed to license it under the applicable terms.

## Questions

Use GitHub Discussions for questions and design conversations. Use Issues for actionable bugs and feature requests.
