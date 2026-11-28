# OmniPanel

<img src="omnipanel-logo-white.png" alt="OmniPanel logo" width="176">

OmniPanel is a free comic reader for Android and Windows 11. Open a local comic, read the whole page or follow its panels, and pick up where you left off. Your comics stay in the folders you choose.

**[Download OmniPanel 1.0.28 for Android](https://github.com/jogra89/OmniPanel/releases/download/v1.0.28/OmniPanel-1.0.28.apk)** · [Android feature list](https://github.com/jogra89/OmniPanel/releases/download/v1.0.28/FEATURES.md) · [Release notes](https://github.com/jogra89/OmniPanel/releases/tag/v1.0.28)

## Windows 11 x64

[**Install OmniPanel for Windows · Preview 8 (.exe)**](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.8/OmniPanel-Windows-1.0-preview.8-setup-x64.exe) · [Portable ZIP](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.8/OmniPanel-Windows-1.0-preview.8-x64.zip) · [Source ZIP](https://github.com/jogra89/OmniPanel/releases/download/windows-v1.0-preview.8/OmniPanel-Windows-1.0-preview.8-source.zip)

Setup installs OmniPanel for your Windows account and adds it to Start. The portable ZIP runs after you extract the entire archive and open `app/OmniPanel.exe`. Both include the .NET runtime. Read local comics and PDFs, match editions on ComicVine, and switch between guided panels, full pages, spreads, and continuous scrolling. [Full Windows feature guide, changes and test results](https://github.com/jogra89/OmniPanel/releases/tag/windows-v1.0-preview.8) · [GitHub release](https://github.com/jogra89/OmniPanel/releases/tag/windows-v1.0-preview.8)

## Start reading on Android

1. On a device running Android 8.0 or later, download and open the signed APK. If prompted, allow the browser or file manager you used to install it.
2. Open OmniPanel and add a folder containing your comics. It reads CBZ, CBR, CB7, CBT and PDF files, and you can add more than one folder.
3. Tap a cover to start reading. Tap the center of a page with the default controls to see the cover, issue details, thumbnails and reader shortcuts. Select panel view to move through the artwork one panel at a time.

## What you can do

- **Browse your collection.** Explore folders and subfolders, or browse by series, creator, character, publisher, story arc and tag. Open a random comic, hide individual items and restore them later, or browse PDFs in their own optional section.
- **Choose how you read.** Turn pages in either direction, scroll continuously, or read two-page spreads. Pinch to zoom, adjust the page fit, or choose among 14 themes.
- **Follow the panels.** Detect gutters, borders and inset frames. Tune the sensitivity, choose a transition and decide how much surrounding artwork stays visible. Export a whole page or an individual panel.
- **Identify an issue.** Read embedded comic metadata or search ComicVine with your own API key. Compare covers, publishers and dates before you choose an issue or collection. The reader can show its synopsis, credits, publisher logo and available creator photos.
- **Track your reading.** Resume from Continue Reading, mark comics as read, and sort folders or series by total page count.

Local reading works offline. ComicVine searches and image downloads need internet access. Credits and portraits depend on the metadata and images available for each issue. [Explore all supported features](https://github.com/jogra89/OmniPanel/releases/download/v1.0.28/FEATURES.md)

## Tested on Android

Version 1.0.28 was tested on real issues in single-page mode. Six forward and six reverse swipes moved exactly six pages in each direction on both Danger Jane and Cyberpunk 2077: Jayk’s Case. Marvels page 14 has a full-page overview and four tall painted panels. Page 24 has an overview and two full-height insets.


On a Galaxy Tab S9 FE+, OmniPanel 1.0.24 displayed all 35 pages of *Midnight Fantastic Four #2* in order through 81 guided views. Pinch zoom enlarged the artwork 2.27× in both reading modes and returned it to its original size. In 1.0.27, device tests also verified forward and reverse issue pulls, four-direction panning on a magnified page, and a live first-opening ComicVine lookup. On some irregular pages, the reader keeps overlapping panels together or shows the whole page. [Device and build checks](https://github.com/jogra89/OmniPanel/releases/download/v1.0.28/TESTING.md)

## Build materials and credits

OmniPanel was built with **vibe coding**. Development combined natural-language direction, AI-assisted coding and testing on a physical tablet. The release includes a rebuild kit and SHA-256 checksums for both the kit and the signed APK. [Rebuild kit](https://github.com/jogra89/OmniPanel/releases/download/v1.0.28/OmniPanel-1.0.28-rebuild-kit.zip) · [Checksums](https://github.com/jogra89/OmniPanel/releases/download/v1.0.28/SHA256SUMS.txt)

The APK includes third-party components and fonts. Consult their bundled notices for the applicable license terms. ComicVine is a third-party service.
