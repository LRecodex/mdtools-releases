# Release and changelog commands

This project uses two repositories:

- `mdtools` contains the private application source and creates the Windows binaries.
- `mdtools-releases` contains public documentation, tags, release notes, and downloadable binaries.

Run the commands below in **PowerShell**. Replace `$Version` and the changelog text for each release.

## 1. Prepare and build the app

```powershell
$Version = '1.3.0'
$AppRepo = 'C:\Users\FauzulAzim\Documents\P\mdtools'
$ReleaseRepo = 'C:\Users\FauzulAzim\Documents\P\mdtools-releases'

Set-Location $AppRepo
git status -sb
git pull --ff-only
npm version $Version --no-git-tag-version
npm install
npm run typecheck
npm run dist
```

`npm version` updates both `package.json` and `package-lock.json`. Confirm that these files show the
same version and that `release\MD Tools-Setup-$Version.exe` and
`release\MD Tools-Portable-$Version.exe` were created.

Commit and push the source version change if it is not already committed:

```powershell
git add package.json package-lock.json
git commit -m "chore: release v$Version"
git push origin main
```

## 2. Update the public changelog

Add a new section at the top of `CHANGELOG.md`, below the introduction:

```markdown
## [1.3.0] — YYYY-MM-DD

### Added

- New user-facing capability.

### Changed

- Existing behavior that changed.

### Fixed

- User-visible bug that was fixed.
```

Only include headings that have entries. Describe user-visible changes, not commit mechanics. Add a
version link at the bottom of the file:

```markdown
[1.3.0]: https://github.com/LRecodex/mdtools-releases/releases/tag/v1.3.0
```

Update `README.md` when installation steps, supported formats, shortcuts, screenshots, or headline
features changed. Then publish the documentation:

```powershell
Set-Location $ReleaseRepo
git status -sb
git pull --ff-only
git add README.md CHANGELOG.md RELEASE.md
git commit -m "docs: prepare MD Tools v$Version"
git push origin main
```

## 3. Create release notes and publish

Create a temporary release-notes file from the matching changelog entry. Keep it concise and include
the package choices and unsigned-build warning.

```powershell
$NotesFile = Join-Path $env:TEMP "mdtools-v$Version-release-notes.md"
@"
## What's new

- Add the release highlights from CHANGELOG.md here.

See the [full changelog](https://github.com/LRecodex/mdtools-releases/blob/main/CHANGELOG.md).

### Downloads

- **Setup**: standard Windows installer.
- **Portable**: runs without installation.

Both builds are unsigned and target 64-bit Windows.
"@ | Set-Content -Encoding utf8 $NotesFile

gh release create "v$Version" `
  (Join-Path $AppRepo "release\MD Tools-Setup-$Version.exe") `
  (Join-Path $AppRepo "release\MD Tools-Portable-$Version.exe") `
  --repo LRecodex/mdtools-releases `
  --target main `
  --title "MD Tools v$Version" `
  --notes-file $NotesFile `
  --latest
```

The `gh release create` command creates the Git tag in `mdtools-releases`, uploads both binaries,
publishes the release, and marks it as latest.

## 4. Verify the release

```powershell
gh release view "v$Version" --repo LRecodex/mdtools-releases
gh release view "v$Version" --repo LRecodex/mdtools-releases --json assets,tagName,publishedAt,url
git ls-remote --tags origin "v$Version"
Get-FileHash (Join-Path $AppRepo "release\MD Tools-Setup-$Version.exe") -Algorithm SHA256
Get-FileHash (Join-Path $AppRepo "release\MD Tools-Portable-$Version.exe") -Algorithm SHA256
```

Finally, open the public release page and confirm that both downloads are present and the
`../../releases/latest` link in `README.md` resolves to the new version.
