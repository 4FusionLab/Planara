# Planara development

[Русская версия](AGENTS.ru.md)

Planara is a planned Autodesk Fusion add-in for flattening selected Solid Body faces into planar geometry.

## Shared 4FusionLab rules

- Shared standards: https://github.com/4FusionLab/.github/blob/main/AGENTS.md; shared CI model: https://github.com/4FusionLab/.github/blob/main/RELEASE_PLATFORM.md.
- Communicate and make plans in Russian; use English for code and Fusion UI. Retain separate README.md and README.ru.md.
- Inspect current files and Git status before changes. Use Conventional Commits; a PR with passing checks is preferred, and direct push to main is allowed.
- Do not change Fusion manifest UUIDs, command IDs, OS support or package format without a migration plan. Do not commit secrets, tokens or personal CAD files.
- Where runtime exists, a push or merge to main creates a release only for paths in .github/release-paths.txt after successful CI. Use GitVersion.Tool 6.8.2, an automatically created immutable tag and GitHub Release; do not create tags manually.
- Docs, README, tests, AGENTS.md or CI changes must not independently publish a release. Pin shared Actions only to a specific commit SHA.
- Unit tests and ZIPs do not replace native Autodesk Fusion validation. Preserve existing limitations and compatibility evidence.

## Current status

- The repository currently contains only the concept and documentation: there is no finished distributable add-in or release pipeline. Do not claim otherwise.
- The MVP targets flat Surface Bodies; measure deformation on non-developable surfaces rather than hiding it.
- Original model geometry must remain intact. Verify actual Autodesk Fusion API limitations and distinguish tested algorithms from hypotheses.
- A first release requires a separate unique Fusion manifest, runtime code, reproducible tests, native CAD acceptance, .github/release-paths.txt, a version, verified ZIP and automatic CI release workflow.
- Update the English and Russian READMEs when user-facing capabilities appear.
