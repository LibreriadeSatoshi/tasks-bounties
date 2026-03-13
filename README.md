# Bitcoin Course Bounties

We have several long-form Bitcoin classes (~2 hours each).  
We want to break them into **smaller, well-structured videos**.

Each bounty is for creating a **segmentation map** of a video so an editor can quickly:

- split the class into topic-based clips
- remove silences or setup time
- remove or isolate student questions
- identify clean clip boundaries

The goal is that someone editing the video **does not need to watch the full 2 hours again**.

---

## Videos


| #   | Video                  | Duration | Bounty  |
| --- | ---------------------- | -------- | ------- |
| 01  | [Bitcoin core principles - 2025/10/13](https://drive.google.com/file/d/1oKfM93tEa_3SGQwYgyJaNIaiUfIFnvY_/view?usp=sharing) | ~2h      | $AMOUNT |
| 02  | [Bitcoin core principles - 2025/10/15](https://drive.google.com/file/d/1fhQyeCfNHXes2Wp-4ZNpO-77zK3uLFh8/view?usp=sharing) | ~2h      | $AMOUNT |
| 03  | [Bitcoin core principles - 2025/10/20](https://drive.google.com/file/d/1dwo3CrepbdugHFmLzfPWn2mEZwZIPhpO/view?usp=sharing) | ~2h      | $AMOUNT |
| 04  | [Bitcoin core principles - 2025/10/22](https://drive.google.com/file/d/1GiuGxfl1Az7UOZcFotAHPNCKa1EBzULX/view?usp=sharing) | ~2h      | $AMOUNT |
| 05  | [Bitcoin core principles - 2025/10/27](https://drive.google.com/file/d/1iO06WGxKVINY-BPHI3_c6tjc_xvPiz2_/view?usp=sharing) | ~2h      | $AMOUNT |
---

# Task

Watch the video and create a **timeline describing what happens throughout the class**.

Your timestamps should allow an editor to clearly see:

- when a **topic starts**
- when a **topic ends**
- when **students ask questions**
- when there is **silence, setup time, or dead time**
- where **clean clip boundaries** exist

Think like an editor trying to split the video into **multiple smaller videos**.

---

# Output Format

Use a table with the following columns:


| Start | End | Type | Description |
| ----- | --- | ---- | ----------- |


Types:

- **Topic** — instructor explains a concept or section
- **Student** — student question or discussion
- **Silence** — pause, setup time, technical issues, dead air
- **Intro** — beginning of the class
- **Outro** — closing section

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


This structure should make it easy to see:

- what clips could be extracted
- what parts might be removed
- where the topics naturally divide.

---

# Quality Guidelines

A good submission should:

- Capture **every major topic**
- Clearly define **topic boundaries**
- Mark **all student questions**
- Mark **noticeable silence or dead time**
- Use **clear topic descriptions**

Typical topic segments should be **3–15 minutes long**.

Avoid:

- vague descriptions like "discussion continues"
- missing topic boundaries
- overly tiny segments

---

# How to submit

1. Pick a video from the table above.
2. Watch it and create your timeline table.
3. Open a **Pull Request** with your file in `submissions/<course-slug>/`.

---

# Submission Format

Submit a PR adding your file in the following structure:

`submissions/course-slug/video-01-2025_10_15.md`

---

# Bounty Payment

- Bounties are paid **per video**
- Payment happens **after review and approval**
- If multiple people work on the same video, the **first accepted PR receives the bounty**

