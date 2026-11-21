# OmniPanel for Windows 11 · Preview 2

OmniPanel is a free desktop comic reader for local archives and PDFs. This release adds guided panel reading, new library shelves, and edition-by-edition ComicVine matching. OmniPanel was built with vibe coding by **jogra89**.

## Download and install

| Download | How to use it |
| --- | --- |
| [Windows installer (.exe)](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/OmniPanel-Windows-1.0-preview.2-setup-x64.exe) | Run setup to install for your Windows account, then open **OmniPanel** from Start. You can also create a desktop shortcut during setup. |
| [Portable x64 (.zip)](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/OmniPanel-Windows-1.0-preview.2-x64.zip) | Extract the entire archive to a writable folder and open `app\OmniPanel.exe`. |
| [Windows source (.zip)](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/OmniPanel-Windows-1.0-preview.2-source.zip) | Build the Windows reader with the .NET 10 SDK. The archive includes the installer source and build instructions. |

Both app downloads include the desktop runtime and target Windows 11 x64. The default setup destination is `%LOCALAPPDATA%\Programs\OmniPanel`. To bring a portable library into the installed app, close OmniPanel and copy its `app\data` folder into the installation’s `app` directory before you start reading. Back up an existing destination library before replacing it, and keep your comic files at their original paths.

[Full Windows feature guide](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/FEATURES.md) · [Download release notes](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/RELEASE_NOTES.md) · [Test results](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/TESTING.md) · [SHA-256 checksums](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/SHA256SUMS.txt)

## Changes since Windows Preview 1

- **Windows setup.** Install for the current Windows account, launch from Start, choose an optional desktop shortcut, and remove the installed program through Windows Settings. Its library and cached artwork are stored in `app\data`.
- **Library navigation.** Source roots now lead into one subfolder at a time. Browse series, creators by role, characters, publishers, story arcs, and tags. Continue Reading, Random comic, PDF visibility, hide/restore, personal tags, read status, group actions and favorites are available. Search includes metadata and paths. Date, issue, and aggregate page counts support useful sorting. Larger collections have navigable result pages.
- **Library appearance and indexing.** Switch between grid, cover wall and list, adjust cover width, and choose whether to show page totals and reading progress. The index reads file metadata and page counts and prepares covers without requiring you to open each book. Library data saves use file replacement. The API-key accessor is excluded from serialized state, and loading an older library removes its redundant clear-text field while keeping the protected credential.
- **ComicVine.** The picker shows the local cover next to the information needed to identify the correct series or collection, with paginated results, an issue-number filter and explicit selection. Choose how online and embedded metadata are merged. Change or forget a match while preserving reading progress and personal organization. Verified credits can supply cached creator portraits. Bulk and automatic lookup apply conservative exact-match rules; you can review uncertain editions manually.
- **Guided reading and export.** Follow detected panels, framed insets, or overlapping rows. Configure detection mode and sensitivity, overview, fallback, surroundings and transitions. Guided progress resumes at the saved stop. Page view exports a whole image and guided view exports a selected panel from the source-resolution archive image or a rendered PDF page.
- **Page reading.** Added two-page spreads with optional solo covers, continuous vertical and horizontal layouts, adjustable spacing, per-comic reading direction, additional page fits, page-edge fill, and richer zoom controls.
- **Information, settings, and themes.** An 80% dim covers the full reading surface behind the menu. The reader shows a full cover, credits and available portraits, synopsis, issue metadata, local time, and nearby page thumbnails in three sizes. Grouped settings have section shortcuts. Fourteen desktop themes apply fonts, window surfaces and settings accents.

- **Desktop controls and artwork.** Configure reader keyboard shortcuts, jump between issues, drag to pan and double-click to zoom. Page and panel view share five background choices. Guided transitions include glide and zoom out/in, with sharper source detail on magnification. Optional publisher images or a custom local logo can be cached for offline use.
- **Reliability.** A double-click cancels its pending single-click action, malformed optional metadata leaves readable pages accessible, and closing the reader cleans up the open archive session.

## Windows feature catalogue

OmniPanel Preview 2 is a self-contained comic reader for Windows 11 x64. Setup installs the reader for your Windows account and adds a Start menu shortcut. The portable ZIP runs from a writable folder after extraction. Both packages include the desktop runtime. [Windows installer](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/OmniPanel-Windows-1.0-preview.2-setup-x64.exe) · [Portable ZIP](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/OmniPanel-Windows-1.0-preview.2-x64.zip)

### Local comics and storage

