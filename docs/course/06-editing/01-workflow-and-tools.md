# Lesson 6.1: Editing workflow and tools

**English** | [Русский](../../ru/course/06-editing/01-workflow-and-tools.md)

**Time:** 50 minutes

## Goal

Set up a repeatable editing pipeline from raw footage to a finished file, pick tools that fit you, and avoid common technical traps.

## The pipeline

Every edit, whatever the tool, follows the same steps:

1. **Ingest:** copy the footage to your computer and back it up.
2. **Normalize:** convert to an editing-friendly format (constant frame rate).
3. **Rough cut:** pick the best takes and put them in order.
4. **Tighten:** remove pauses, mistakes and slack (lesson 6.2).
5. **Add layers:** b-roll, captions, music, sound design (lesson 6.3).
6. **Polish:** color, audio level, transitions, cover.
7. **Export and check** (lesson 6.4).

Doing the steps in this order prevents wasted work. Don't add captions or music before the cut is final.

## Choosing a tool

You do not need professional software. Choose by where and how you edit.

**On the phone:**

* Instagram's and TikTok's built-in editors: quick, good for simple edits, with direct publishing.
* Free or low-cost mobile editors like CapCut: auto-captions, templates, effects, easy cutting.

**On the computer:**

* **DaVinci Resolve (free version):** professional features, steeper learning curve, strong color and audio tools.
* **CapCut desktop:** the same style as mobile with a bigger screen.
* **Other options:** many free or paid editors exist; the best one is the one you will actually open every day.

**Command line:**

* **ffmpeg:** a free tool for converting, trimming, joining and processing video and audio. It is powerful for batch tasks and fixing format problems, and it is less suited to creative timeline work. Many creators use ffmpeg to prepare files and a visual editor to cut.

Start with one tool. Learn it deeply enough to cut, caption and export without searching. Switching tools frequently is a form of procrastination.

## Normalize: avoiding variable frame rate problems

Phone videos often use variable frame rate (VFR). Some editors and tools mishandle it, producing audio drift, frozen frames or stutters. A safe habit is to convert to a constant frame rate (CFR) at the start. With ffmpeg:

```
ffmpeg -i input.MOV -vf "fps=30" -c:v libx264 -crf 18 -preset medium -pix_fmt yuv420p -c:a aac -b:a 192k -movflags +faststart output.mp4
```

What it does: `fps=30` sets a constant 30 frames per second; `libx264` with `crf 18` creates a high-quality H.264 file; `yuv420p` ensures wide compatibility; `aac` encodes the audio; `faststart` moves metadata to the front for quick playback.

Notes:

* Match the fps to what you filmed (30 or 60).
* This re-encodes the video, which takes time and a small quality cost. `crf 18` keeps it visually close to the original.
* If you filmed in HEVC and your tool struggles with it, this also converts to H.264.
* Keep the originals; work on the converted copies.

To convert a whole folder (Linux or macOS shell):

```
mkdir -p cfr
for f in *.MOV; do ffmpeg -i "$f" -vf "fps=30" -c:v libx264 -crf 18 -preset medium -pix_fmt yuv420p -c:a aac -b:a 192k "cfr/${f%.*}.mp4"; done
```

## Project setup in your editor

* Create a **vertical project**: 1080x1920 at 30 fps (match your footage).
* Import the converted files.
* Create a sequence from your best take.
* Save the project with a clear name and the date.
* Turn on auto-save.

## Editing hygiene

* **Keep a template project** with your caption style, safe-zone guides and export preset. Duplicate it for each reel.
* **Use keyboard shortcuts.** Learn five: play, cut/split, delete, undo, zoom.
* **Work in short passes.** One pass for cuts, one for audio, one for captions.
* **Save versions.** `v1`, `v2`, `final`.
* **Limit time.** Aim for 30-45 minutes per reel once you are practiced. If you spend three hours on 20 seconds, the idea or the process needs simplifying.

## What good editing is

Good editing is invisible. The viewer should notice the idea and the emotion, not the effects. Resist heavy transitions, flashy filters and constant zooms. The most important edit is the simplest: **remove what does not help.**

## Common mistakes

* **Starting with captions.** The cut will change.
* **Editing the raw VFR file** and chasing sync bugs.
* **Choosing a tool by features rather than comfort.**
* **Overediting.**
* **Losing originals.**

## Exercise

1. Pick one editing tool and install it.
2. Convert your test footage to CFR.
3. Create a vertical template project.
4. Rough-cut one reel: pick the best takes and order them. Do not polish yet.

## Daily practice

* **Minimum (keeps the streak):** a voice note of any length.
* **Today's take (about 30 seconds):** Film, convert it to constant frame rate and import it into your editor.
* Weeks 1-2 everything stays private; from week 3 follow your publishing plan.
* Don't watch the take right away (lesson 4.1). Tick the day in your tracker.

## Reading (optional)

This week's book, about 15-20 minutes: Austin Kleon, *Show Your Work!*. A loose suggestion; it does not have to match the lesson. More in [resources](../../resources.md) and the [schedule](../schedule.md).

## Checklist

* [ ] I chose one editor.
* [ ] I convert footage to constant frame rate before editing.
* [ ] I have a vertical project template.
* [ ] I know the seven pipeline steps.
* [ ] I recorded today's voice note and take.

---

[← 5.5: B-roll, shot lists and batching](../05-filming/05-broll-and-batching.md) | [Course index](../README.md) | [6.2: Cutting for pace →](../06-editing/02-cutting-for-pace.md)
