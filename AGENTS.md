# Repository Guidelines

## Project Structure & Module Organization
This repository is a compact archive of one ChatGPT export in three synchronized formats at the repository root:

- `ChatGPT-Critical State of Granular Flows.md`: readable Markdown transcript.
- `ChatGPT-Critical State of Granular Flows.json`: structured export metadata and message data.
- `ChatGPT-Critical State of Granular Flows.pdf`: frozen reference copy for sharing or review.

Keep related files in the root unless the repository grows enough to justify subdirectories. When adding a new export set, keep the same basename across formats.

## Build, Test, and Development Commands
There is no build pipeline or application runtime in this repository. Use lightweight validation commands instead:

- `git status`: confirm the working tree before and after edits.
- `python -m json.tool "ChatGPT-Critical State of Granular Flows.json" > /dev/null`: validate JSON syntax.
- `sed -n '1,20p' "ChatGPT-Critical State of Granular Flows.md"`: spot-check Markdown headers and metadata.

If scripts are added later, place them in a dedicated `scripts/` directory and document their usage here.

## Coding Style & Naming Conventions
Prefer Markdown and JSON edits that preserve the existing export structure. Use UTF-8 text, wrap prose naturally, and avoid reformatting large blocks unless needed.

- File names: descriptive title + format suffix, for example `ChatGPT-Topic Name.md`.
- Markdown: standard ATX headings (`#`, `##`) and short paragraphs.
- JSON: keep original key ordering and indentation style when possible.

## Testing Guidelines
There is no automated test framework yet. Validation is manual:

- Confirm JSON parses cleanly.
- Check that Markdown metadata matches the JSON metadata.
- Ensure `.md`, `.json`, and `.pdf` versions describe the same conversation/export.

For any future tooling, add small reproducible checks and document exact commands.

## Commit & Pull Request Guidelines
Current history uses short, imperative commit messages such as `upload AI talks`. Continue with concise action-first subjects, for example `add granular flow export` or `update transcript metadata`.

Pull requests should include:

- A brief summary of what changed.
- Whether all three export artifacts were added or updated.
- Any manual validation performed, especially JSON parsing and metadata checks.