| Source | Desktop behavior |
| --- | --- |
| CBZ / ZIP | Opens image pages inside ZIP archives and uses natural filename ordering, so page 2 comes before page 10. |
| CBR / RAR | Reads RAR comics, including RAR5. Solid archives use temporary extraction for navigation. |
| CB7 / 7z and CBT / TAR | Opens 7z or TAR comic archives and reads the supported images as pages. |
| PDF | Renders individual pages with Windows’ PDF engine. The optional PDFs shelf keeps documents separate from comic browsing. |

- Select **Add folder** to scan one or more source folders recursively. Opening a single file, passing a path when starting the executable, or dropping supported files and folders onto the window also works.
- Indexing reads the page count and embedded `ComicInfo.xml`, and prepares the first-page cover. The library can show a comic’s metadata and group page totals before you first read it. **More → Rescan source folders** picks up changes.
- The app uses each comic’s original file path. Showing or hiding a shelf, tagging a book, and marking it read change the local library only.
- By default, the library and artwork cache live in `data` beside `OmniPanel.exe`. The app caches covers, decoded pages during reading, and available online portraits. Portable updates can reuse the whole data directory.

### Browse, sort, and organize

| Shelf | What it includes |
| --- | --- |
| **All comics** | Visible non-PDF books. **Random comic** opens an accessible comic from this pool. |
| **Continue reading** | In-progress comics, ordered by recent reading under the default sort. The main library also offers shortcuts to recent in-progress issues. |
| **Folders** | Top-level sources followed by their immediate child folders and files. Open a group to descend and use **Up** to go back. |
| **Series** | Issues grouped by series name, with numeric issue ordering under the default sort. |
| **Creators** | One group per credited name. Filter by the roles present in your collection. A matched issue can supply a verified creator portrait. |
| **Characters**, **Publishers**, **Story arcs** | Groups based on the available file or matched metadata. |
| **Tags** | Both embedded and personal tags. Choose **Options → Edit personal tags** on a comic to change its personal tags. |
| **PDFs** | Visible PDF documents. Hide or show the entire shelf from **More** or **Settings → Library**. |
| **Hidden** | Individually hidden comics and PDFs. Choose **Restore to library** to bring one back with its reading position. |

- Search across names, titles, series and issue number, file paths, dates, publishers, credits, characters, story arcs, genres, and tags.
- Filter to unread, currently reading, finished, or favorite books. Mark individual issues or groups read or unread. Add or remove favorites from the library or reader details.
- Sort by series and issue, title, recent addition, recent reading, year, or total pages in either direction. A group’s total is the sum of the indexed books in that group.
- Use the **Options** button or right-click a tile for item or group actions. The library keeps long result sets accessible with previous/next controls.
- Choose **Grid**, **Cover wall**, or **List** in library settings. Adjust cover width for cover layouts and toggle page counts and progress indicators.
- Choose which browse shelves appear. **All comics** and **Hidden** remain accessible; PDFs have their own visibility switch. Completed issues and fully read groups can keep their usual cover art or use a fade, blur, or desaturation effect with adjustable strength. At full desaturation, the cover is grayscale.

### ComicVine matching

1. Open **Settings → ComicVine**, enter your personal API key, and use **Test ComicVine key** if desired. Save the settings. Windows protects the stored key for the current Windows account.
2. Choose **Match on ComicVine** from an issue’s library menu, or **ComicVine** beside its title in the reader. The picker shows the local cover, filename, and available series, number, year, and publisher. Edit the suggested series query when a filename is ambiguous.
3. Search series and collected editions. Compare candidate covers, publishers, start years, and issue counts. Choose a series to see its issues. Filter by number or select **Show all** and browse the paginated results.
4. Compare the issue cover, number, title, and date. Confirm the edition that belongs to this file. You can later **Change ComicVine match** or **Forget online details** from the issue menu.

By default, a match fills missing file information. An optional setting prefers available online values when the file and selected issue both supply a field. The match can supply issue identity, series, title, year, publisher, synopsis, role-based credits, characters and story arcs. Forgetting a match restores file metadata while retaining personal tags, favorites and reading progress. The original archive is left intact.

- **Match a group or library.** Select **Match unmatched comics** for a group, or choose it under **More** for the visible comic collection. A progress dialog reports the work and supports cancellation. The automatic decision requires a unique exact series and matching issue number and year. Ambiguous matches and collected editions that need review remain available for the individual picker.
- **Automatic matching.** Choose Off, New additions, Daily, Weekly, Every two weeks, or Monthly. Matching runs while the app is open. New additions establishes a baseline and considers files added afterward. Eligible comics have been indexed, are visible, and have no match. PDFs are excluded. A Wi-Fi-only option and a last-run result are available.
- **Creator portraits.** Available portraits are retrieved using matched creator identities and cached. Same-name or unavailable identities can display a placeholder. Local reading and file metadata work without a key. Live search, online details and new images require connectivity and API access.
- **Publisher artwork.** In reader details, open **Publisher artwork…** to choose a local image, fetch an available image from ComicVine for a verified publisher, or remove cached artwork. The publisher shelf can display the saved image for that publisher. Without one, its tile uses a representative cover.

