# OmniPanel for Android · Feature catalogue

OmniPanel reads comics from folders you choose on your Android phone or tablet. Open an issue as printed, scroll through its pages, or follow the artwork panel by panel. Local reading and library organization work offline. ComicVine matching, creator-photo retrieval, and publisher-logo downloads use an internet connection.

## Files, folders, and storage

| File type | What OmniPanel opens |
| --- | --- |
| CBZ | Comic pages packed in a ZIP archive. |
| CBR | Comic pages packed in a RAR archive, including RAR5. |
| CB7 | Comic pages packed in a 7z archive. |
| CBT | Comic pages packed in a TAR archive. |
| PDF | Unencrypted PDF documents, available in a dedicated library section. Password-protected PDFs are unsupported. |
| ZIP, RAR, and 7z | The optional ordinary-archive scan includes image archives even when their filenames use the general-purpose extension. |

- **Add library folders.** Select one or more directories on internal storage or an accessible SD card. OmniPanel indexes books in place, so a library can span several locations and preserve the folder structure you use outside the app.
- **Grant folder access.** Use Android’s system folder picker. An all-files-access route is also available for locations such as Downloads, subject to the access Android grants.
- **Open a file directly.** Use Android’s **Open with** action for a supported comic or PDF that another app makes available.
- **Refresh the index.** Rescan source folders and optionally enable a rescan when the app launches. Scanning progress can be shown or hidden.
- **Manage reading storage.** Recently opened archives can be retained unpacked for faster reopening. Storage settings show cache usage and let you adjust the page-cache size.
- **Remove a source.** Removing a source folder from the library stops indexing it. The separate file-deletion commands for comics and folders identify the destructive action in their confirmation text.
- **App data.** OmniPanel uses Android’s private app storage for its own settings and library data. Adding a shared comic folder gives access to its files. Private library data belonging to another Android app stays with that app.

## Library shelves, discovery, and organization

| Browse by | What you see |
| --- | --- |
| Individual comics | A shelf of visible issues, with your choice of cover or list presentation. |
| Series | Issues grouped by series. A setting lets a series containing a single comic open directly in the reader. |
| Folders | The scanned source folders first. Open a root such as Downloads, then follow its subfolders one level at a time. Single-comic folders can also open their issue directly. |
| Creators | Groups by credited person, with a role selector. A group can show the person’s portrait when a matched ComicVine issue confirms their credit and a photo is available. |
| Characters, publishers, and story arcs | Browse issues associated with a character, publishing company, or named storyline. Results depend on the metadata available for the issues. |
| Tags | Browse by tag. Add or remove your own tags to organize a personal collection. |
| PDFs | Open **PDFs** from the library to browse or read documents. Use **More** to hide or show the PDF section as a whole. |

- **Random comic.** Tap **Random comic** to open an issue from the visible comics. Hidden books and PDFs are excluded.
- **Search.** Look up titles, series, characters, creators, or tags. Choose which browse tabs remain on the library screen.
- **Sort.** Order books by series and issue number, title, year, date added, date last read, or total pages. Total pages supports ascending and descending order. For a folder or group, OmniPanel adds its indexed comics’ page counts. For an issue, it uses that file’s page count.
- **Filter.** Show all, unread, currently reading, finished, or favorite comics. Mark a single issue or a whole group read or unread.
- **Resume reading.** The **Continue Reading** row returns you to books in progress. The reader saves the current page, and optional progress bars show how far you have read.
- **Hide an individual item.** Choose **Hide from library** on a comic or PDF to remove it from ordinary browsing while retaining the file and its reading progress. Open **More → Hidden comics**, select the item, and choose **Restore** to bring it back. The separate PDF-section visibility setting controls the entire shelf.

## Library appearance

- **Shelf layout.** Switch between a cover wall, a grid, and a list. Adjust cover size and the spacing between covers on the wall.
- **Cover information.** Choose whether to show series names, publisher logos, issue-count and read-status badges, and reading progress bars. Show or hide page counts for individual issues and combined counts for groups.
- **Finished books.** Change the appearance of finished issues and completed series. Choose normal, desaturated, black-and-white, blurred, or faded covers and adjust the strength of the effect.
- **Library controls.** Show or hide the library title and counts. Select the buttons that stay on the top bar. Other button actions remain accessible from the overflow menu.

## Comic metadata and ComicVine

OmniPanel can read embedded `ComicInfo.xml`. A book with suitable file metadata can show its details offline. Online matching is optional and requires a ComicVine API key. Enter and test the key in **Settings → ComicVine**.

| Detail | Fields shown when supplied |
| --- | --- |
| Publication | Title, series, issue number, volume, year, and publisher. |
| Story | Synopsis, characters, genres, story arc, and metadata tags. Personal tags appear as a separate field. |
| Credits | Writer, penciller, inker, colorist, letterer, cover artist, and editor. |
| Reading direction | Embedded manga-direction metadata, with a per-comic reading-direction control. |

