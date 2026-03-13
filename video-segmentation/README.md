# Video segmentation

Create a **segmentation map** of a long-form class video so an editor can split it into clips, remove silences, and isolate sections. The goal: the editor **does not need to watch the full video again**.

## Videos

| #   | Video                  | Duration | Bounty  |
| --- | ---------------------- | -------- | ------- |
| 01  | [Bitcoin core principles - 2025/10/13](https://drive.google.com/file/d/1oKfM93tEa_3SGQwYgyJaNIaiUfIFnvY_/view?usp=sharing) | ~2h      | $AMOUNT |
| 02  | [Bitcoin core principles - 2025/10/15](https://drive.google.com/file/d/1fhQyeCfNHXes2Wp-4ZNpO-77zK3uLFh8/view?usp=sharing) | ~2h      | $AMOUNT |
| 03  | [Bitcoin core principles - 2025/10/20](https://drive.google.com/file/d/1dwo3CrepbdugHFmLzfPWn2mEZwZIPhpO/view?usp=sharing) | ~2h      | $AMOUNT |
| 04  | [Bitcoin core principles - 2025/10/22](https://drive.google.com/file/d/1GiuGxfl1Az7UOZcFotAHPNCKa1EBzULX/view?usp=sharing) | ~2h      | $AMOUNT |
| 05  | [Bitcoin core principles - 2025/10/27](https://drive.google.com/file/d/1iO06WGxKVINY-BPHI3_c6tjc_xvPiz2_/view?usp=sharing) | ~2h      | $AMOUNT |

## Task

Watch the video and create a **timeline** with:

- when a **topic starts** and **ends**
- when **students ask questions**
- **silence, setup time, or dead time**
- **clean clip boundaries**

Think like an editor splitting the video into smaller videos.

## Output format

Table with columns: **Start** | **End** | **Type** | **Description**

Types: **Intro** (start of class), **Topic** (concept/section), **Student** (question or discussion), **Silence** (pause, setup, dead air), **Outro** (closing).

Example:

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

## Quality guidelines

- Capture **every major topic** and **topic boundaries**
- Mark **all student questions** and **noticeable silence/dead time**
- Use **clear topic descriptions**. Typical segments **3–15 minutes**
- Avoid vague descriptions, missing boundaries, or overly tiny segments

## How to submit

1. Pick a video from the table above.
2. Create your timeline table.
3. Open a PR with your file at:  
   `video-segmentation/submissions/<course-slug>/video-XX-YYYY_MM_DD.md`  
   Example: `video-segmentation/submissions/bitcoin-core-principles/video-01-2025_10_15.md`

First accepted PR per video gets the bounty.
