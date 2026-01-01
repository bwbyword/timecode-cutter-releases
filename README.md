<p align="center">
  <img src="https://github.com/bwbyword/Timecode-Cutter/blob/main/public/icon.png" alt="App Icon" width="170" height="170">
</p>

<h1 align="center">Timecode Cutter</h1>

<p align="center">
  <img src="https://img.shields.io/badge/version-v1.4.4-blue.svg" alt="Version v1.4.4">
</p>

<p align="center">
  A powerful, cross-platform desktop application for automatically cutting and merging video files based on timecodes. <br>
  Streamline your workflow with CSV imports, NLE exports, and a visual timeline.
</p>



## Features

-   **Video Import**: Drag & drop support for easy video loading.
-   **Flexible Timecode Input**: Supports `MM:SS`, `HH:MM:SS`, and range formats (e.g., `00:00 - 01:30`).
-   **Smart Hint Overlay**: Interactive, non-intrusive guide overlay for timecode formatting that disappears when typing.
-   **CSV Import**: Import timecodes via CSV file (Drag & Drop or Button). Supports `start, end, [caption]` format.
-   **Keep / Remove Modes**: Toggle between keeping selected segments or removing them (inverting selection).
-   **Smart Sorting & Merging**: Automatically sorts new timecodes chronologically and merges overlapping segments.
-   **Caption Support**: Add captions to timecodes (e.g., `00:05 - 00:10, My Caption`). Captions are exported as subtitles (`.srt`) and NLE metadata.
-   **Global Timecode Display**: Moved the large timecode display to the center of the top bar for better visibility.
-   **Editable Timecode**: You can now click the timecode in the top bar to type a specific timestamp (e.g., "01:20:00") and jump instantly to that frame.
-   **Cancel Pending In-Point**: Clicking "In Set" again will now cancel the pending in-point operation, improving usability.
-   **Visual Annotations**:
    -   **Draw & Text**: Add freehand drawings, arrows, rectangles, and text labels directly onto video segments.
    -   **Segment-Specific**: Annotations are bound to specific clips, ensuring they only appear when relevant.
    -   **Interactive Editing**: Drag, move, and right-click to delete annotations.
-   **Image Overlays & Watermarks**:
    -   **Global Overlays**: Add a persistent overlay (logo/watermark) that appears throughout the entire video.
    -   **Segment Overlays**: Attach specific images to individual video segments (e.g., lower thirds, slides).
    -   **Visual Editing**: Drag, resize, and position overlays directly in the preview window with 1:1 aspect ratio accuracy.
    -   **Burn-In Rendering**: Overlays are high-quality burned into the exported MP4 using FFmpeg (resolves video/audio streams automatically).
    -   **FCPXML Export**: Overlays are exported as valid connected clips in `.fcpxml` for Final Cut Pro.
-   **Auto-Validation**: Real-time validation of timecodes to prevent overlaps and format errors.
-   **Visual Timeline**: 
    -   16:9 Video Preview with local streaming.
    -   Visual representation of "kept" (green) vs "removed" (gray) segments.
    -   Multi-line Filmstrip with generated thumbnails.
    -   Interactive selection and seeking.
-   **Smart Processing**: Automatically cuts and merges video segments using FFmpeg.
-   **Professional Export**: 
    -   **Rough Cut Export**: Generate EDLs or FCPXML files.
    -   **NLE Support**: Optimized for DaVinci Resolve, Premiere Pro, and Final Cut Pro.
    -   **Gap Management**: Option to Close Gaps (continuous timeline) or Preserve Gaps (maintain spacing).
-   **Detailed Captions**: Comments from your CSV/Text import are carried over to the NLE as markers or sidecar subtiles.
-   **Smart EDL**: Automatically detects source start timecode to ensure perfect synchronization in Resolve (fixes "extents do not match" errors).
-   **Subtitle Export**: Automatically generates a sidecar `.srt` file alongside EDLs for easy captioning in NLEs.
-   **Professional UI**: Timecode display (HH:MM:SS:FF), dark mode, and responsive layout.
-   **Progress Tracking**: Real-time progress bar and inline success notifications.
-   **Customizable Settings**: Configure output file location (Source, Downloads, or Ask Every Time).

## Installation

### Prerequisites
-   Node.js (v16 or higher)
-   npm or yarn

### Steps
1.  Clone the repository:
    ```bash
    git clone https://github.com/bwbyword/Timecode-Cutter.git
    cd Timecode-Cutter
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

3.  Start the development server:
    ```bash
    npm run dev
    ```

## Building for Production

To create a distributable application (DMG for Mac, NSIS for Windows):

```bash
npm run build
```

The output files will be located in the `dist` directory.

## Tech Stack

-   **Electron**: Cross-platform desktop framework.
-   **React**: UI library.
-   **Vite**: Fast build tool and dev server.
-   **Tailwind CSS**: Utility-first CSS framework.
-   **FFmpeg**: Powerful multimedia framework for video processing.
-   **TypeScript**: Type-safe JavaScript.

## License

[GPL-3.0](LICENSE)
