# Changelog

All notable user-facing changes to MD Tools are recorded here. Versions follow semantic versioning.

## [1.2.0] — 2026-07-22

### Added

- Editable plain-text, JSON, and source-code documents with language-aware editor support.
- Read-only previews for images, PDFs, Word documents (`.docx`), Excel workbooks (`.xlsx` and `.xlsm`), and CSV files.
- Rendered Markdown export to PDF, including code highlighting and Mermaid diagrams.
- Markdown, TXT, and JSON file-type selection when creating a document.
- Resizable divider in Split mode.

### Changed

- Workspace browsing and Quick Open now recognize supported non-Markdown documents.
- The status bar and editor controls now adapt to editable and read-only file types.
- Markdown preview supports a useful set of inline HTML elements.

### Security

- Markdown, Word, and highlighted-code HTML is sanitized before display.
- External links are restricted to safe attributes and opened outside the app.

## [1.1.0] — 2026-07-22

### Added

- Formatting toolbar for headings, emphasis, links, images, quotes, lists, tasks, tables, code blocks, and Mermaid diagrams.
- Fifteen built-in templates for general, work, study, and development documents.
- Template picker for new documents and applying a template to an existing document with replacement confirmation.
- Collapsible sidebar with persisted visibility and the `Ctrl+Shift+B` shortcut.
- `Ctrl+Shift+T` shortcut for applying a template.

### Changed

- `Ctrl+N` now opens the template-based document creator.
- Improved preview styling, dialogs, inline file creation, tab handling, and save-error feedback.

## [1.0.0] — 2026-07-19

### Added

- Initial public Windows release.
- Workspace sidebar with file and folder creation, rename, and delete actions.
- Multi-tab Markdown editor with autosave and unsaved-change protection.
- Source, Split, and Preview modes.
- Live Markdown preview with syntax-highlighted fenced code blocks.
- Mermaid diagram rendering.
- Quick Open fuzzy search with `Ctrl+P`.
- Light, dark, and system themes.
- Built-in help and keyboard-shortcut reference.
- Setup installer and portable 64-bit Windows packages.

[1.2.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.2.0
[1.1.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.1.0
[1.0.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.0.0