### Choose the exact issue or collected edition

1. Open the comic and tap the reader’s menu zone. Use the **ComicVine logo beside the title** to choose a match or change an existing one.
2. Edit the suggested series or collection title if needed. Choose **Search series and collections**. Compare the available cover, start year, publisher, and issue count to distinguish similarly named runs.
3. Open the matching series or collection. Compare issue numbers, titles, cover dates, and cover images. For long runs, browse more issue results in groups of 100.
4. Select the issue or collected edition, review the confirmation, and choose **Use this match**. The choice applies to the comic you opened. Reopen the badge if you later identify a better edition.

### Match a series or maintain a library

- Search ComicVine for a series and select a matching issue. A series can also be matched from its library page. A library-wide scrape looks for unmatched series.
- Choose whether online metadata fills only missing fields or replaces fields supplied by the file. **Forget online details** returns to file metadata while preserving reading progress and personal tags.
- Choose manual lookup, automatic lookup when new comics are added, or a daily, weekly, fortnightly, or monthly schedule. Automatic scraping can be restricted to Wi-Fi. The app displays the last library scrape and its result.
- With **new additions** selected, OmniPanel first records the existing library as a baseline. It waits for scanning to settle before checking for additions. Reopening an unchanged library, changing metadata, or removing a book does not trigger this mode.
- **Creator photos** come from available ComicVine person records associated with the issue’s credits. Portraits are cached. A creator can have a valid text credit without a verified photo, in which case the interface can show a placeholder.
- **Publisher logos** can be downloaded and kept for offline display. Long-press a publisher logo to supply a custom image. An available ComicVine item link opens the corresponding page.

## Page reading

| Setting | Choices and behavior |
| --- | --- |
| Reading direction | Read left to right or right to left. Set direction for an individual comic. |
| Page turns | Choose slide, page-turn, fade, stack, vertical-slide, or instant transitions. |
| Continuous reading | Scroll vertically or horizontally through successive pages. Adjust the gap between pages in scrolling modes. |
| Page fit | Fit screen, fit width, fit height, smart fit, stretch, fill and crop, or original size. Fit screen shows the page as a whole. Fit width is useful for reading a narrow page across the display. Fill and crop can trim edges to occupy the available area. |
| Printed margins | Automatically trim white or black borders from scans. Guided whole-page framing also checks proposed crops for visible art or small details near the edges. |
| Facing pages | Display two pages side by side. Keep the cover on its own when needed to align the following left/right pairs with the print edition. |
| Wide artwork | Split a spread in portrait, always split it, rotate the device, rotate the image, or show the whole spread. |
| Orientation | Follow the device, lock portrait, or lock landscape. Automatic landscape rotation for wide pages is available even with the reader orientation locked. |
| Background fill | Use the page-edge color, blurred artwork, black, white, or a custom color around the image. |

- **Pinch and double-tap zoom.** Spread two fingers to enlarge the visible artwork and bring them together to zoom back out. An oversized fitted page can shrink to show the whole page. Double-tap zoom can be disabled if you want a single tap to act immediately.
- **Scan and screen adjustments.** Optional sharpening helps with low-resolution scans. Follow system brightness or choose reader brightness, apply a warm-light tint, and keep the screen awake during reading.
- **Page numbers.** Hide the number, keep it visible, or display it for two seconds after opening or turning a page. Choose bottom center, top left, top right, bottom left, or bottom right.
- **Move between issues.** A long pull beyond the last page can open the next issue in the series. Pull back at the first page to open the preceding issue. The gesture previews its destination and has an adjustable pull distance. Navigation accounts for single-page issues.
- **Save the page.** In page view, **Save page** exports the complete current page.

## Guided panel reading

Switch to **Panel-by-panel view** in the reader controls, or set comics to open directly in panel view. Moving forward advances through detected regions in reading order. You can also choose to see the whole page before its individual panels.

| Detection mode | When to use it |
| --- | --- |
| Smart detection | Use gutters, drawn borders, and shapes together. The detector checks continuous boundaries and can recognize framed insets on dark pages. |
| Gutters only | Follow the spaces separating panels on pages with clear gutters. |
| Panel borders | Look for drawn boundaries on full-bleed artwork where gaps between panels are scarce. |
| Row mode | Glide down the page in full-width rows. Useful for an irregular composition or when you want a predictable path through the page. |