### Page reading and navigation

- Read one page at a time or use **Two-page spread**. Keep the cover on its own to preserve printed pairing. Choose a default left-to-right or right-to-left direction and override it for an individual comic.
- **Vertical scroll** and **Horizontal scroll** present a continuous sequence of pages. Set the gap from 0 to 64 pixels. The reader tracks which page is in view, loads nearby pages as needed and supports direct jumps.
- In paged view, choose **Fit page**, **Fit width**, **Fit height**, **Actual size**, **Fill and crop**, or **Stretch**.
- Zoom using **Ctrl + mouse wheel** or the plus/minus keys. In the paged viewport, double-click toggles an enlarged view, and touch manipulation supports scaling and panning. Hardware coverage is listed in [device and build tests](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.2/TESTING.md).
- The reader saves the current page. Guided mode also remembers the panel position for an issue. **F11** switches fullscreen.

- Page and panel view both offer black, white, page-edge color, blurred page artwork, and a custom hexadecimal color. Blurred artwork is cached. When you zoom into a high-resolution page, the reader can load additional source detail without moving the viewport.

### Guided panel reading

- Press **P** or click **Panel view** to start guided reading on the current comic. Toggle it again to return to your page layout. Set the opening mode for new comics in **Settings → Panel reading**.
- **Smart detection** examines gutters and drawn boundaries. **Gutters only** and **Drawn borders** give you alternatives for different page designs. **Scrolling rows** moves through overlapping full-width bands without trying to separate every drawn panel.
- The six sensitivity choices are **Only clear panels**, **Cautious**, **Balanced**, **Eager**, **Join speech-bubble panels**, and **Find every panel**. Joining uses the page’s visual structure around a divider. It cannot interpret dialogue.
- Enable a whole-page overview before detected panels. Detection can also preserve an overview when framed insets leave other artwork or dialogue outside their borders. When the detector cannot establish a boundary, choose a whole page or overlapping rows as the fallback.
- Panel navigation follows the selected reading direction. Moving ahead from the last stop opens the next page; going back from a page’s first stop returns to the preceding page’s last stop.
- Choose **Hide**, **Dim**, or **Show** for surrounding artwork. Set dim strength from 0 to 100 percent. Choose instant, fade, slide, glide, or zoom out/in. The duration is adjustable up to 800 milliseconds. Glide follows the artwork between panels on the same page. Turning to a different page can use a fade.
- **Save panel** writes the selected panel to PNG. On a whole-page overview, select a detected panel or switch to page mode and use **Save page**. Archive-image exports use original decoded image dimensions. PDF pages are rasterized on export.

### Reader information and controls

Select **Details**, press **Space**, or click the center of the paged artwork. The overlay darkens the page by 80 percent and extends behind the top and bottom controls. An uncropped cover appears on the right and scrollable information appears on the left.

Read the issue title, page and panel status, local time, synopsis, publisher and year. Available comic metadata can also supply the volume, writer, penciller, inker, colorist, letterer, cover artist, editor, characters, genres, story arcs and tags. A missing synopsis is identified in the reader. When available, creator portrait tiles appear with names and roles.

The thumbnail strip shows nearby page previews. Select a preview to jump, or use the first/last-page shortcuts when they appear. Choose compact, standard, or large thumbnails.

| Control | Action |
| --- | --- |
| Left / Right arrow | Move between pages or panel stops in the selected reading direction. |
| Page Up / Page Down | Move backward or forward in sequence. |
| Home / End | Jump to the first or last page. |
| P | Toggle page and panel view. |
| Space | Show or close issue information. |
| Ctrl + mouse wheel, plus / minus | Zoom. |
| F11 | Toggle fullscreen. |
| Escape | Close settings or comic details, or return from the reader to the library. |

- **Custom shortcuts.** In Reading settings, assign keys or combinations to panel or page steps, whole-page jumps, issue navigation, the information view, and panel mode. Ctrl + Right/Left skips to the next/previous whole page. Alt + Right/Left opens the next/previous visible issue when series, volume, and publisher match.
- In the paged reader, drag to pan when the image extends beyond the viewport. Double-click zoom can be turned off for immediate single-click navigation.

