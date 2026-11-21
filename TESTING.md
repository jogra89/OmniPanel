# OmniPanel 1.0.24 for Android · Test results

The full-issue reading test used a physical Samsung Galaxy Tab S9 FE+ (SM-X610) with a 1600 × 2560 display. Captured views were matched against the original pages of *Midnight Fantastic Four #2*.

## Guided reading

| Check | Observed result |
| --- | --- |
| Read from cover to back page | All 35 pages appeared in order across 81 guided views. Thirteen pages had multiple stops. |
| Small details near a page edge | Page 10 kept its full height, including the footer. |
| A shaded face inside a wide panel | Page 31 followed six drawn panels and kept the conversation together. |
| Intricate layouts | Pages 9 and 15–18 displayed whole. Page 24 grouped several insets. |
| End of issue | The single back page displayed in full. |

## Pinch zoom

On page 19, an outward two-finger pinch enlarged the artwork 2.27× in ordinary page view and in guided panel view. An inward pinch returned the artwork to its starting scale in each mode.

## Build checks

Android's APK signer verified the v2 and v3 signatures. The native libraries passed 16 KiB alignment checks. Host tests covered library visibility, folder navigation, reader-menu transitions, metadata matching scope, page geometry, panel order and inset framing.

The full-issue walkthrough covers one comic on one tablet. Borderless artwork and overlapping or irregular panels may appear together. Creator photos require a matched issue with available images. Other Android devices, collections, orientations and setting combinations can give different results.
