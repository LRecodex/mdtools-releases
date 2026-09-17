# Changelog

All notable user-facing changes to MD Tools are recorded here. Versions follow semantic versioning.

## [1.9.0] - 2026-09-17

### Added

- Command palette with workspace, search, settings, update, theme, and help commands.
- Welcome dashboard with recent workspaces and quick actions.
- Markdown insights panel for document outline, wiki links, and backlinks.
- `[[Page Name]]` wiki links that open existing Markdown pages or create new ones.
- Rendered Markdown export to standalone HTML.
- Settings dialog for theme, editor mode, sidebar layout, and update status.
- Update dialog with latest release notes and explicit Download / Restart actions.

## [1.8.2] - 2026-09-17

### Changed

- Reworked packaged-app updates into a user-controlled status bar flow: check in the background, show an update button, download on request, then restart to install.

## [1.8.1] - 2026-09-17

### Added

- Packaged-app update checks against this repository's GitHub Releases feed.

### Changed

- Focused the Support LRecodex donation image on the scannable QR code and improved its dialog presentation.

## [1.8.0] - 2026-09-17

### Added

- Workspace Quick Open now searches file names, folder names, paths, and text inside Markdown, text, JSON, code, and CSV files.
- Content search results show a short excerpt around the matching text.
- Support LRecodex donation section in the sidebar.

## [1.7.0] - 2026-09-17

### Added

- Visible sidebar search button for Quick Open.
- Current-document search with `Ctrl+F` in Source, Split, and Preview modes.
- Preview search highlighting, match counts, next/previous navigation, case sensitivity, and Escape close behavior.
- Source/Split find and replace through CodeMirror, including whole-word and regular-expression options.
- Integration coverage for search, replacement, folder navigation, and responsive status bar layout.

### Changed

- Improved status bar alignment so long paths truncate and counters remain readable on narrow windows.
- Folder search results now expand ancestors and reveal the selected folder in the sidebar.

## [1.6.0] - 2026-09-01

### Added

- Tab context actions for closing current, other, right-side, saved, or all tabs.
- Tab utilities to copy paths or reveal files in Explorer.
- Persisted sidebar resizing with double-click reset.
- Visible app version and "Made by LRecodex" credit.
- `Ctrl+Shift+W`, `Ctrl+PageUp`, and `Ctrl+PageDown` tab shortcuts.

## [1.5.1] - 2026-08-20

### Changed

- Fixed window restoration after display changes so the app remains visible.

## [1.5.0] - 2026-08-05

### Added

- Copy files or entire folders from the workspace tree and paste them into any folder.
- Copy a file or folder's full path directly to the system clipboard.
- Right-click empty space in the sidebar to access the workspace root's folder actions.

### Changed

- Pasted duplicates receive automatic "Copy" names while retaining file extensions.
- The workspace root can no longer be renamed or deleted from its context menu.

## [1.4.0] - 2026-08-05

### Added

- A clear "Create in" indicator shows where toolbar-created files and folders will be placed.
- A Collapse All Folders button quickly resets the workspace tree and creation target.

### Changed

- The top New File and New Folder buttons now create inside the selected folder instead of always using the workspace root.
- Right-clicking a folder selects it as the creation target, and new folder inputs automatically reveal collapsed targets.
- Folder selection now follows folder renames and safely returns to the parent when the selected folder is deleted externally or from the app.

## [1.3.0] - 2026-07-27

### Added

- Open Markdown files by dragging them into MD Tools from File Explorer, without opening their parent folder.
- Drop multiple Markdown files at once to open each one in an editor tab.
- Clear drop-target feedback and an error message when a dropped item is not a supported Markdown file.

### Changed

- Standalone dropped files remain editable with live Source, Split, and Preview modes while the current workspace stays unchanged.

## [1.2.0] - 2026-07-22

### Added

- Editable plain-text, JSON, and source-code documents with language-aware editor support.
- Read-only previews for images, PDFs, Word documents, Excel workbooks, and CSV files.
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

## [1.1.0] - 2026-07-22

### Added

- Formatting toolbar for headings, emphasis, links, images, quotes, lists, tasks, tables, code blocks, and Mermaid diagrams.
- Fifteen built-in templates for general, work, study, and development documents.
- Template picker for new documents and applying a template to an existing document with replacement confirmation.
- Collapsible sidebar with persisted visibility and the `Ctrl+Shift+B` shortcut.
- `Ctrl+Shift+T` shortcut for applying a template.

### Changed

- `Ctrl+N` now opens the template-based document creator.
- Improved preview styling, dialogs, inline file creation, tab handling, and save-error feedback.

## [1.0.0] - 2026-07-19

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

[1.9.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.9.0
[1.8.2]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.8.2
[1.8.1]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.8.1
[1.8.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.8.0
[1.7.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.7.0
[1.6.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.6.0
[1.5.1]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.5.1
[1.5.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.5.0
[1.4.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.4.0
[1.3.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.3.0
[1.2.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.2.0
[1.1.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.1.0
[1.0.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.0.0
