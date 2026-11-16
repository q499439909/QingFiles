# QingFiles pull-request visual aids

These assets supplement PRs [#3](https://github.com/THUdzy51/QingFiles/pull/3), [#5](https://github.com/THUdzy51/QingFiles/pull/5), [#7](https://github.com/THUdzy51/QingFiles/pull/7), [#9](https://github.com/THUdzy51/QingFiles/pull/9), and [#11](https://github.com/THUdzy51/QingFiles/pull/11). They do not update the project's README or release screenshots.

## Source and environment

| PR | Captured feature commit |
|---|---|
| #3 — blank documents | `78654dc025140ccee7c277da3b8c132a533103d9` |
| #5 — compact headers | `ac44cea0ed7bd99db04964eb454765112cb9cf60` |
| #7 — path interaction | `e89c1621e88f1f4483d201b67fbfec7e5b521088` |
| #9 — external reveal | `ee2522e2049e8b546ef5d926b3c524eeb2854fbb` |
| #11 — filename-click rename | `d945ab796e8bd21ee52f2f87f8620b6316a5ef47` |

Captured on macOS 15.6, Apple silicon, with the app's Aqua appearance. All displayed documents and folders belong to the disposable `/tmp/QingFiles-PR-Demo` fixture. No chat or real attachment contents are shown.

## What the images demonstrate

- Each PNG is an export of native AppKit views from the corresponding feature build. The GIFs are **step-by-step state walkthroughs**, assembled from those exports with captions and viewport crops. They are **not continuous desktop screen recordings**.
- Capture-only Review menu controls exercised the production creation, search, navigation, and editor handlers. Controlled key-window state was used to display the inline editors for #3 and #11. The #11 capture helper enters the editor directly after exercising its filename-click entry point, so the GIF is not evidence of mouse timing or double-click compatibility.
- For #7, the GIF shows path text selection/editing, restoration of breadcrumbs, and clicking the Projects breadcrumb. It does not depict a Return-based path submission. The native subfolder menu options were observed through accessibility, but separate system menu windows are omitted by the view-capture mechanism.
- For #9, the demo sends a real `open -a QingFiles <sample.pdf>` request through macOS to reveal and select the original file. It is not a recording of WeChat's own menu. The settings image shows the existing saved setting; it was not toggled for capture. Its transparent content export is flattened onto the resolved Aqua window background, RGB `(236, 236, 236)`.
- UI state and controls come from the app, not an illustrated mockup. Captions and crops are outside the app's UI. These assets add no automated-test, physical-mouse, or third-party compatibility claims beyond the PRs' existing validation and acceptance records.

## Repository scope

Only media and these capture notes live on the contributor's `codex/pr-review-media` branch. Capture-only instrumentation is excluded from all feature branches and the restored installed application. The existing PR descriptions receive links to immutable versions of these files; their feature commits and README changes are untouched.

See `manifest.json` for per-PR steps and media checksums.
