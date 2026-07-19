# MD Tools — Releases

Prebuilt Windows installers for **MD Tools**, a fast, polished desktop app for browsing, viewing,
and authoring Markdown files — with live preview and built-in Mermaid diagram rendering.


![MD Tools — Mermaid diagram rendered live in Preview mode](.github/assets/screenshot-mermaid.png)

## Download

Grab the latest installer from the [Releases](../../releases) page:

- **`MD Tools-Setup-x.x.x.exe`** — standard installer (recommended), adds Start Menu / Desktop shortcuts
- **`MD Tools-Portable-x.x.x.exe`** — portable build, no installation required

These builds are unsigned, so Windows SmartScreen may show a warning on first run
("Windows protected your PC"). Click **More info → Run anyway** to proceed.

## Features

- Sidebar file browser — open a folder, create/rename/delete files and folders
- Tabs with autosave and an unsaved-changes prompt before closing
- Source / Split / Preview editor modes
- Live Markdown preview with syntax-highlighted code blocks
- Live **Mermaid diagram** rendering
- Quick Open (`Ctrl+P`) fuzzy file search
- Light / dark / system theme (`Ctrl+,`)
- Built-in Help dialog (`Ctrl+/`)

## Markdown & Mermaid support

Standard Markdown — headings, bold/italic, links, task lists, tables, and fenced code blocks —
renders with syntax highlighting for JS/TS, Python, Bash, JSON, HTML, CSS, YAML, C++, Java, and SQL.

Fence a code block with `mermaid` to render flowcharts, sequence diagrams, Gantt charts, and more
directly in the preview, no extra setup required:

````markdown
```mermaid
graph TD
  A[Write Markdown] --> B{Need a diagram?}
  B -->|Yes| C[Add a mermaid block]
  B -->|No| D[Preview instantly]
  C --> D
```
````

![Source on the left, live preview with syntax highlighting on the right](.github/assets/screenshot-split.png)

## How to use

1. Install (or run the portable build), then launch **MD Tools**.
2. **Open a folder** — `Ctrl+O`, or the folder icon in the sidebar. That folder becomes your workspace.
3. Click a file in the sidebar to open it in a tab; right-click for new file / new folder / rename / delete.
4. Use the **Source / Split / Preview** switcher (top-right of the editor) to pick how you want to work.
5. Changes autosave shortly after you stop typing, or instantly with `Ctrl+S`.

### Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl+N` | New file |
| `Ctrl+O` | Open folder |
| `Ctrl+S` | Save current file |
| `Ctrl+W` | Close current tab |
| `Ctrl+P` | Quick Open |
| `Ctrl+Tab` / `Ctrl+Shift+Tab` | Next / previous tab |
| `Ctrl+,` | Cycle theme (system → light → dark) |
| `Ctrl+/` | Toggle in-app help |