- **Sensitivity.** Choose **Only clear panels**, **Cautious**, **Balanced**, **Eager**, **Join speech-bubble panels**, or **Find every panel**. The more eager settings look for additional boundaries. Even the most sensitive setting can group panels with ambiguous borders.
- **Speech balloons across dividers.** The join option looks for a white balloon crossing a divider between side-by-side or stacked panels. It uses the shape of the printed page and can miss balloons or join regions differently from the artist’s intended sequence.
- **Keep art and captions in context.** A boundary check looks for a divider that stays in place, reducing false cuts through changing tones such as a highlight on a face. When separate inset panels leave art or captions outside their frames, guided view includes a page overview.
- **Fallback.** Select a whole-page view or scrolling rows for pages without confidently detected divisions. Splash pages, letters pages, overlapping panels, and borderless compositions can stay whole or appear in groups.
- **Frame the current panel.** Show the surrounding page, dim it by an adjustable amount, or hide it. The same five background fills used in page view are available, including blurred artwork around hidden surroundings.
- **Animate the transition.** Pick glide, zoom out/in, fade, slide, or instant movement and set the transition duration. On the whole-page view, optional outlines and numbers show the detected regions and their order.
- **Zoom within panel view.** Pinch outward or inward to inspect the artwork at a different scale.
- **Save a panel.** In panel view the export action becomes **Save panel**. Select a detected panel and export it as a PNG at the original exported page’s resolution. From a whole-page preview, enter a panel first.
- **Transition preparation.** Detection, joining neighboring regions, and preparing small blurred backgrounds happen outside transition drawing. Cached results can be reused as you move through the page.

## Reader menu, controls, and shortcuts

- **Open the menu.** Tap the menu zone to bring up reading controls and information for the current issue. The page behind the menu is dimmed by 80%, including behind the top and bottom controls. Closing the menu reveals the artwork at normal brightness.
- **Read issue details.** A scrollable column on the left shows the title, synopsis, available metadata and credits, and creator photos when available. Text is white and uses the selected theme’s font. On the right, the cover is scaled to fit in full. An available cached publisher logo appears beneath it. The information area leaves margins inside the reading controls.
- **Check your position.** The information view shows current page and total pages, identifies panel mode when active, and displays the time in Android’s preferred format. Turning a page updates the indicator independently. An issue with no synopsis displays **No synopsis available**.
- **Jump by thumbnail.** Use the page strip to move directly to a page. In Settings, choose **Compact — more pages**, **Standard**, or **Large pages**. Compact fits more thumbnails across the strip. Large gives each preview more space. Standard is the initial thumbnail size.
- **Reader artwork.** Cover images are decoded away from the main UI thread. Recent artwork and available portraits are cached. The information view follows the reader controls and is removed when the reader closes or the app pauses.
- **Touch controls.** Choose edge tap zones, half-screen zones, or menu-only tapping. Invert the zones to exchange the page-turn sides.
- **Physical controls.** Turn pages with the volume buttons and optionally swap their directions. Map supported keyboard, remote, controller, or volume-button input to next/previous panel or page, next/previous whole page, show/hide menu, toggle panel view, or close comic.
- **Reader shortcut bar.** Choose shortcuts for panel mode, animation, cropping, fit, reading direction, two-page mode, orientation, automatic rotation, background fill, and image export. Reading settings open in a full-screen overlay.

## Themes, settings, and credits

- **Fourteen themes.** Choose Modern, Terminal, Desktop 95, Synthwave, Holo HUD, Atomic Age, Golden Age Pulp, Manga Ink, Deco Noir, Blueprint, Grimoire, Sketchbook, Bauhaus, or Bubblegum. Themes change colors, fonts, shapes, and decorative details.
- **Light, dark, and system appearance.** Follow the system preference or choose light or dark appearance. Some themes define their own palette. Wallpaper-derived colors are optional. Pick an accent preset or a custom hue, and keep a separate accent choice for each theme.
- **Find a setting.** **Jump to settings group** offers Theme, Library appearance, Reading, Panel reading, Controls, ComicVine, Library management, Storage, and About. Large group headings use theme-specific rules. For example, Terminal and Blueprint use dashed separators, while Desktop 95 and Deco Noir use double rules.
- **Credits.** About credits OmniPanel to **jogra89**. OmniPanel was built with vibe coding. The bundled theme fonts include their SIL Open Font License notices.

## Device checks and practical limits

Guided reading and zoom were checked on a Galaxy Tab S9 FE+ using all 35 pages of *Midnight Fantastic Four #2*. The reader displayed 81 guided views in sequence. The dark footer on page 10 stayed visible, and page 31 showed the six drawn panels without splitting a conversation. On page 19, a pinch enlarged the artwork by 2.27× in both page and panel view and the reverse gesture returned to the original measured scale.

The same issue illustrates the limits of automatic detection. Thirteen pages had multiple guided views. Several irregular layouts stayed whole, and some inset frames shared a view. Other comics, device sizes, orientations, and settings combinations can produce different results. Creator photos, edition choices, publisher information, and other online details depend on what ComicVine supplies.
