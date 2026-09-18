# MD Tools - Releases

Download ready-to-use Windows builds of **MD Tools v1.10.0**, a focused desktop workspace for writing Markdown, browsing project documents, and previewing Mermaid diagrams.

Get the newest build from the **[latest release](../../releases/latest)**.

## Download

- **`MD-Tools-Setup-x.x.x.exe`** - standard Windows installer with Start Menu and Desktop shortcuts.
- **`MD-Tools-Portable-x.x.x.exe`** - portable app; run it without installing.
- **`latest.yml`** and **`.blockmap`** - updater metadata used by installed packaged builds.
- **`SHA256SUMS.txt`** - SHA-256 checksums for release verification.

Both packages target **64-bit Windows**. The builds are currently unsigned, so Windows SmartScreen may show a warning the first time you open one. Choose **More info > Run anyway** only when the file was downloaded from this repository.

## What's New In v1.10.0

- Added a formula-aware Excel preview with row and column labels.
- Select any spreadsheet cell to inspect its formula and calculated result.
- Formula references and their input cells use matching colors, making calculations easy to follow.

See [CHANGELOG.md](CHANGELOG.md) for the release history.

## Core Features

- Browse a workspace and create, copy, paste, rename, or delete files and folders from the sidebar.
- Edit Markdown in Source, Split, or Preview mode with live Mermaid rendering.
- Open commands from `Ctrl+Shift+P`.
- Search workspace file names, folder names, paths, and supported text file contents with `Ctrl+P`.
- Navigate Markdown headings, wiki links, and backlinks from the insights panel.
- Find inside the current document with `Ctrl+F`; Source/Split also support replace, regex, whole-word, and case-sensitive search.
- Format headings, emphasis, links, lists, tasks, tables, code, and Mermaid diagrams from the toolbar.
- Start from 15 built-in templates for meetings, projects, study, development, journals, and checklists.
- Preview Markdown, text, JSON, code, CSV, images, PDF, Word, and Excel documents.
- Autosave editable files shortly after typing, or save immediately with `Ctrl+S`.
- Use light, dark, or system theme, with responsive status and sidebar controls.

## Keyboard Shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl+N` | New document from a template |
| `Ctrl+O` | Open folder |
| `Ctrl+S` | Save current file |
| `Ctrl+W` | Close current tab |
| `Ctrl+Shift+W` | Close all tabs |
| `Ctrl+P` | Quick Open workspace search |
| `Ctrl+Shift+P` | Command Palette |
| `Ctrl+F` | Find in current document |
| `F3` / `Shift+F3` | Next / previous match |
| `Ctrl+H` | Find and replace in Source or Split mode |
| `Ctrl+Tab` / `Ctrl+Shift+Tab` | Next / previous tab |
| `Ctrl+PageUp` / `Ctrl+PageDown` | Previous / next tab |
| `Ctrl+Shift+B` | Show / hide sidebar |
| `Ctrl+Shift+T` | Apply a template to the current Markdown document |
| `Ctrl+,` | Cycle system / light / dark theme |
| `Ctrl+/` | Toggle in-app help |

## Updating

Installed packaged builds check this repository's latest GitHub Release shortly after startup. When a newer setup build is available, MD Tools shows an update action in the status bar. The user can keep working, download when ready, then restart to install.

Maintainers: see [RELEASE.md](RELEASE.md) for release commands.
