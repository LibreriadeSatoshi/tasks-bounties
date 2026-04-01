# Video segmentation

Produce a **segmentation map** of the source class video and a **finished edit** that matches it. The map must let a maintainer verify the edit against the raw file without rewatching the full recording.

## Videos


| #   | Video                                                                                                                      | Duration | Bounty  |
| --- | -------------------------------------------------------------------------------------------------------------------------- | -------- | ------- |
| 01  | [Bitcoin core principles - 2025/10/13](https://drive.google.com/file/d/1oKfM93tEa_3SGQwYgyJaNIaiUfIFnvY_/view?usp=sharing) | ~2h      | $AMOUNT |
| 02  | [Bitcoin core principles - 2025/10/15](https://drive.google.com/file/d/1fhQyeCfNHXes2Wp-4ZNpO-77zK3uLFh8/view?usp=sharing) | ~2h      | $AMOUNT |
| 03  | [Bitcoin core principles - 2025/10/20](https://drive.google.com/file/d/1dwo3CrepbdugHFmLzfPWn2mEZwZIPhpO/view?usp=sharing) | ~2h      | $AMOUNT |
| 04  | [Bitcoin core principles - 2025/10/22](https://drive.google.com/file/d/1GiuGxfl1Az7UOZcFotAHPNCKa1EBzULX/view?usp=sharing) | ~2h      | $AMOUNT |
| 05  | [Bitcoin core principles - 2025/10/27](https://drive.google.com/file/d/1iO06WGxKVINY-BPHI3_c6tjc_xvPiz2_/view?usp=sharing) | ~2h      | $AMOUNT |


## Task

1. Watch the **source** file for the row you claim.
2. Build a **segmentation table** (format below) that covers the full source timeline: topics, questions, silence, and intended cut points.
3. Edit the source into a **final video** that follows the table, **[Required video structure](https://github.com/LibreriadeSatoshi/tasks-bounties/tree/main/video-segmentation#required-video-structure)**, and **Editing rules**.

## Deliverables


| Deliverable  | Requirement                                                                   |
| ------------ | ----------------------------------------------------------------------------- |
| Edited video | Single master file, uploaded to Google Drive (or link agreed by maintainers). |
| Link         | Public or “anyone with link can view” URL to that file.                       |
| Markdown     | One `.md` under `video-segmentation/submissions/<course-slug>/<language>/` (path below). |


The markdown file must contain:

1. A single line with the edited video URL (`edited_video: <URL>`).
2. The segmentation table (required format below).

No extra metadata block is required.

## Official assets (maintainers)

Contributors **must** use only these assets for bumpers and caption language unless a maintainer posts an exception in the PR.

| Asset | Spec | Link |
| ----- | ---- | ---- |
| Intro / outro **music** | **Fixed** for all submissions: use only the file(s) linked here (same intro/outro audio every time). Use **full duration** of the 5 s bumper; fade in/out **0.5 s** unless the file metadata says otherwise. **No** substitute music. Do **not** list music in the submission header. | `[LINK — e.g. Drive/WAV or MP3]` |
| Intro **image** | Full-frame **1920x1080** (or match **Delivered master file** resolution below), **RGB**, `.png` or `.jpg`. Displays behind title text; keep **safe area** per template. | `[LINK]` |
| Outro **image** | Same technical rules as intro; end-card layout (logo, URL, next-lesson text as per template). | `[LINK]` |
| Optional **logo** / overlay | Use for bumpers only if linked here; same safe-area rules. | `[LINK or “none”]` |
| **Subtitle style** | Readable sans-serif, strong contrast, max **two lines** per cue, no overlapping cues, timing aligned to speech (not early by more than ~0.2 s or late by more than ~0.5 s without cause). | (policy text only) |

Replace the bracketed placeholders when files and language policy are finalized.

## Required video structure

### Intro (exactly 5 seconds)

- Placed at **file start**, before main class content.
- **Audio:** Official **intro music** only; peak loudness consistent with the rest of the edit (no clipping). If any spoken line appears on the bumper, duck music so speech is clearly intelligible.
- **Video:** Official **intro image** full frame; title text must include **course name** and **video title or date** matching the **Videos** table row.
- **Text:** Language of on-screen text = **subtitle language** (or bilingual only if maintainers allow it in the asset notes).

### Outro (exactly 5 seconds)

- Placed at **file end**, after main class content.
- **Audio:** Official **outro music** (or the same approved track as intro if only one file is provided); same loudness and fade rules as intro.
- **Video:** Official **outro image** full frame; required end-card elements per template (e.g. brand, link, call to action).
- **Text:** Same language rules as intro.

**Subtitles (main body):** Follow **Subtitle language**, **Subtitle delivery**, and **Subtitle style** in **Official assets**. The `<language>` folder in the submission path must match that language policy. Caption **all** speech in the main body (not music-only beds). Intro/outro on-screen text follows the same language unless **Official assets** allow bilingual bumpers.

**Delivered master file:** Single **MP4**, **H.264** video, **AAC** audio, **1920x1080** unless the source is lower resolution (then match source max), frame rate **match source**. Upload to Drive; link via `edited_video:` in the submission file.

## Editing rules

**Remove**

- Long dead air, slide setup, technical gaps, and repeated false starts unless pedagogically necessary.
- Silence that does not carry meaning (use judgment: under ~1–2 s between sentences may stay for natural pacing).

**Keep**

- All substantive instruction and worked examples.
- Every **student question** and the instructor’s answer, unless clearly inaudible or duplicate; if removed, note `REMOVED` in that row’s Description (see table rules).

**Pacing**

- Cuts must feel continuous: no jarring mid-word edits, level jumps, or visible flash frames.
- Normalize obvious volume spikes only if they harm listenability.

## Segmentation table (required format)

**Scope:** `Start` and `End` are **timecodes in the source file** for that video row (`00:00:00` through end of source). They describe what appears in the raw before your edit, not timecodes in the final export.

**Columns (exact names, order):**


| Column      | Rule                                                                                                                                                                                                                                                                                                         |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Start       | `H:MM:SS` or `MM:SS` (pick one style for the whole file and use zero-padding, e.g. `01:05:03` or `65:03`).                                                                                                                                                                                                   |
| End         | Strictly greater than Start; same time format as Start.                                                                                                                                                                                                                                                      |
| Type        | Exactly one of: `Intro`, `Topic`, `Student`, `Silence`, `Outro`. Use `Intro`/`Outro` only for segments that correspond to **in-source** class opening/closing; your 5 s bumper intro/outro are **not** listed here unless they replace source time (normally they are additive in the export only—see note). |
| Description | Single line, specific (who/what). No placeholders like “discussion”. If content is cut entirely, start with `REMOVED —` and briefly why.                                                                                                                                                                     |


**Structural rules**

- Rows are **chronological**. Adjacent rows should meet at boundaries (End of row N = Start of row N+1) except where you document a **jump cut** (then End of N < Start of N+1 and Description must say `Jump: source removed from … to …`).
- Cover the **entire** source from `00:00:00` to last frame; the last row’s End equals source duration.
- **Silence** rows: any continuous region you remove or would remove for pacing (even if you keep a sliver in the edit, the map still reflects the source span).
- **Student** rows: every distinct question; **Topic** rows: each instructional block.

**Note on bumpers:** The mandatory 5 s intro/outro exist **only** in the edited file. The segmentation table still maps the **full** source timeline; do not insert fake Start/End rows for bumpers.

Example (illustrative only):


| Start | End   | Type    | Description                             |
| ----- | ----- | ------- | --------------------------------------- |
| 00:00 | 01:40 | Intro   | Instructor introduction and overview    |
| 01:40 | 08:20 | Topic   | What is Bitcoin                         |
| 08:20 | 15:10 | Topic   | Blockchain basics                       |
| 15:10 | 17:00 | Student | Student asks about inflation vs Bitcoin |
| 17:00 | 32:40 | Topic   | Instructor explains monetary inflation  |
| 32:40 | 33:20 | Silence | Instructor setting up slides            |
| 33:20 | 45:05 | Topic   | Mining and proof of work                |
| 45:05 | 47:10 | Student | Student question about mining           |
| 47:10 | 58:00 | Topic   | Mining economics                        |


## Quality bar (segmentation)

- Every **major** topic change has its own **Topic** row or boundary.
- **Student** and **Silence** rows are complete
- Descriptions are reviewable in under a few seconds per row.

## Definition of done

A submission is complete when **all** are true:

- One PR adds exactly one new markdown file at the path below.
- Submission file starts with `edited_video: <URL>` and includes the segmentation table in the required format.
- Segmentation table satisfies **Segmentation table (required format)**.
- Edited file meets **Official assets**, **Required video structure**, and **Editing rules**.
- Maintainer can play the edited video and spot-check random table rows against the source without ambiguity.

## How to submit

1. Choose one row from **Videos** (first merged PR per `#` wins).
2. Complete **Definition of done**.
3. Open a PR adding one file at:

   `video-segmentation/submissions/<course-slug>/<language>/video-XX-YYYY_MM_DD.md`

   - `<course-slug>`: lowercase, hyphenated course id.
   - `<language>`: lowercase **BCP 47** tag matching captions (e.g. `en-us`, `es-419`). Must match the subtitle language and chosen localization for this submission.

   Example: `video-segmentation/submissions/bitcoin-core-principles/en-us/video-01-2025_10_15.md`

Payment is per merged, accepted submission after review.
