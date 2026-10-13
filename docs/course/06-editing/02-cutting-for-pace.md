# Lesson 6.2: Cutting for pace

**English** | [Русский](../../ru/course/06-editing/02-cutting-for-pace.md)

**Time:** 50 minutes

## Goal

Learn to tighten a talking video so it feels fast and clear: remove pauses, fix stumbles, trim beats and use cuts to keep attention.

## Pace is a decision

When you watch a good short video, you rarely notice cuts. You notice that nothing is wasted. Pace is the number of ideas per second. A talking video filmed in one take usually contains about 20-30 percent slack: pauses, breaths, stumbles, restarts, repetition. Cutting them makes the same content feel energetic without making you talk faster.

## The cutting passes

### Pass 1: Choose takes

Select the best take for each beat. Usually the last, but not always. Criteria: clear words, good energy, eye line on lens. Make a rough sequence.

### Pass 2: Cut the start and end of each clip

Remove the "ready, set" at the beginning and the exhale at the end. Cut a few frames before you speak and a few frames after you finish. Leave about 3-5 frames of room (a tenth of a second) so speech does not feel clipped.

### Pass 3: Remove pauses

Silences between sentences are the main source of slack. Rules of thumb:

* Between sentences: leave about 0.1-0.3 seconds, or none for a punchy feel.
* Before an important word or a turn: keep a short pause (0.3-0.6 seconds) for effect.
* Delete long pauses, thinking gaps and false starts.

This technique of removing silences creates **jump cuts**: instant jumps in the video where the person's head or body shifts slightly. Jump cuts are normal and accepted in short video. Hide the jump with a punch-in or b-roll if it bothers you.

### Pass 4: Fix stumbles and fillers

* Remove "um", "uh" and false starts, if the cut is clean.
* Keep some natural fillers for authenticity; not every "like" needs removing.
* If a stumble lands in the middle of a word, re-record rather than cut.

### Pass 5: Check the beats

Play the whole reel and note where your attention drops. Cut or tighten that section. If the middle drags, ask: can this beat be shorter, or can I drop it?

### Pass 6: Add variation

If you hold the same framing for more than about 5-8 seconds, consider a change: a punch-in, a cutaway to b-roll, a text card, a change of angle. Variation resets attention. Do not add changes for the sake of change; use them at idea boundaries.

## Finding silences with ffmpeg

To list silent stretches in a clip (useful for tracking where to cut):

```
ffmpeg -i clip.mp4 -af silencedetect=noise=-35dB:d=0.4 -f null - 2>&1 | grep silence_
```

It prints start, end and duration of silences quieter than -35 dB and longer than 0.4 seconds. Adjust the `noise` level for your room tone. Many editors also have an "auto-remove silences" feature; treat auto-cuts as a first pass and review them, since they can chop breaths awkwardly and remove deliberate pauses.

## Targets for length

Keep your actual finished length in mind:

* Aim to remove at least 15 percent from your raw take.
* Your finished reel should have no sentence that does not serve the promise.
* Most reels in the early weeks fall in the 15-40 second range. Use your data later (lesson 7.2) to decide.

## Rhythm and music

If you add music (lesson 6.3), you can align cuts roughly to the beat, but speech rhythm matters more than music rhythm. Don't force a talking video to a beat.

## Audio cuts: J-cuts and L-cuts

A **J-cut** starts the audio of the next shot before the picture changes. An **L-cut** keeps the audio of the previous shot after the picture changes. Both make cuts feel smooth. Example: while b-roll of a laptop appears, you continue speaking (audio from the talking shot), and then you reappear. Practice with b-roll.

## Common mistakes

* **Cutting too tight,** so breaths vanish and speech sounds robotic.
* **Leaving long pauses** because the take felt natural.
* **Adding transitions** to hide poor cuts.
* **Cutting audio at a noise peak,** causing clicks. Use short fades (a few frames) at cut points.
* **Not reviewing on a phone.** Watch the result at phone size.

## Exercise

1. Take your rough cut. Do passes 2-5.
2. Note the length before and after. Calculate the percentage removed.
3. Add one cutaway or punch-in at an idea boundary.
4. Watch the final cut on your phone with headphones, and again with the sound off.

## Daily practice

* **Minimum (keeps the streak):** a voice note of any length.
* **Today's take (about 30 seconds):** Film, then cut it with passes 2-5. Note the percentage removed.
* Weeks 1-2 everything stays private; from week 3 follow your publishing plan.
* Don't watch the take right away (lesson 4.1). Tick the day in your tracker.

## Reading (optional)

This week's book, about 15-20 minutes: Austin Kleon, *Show Your Work!*. A loose suggestion; it does not have to match the lesson. More in [resources](../../resources.md) and the [schedule](../schedule.md).

## Checklist

* [ ] I removed pauses and false starts.
* [ ] I varied the picture at least once in a longer reel.
* [ ] My cuts have no clicks or clipped words.
* [ ] I watched it on a phone.
* [ ] I recorded today's voice note and take.

---

[← 6.1: Editing workflow and tools](../06-editing/01-workflow-and-tools.md) | [Course index](../README.md) | [6.3: Captions, music and sound design →](../06-editing/03-captions-music-sound.md)
