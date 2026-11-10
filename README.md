# Little Steps

An independent Goblin Tools-inspired prototype, built in vanilla HTML, CSS, and JavaScript. “Little Steps” and the sprout mascot are placeholders for future branding.

## Run locally

No install or build step is required. From this directory:

```sh
python3 -m http.server 5173 --bind 127.0.0.1
```

Open http://127.0.0.1:5173. Hash routes work with any static server, without rewrite configuration.

## Implemented

- Responsive nine-tool home grid and individual tool pages
- Light/dark themes and a dismissible announcement
- Locally saved tasks, editing, custom nested steps, completion filters, undo/redo, and clearing completed tasks
- JSON backup import (adds to the current list), JSON and Markdown exports
- Focus timer linked to unfinished steps; start/pause/reset/skip/complete
- Local text-replacement, tone-cue, task-extraction, estimate, and decision-worksheet demos
- Sample leap-year explanation and fried-rice recipe
- Accessible labels, keyboard focus, modal dialogs, reduced-motion support, safe text rendering

## Prototype boundaries

There is no AI API, server, account system, payment, or cross-device sync. Tool pages explicitly describe their local rules or sample-only behavior. Task breakdown uses small editable templates. Timer pauses on leaving the focus page and resets on reload. Tasks/theme persist in localStorage; drafts only live in memory. No external scripts, fonts, or analytics are loaded.

## Change the placeholders

Edit `branding.js` for the name, wordmark, tagline, and mascot path. Replace `assets/mascot.svg` for the character. Tool definitions and demo handlers live in `app.js`; design tokens and responsive styles are in `styles.css`.

Reference: https://goblin.tools/. This project is independent and does not reuse its logo or proprietary backend.

## Polymer learning demo

The home page now centers a five-section polymer course and education tools. Judge, Consultant, Chef, and the generic Professor/Formalizer entries are removed from navigation. The original task and focus tools remain.

- `learning.js`: curated lesson content, browser speech, interactive chain and DP models, section progress, highlights, notebook, custom flashcards, confidence capture, question feedback, and retry of missed questions.
- `learning.css`: responsive learning layouts using the existing pink/green palette.
- `assets/polymer-synthesis.pdf`: supplied eight-page source, available through page-specific links and a reader.
- Instructor demo: selects learning objectives for a sample assignment in this browser only. It does not enroll students or sync with an LMS.

Notes are made on the guided lesson text, not inside the original PDF. The five-question bank and sample flashcards are curated, not AI-generated at runtime. Retry targets missed questions; this is not a full adaptive difficulty engine. Browser speech playback depends on installed voices. The handout references supplementary video but no video files were supplied. The separate Canvas presentation mentioned in the brief was not provided or used.

### Reference inspection

Reviewed Norton's public InQuizitive introduction and illustrated student guide, rather than an authenticated course. Adopted the patterns of learning objectives, question feedback, confidence reflection, and returning to source material. The notebook and guided lesson implement the user's requested extensions.

- https://knowledgebase.wwnorton.com/help/inquizitive-instructors-introduction
- https://knowledgebase.wwnorton.com/help/inquizitive-students-vg-how-to

### Verification

Checked JavaScript syntax, assignment selection, saving notes, note-to-card creation, card reveal and self-rating, interactive DP calculation, saved highlights and section restoration, question feedback, and missed-question review in the browser. Checked all six learning routes at 390, 768, and 1920 pixels with no horizontal overflow. Audible voice output is device-dependent and was not independently verified.