### Themes and settings

The Windows app includes **Modern, Terminal, Desktop 95, Synthwave, Holo HUD, Atomic Age, Golden Age Pulp, Manga Ink, Deco Noir, Blueprint, Grimoire, Sketchbook, Bauhaus, and Bubblegum**. Themes style the desktop typography, window surfaces, and settings accents. The full-window settings overlay has jump controls for Appearance, Library, Reading, Panel reading, ComicVine, and About. Select **Save settings** to apply edits.

### Scope and practical limits

- The installer and portable ZIP target Windows 11 x64. The reader uses the Windows image codecs available on the machine. New releases are installed manually. Local PDFs are limited to 256 MB. Password-protected content is unsupported. Solid archive extraction is limited to 2 GB per reading session and 160 MB per extracted page.
- Panel detection is local image analysis. Unframed artwork, diagonals, overlapping panels, decorative borders and speech bubbles can produce grouped views or a full-page fallback.
- Windows has its own interface and library. Android-specific gestures, volume-button and controller remapping, page auto-rotation, warm light, and additional Android page-turn animations are outside this build. The desktop library does not synchronize with a tablet.
- ComicVine is a third-party service. A search can return no match, API limits can delay lookups, and some records have no portrait, synopsis, or detailed credits. Review uncertain editions with the individual picker.

OmniPanel was built with vibe coding by **jogra89**.

## Test results

### Real comic and native Windows controls

The desktop checks used the actual 35-page archive of *Midnight Fantastic Four #2*. The app read from the archive in place and stored test progress and cached artwork in an isolated desktop library.

| Area | Observed result |
| --- | --- |
| Library indexing and navigation | The native WPF window indexed all 35 pages and cached the cover. The folder and series shelves both opened down to the issue. Hiding and restoring it through the tile menu preserved its page. The PDF shelf toggle changed its visibility in the browse control. |
| Guided reading | The Windows decoder and default panel detector produced 81 views across all 35 pages. Thirteen pages had multiple stops. Page 31 yielded six panels with its conversation intact. Every computed crop stayed within the source image. |
| Sizes and reading order | The page 31 check exercised the optional whole-page overview. Framed insets changed order in manga mode. Overlapping full-width rows reached the bottom of a page, and all 24 combinations of detection mode and sensitivity returned valid crop coordinates on the checked artwork. |
| Export geometry | A PNG panel was decoded again and compared pixel-for-pixel with the selected region of the source used for export. |
| Continuous scrolling | The native scrolling viewport loaded real pages vertically and horizontally. Jumping to page 19, crossing adjacent pages, changing zoom, restoring page 7, and a measured 32-unit gap worked in the vertical layout. The horizontal layout supported left-to-right jumps and right-to-left travel from the cover to the end. |
| Loading and disposal | Leaving continuous mode during decoding suppressed stale results. Reopening displayed the requested page, and the tested viewport kept no more than eight page containers active. |

### Library and matching checks

Library regression checks covered nested folders, hidden/PDF separation, random-comic eligibility, creator roles, cross-field search, personal and embedded tags, group page totals, both page-count sort directions, progress and favorites, and saved options. A 327-item visible pool retained access to every issue. The serializer excluded the plaintext API-key accessor.

ComicVine checks use controlled API responses to exercise series search, paginated and number-filtered issue queries, wrong-series rejection, fill-versus-replace behavior, forgetting a match, and preserved reading state. They cover ambiguous and collected-edition handling, creator identity checks, missing photos, and rate-limit feedback. A personal key, network access, and a matching service record are needed to reproduce a live lookup.

### Coverage limits

These checks describe a Windows desktop build and the workflows exercised. Windows touch scaling is implemented in the paged reader; the tests did not use a physical Windows touchscreen. Computer-generated panel regions can still group irregular artwork or use a whole-page fallback. ComicVine’s live catalogue, the availability of any particular photo, and every combination of Windows hardware, codecs, archives and themes are outside the measured results.

### Packaged reader checks

The normal Windows reader advanced through all 35 pages and 81 stops. It reopened at the saved panel, navigated backward across a page boundary, kept the page 10 footer, and showed six panels on page 31. Double-click zoom suppressed the pending single-click page turn or menu action. Both continuous layouts jumped to the requested page and switched back into guided view. All five page backgrounds and five guided transitions were exercised, including rapid turns. Malformed optional XML left readable pages accessible. Closing the reader released its solid-archive session. The portable ZIP was extracted and run with an isolated library. The source ZIP was independently rebuilt with .NET SDK 10.0.404.
