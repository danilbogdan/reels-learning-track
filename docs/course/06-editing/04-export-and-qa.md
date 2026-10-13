# Lesson 6.4: Export and quality check

**English** | [Русский](../../ru/course/06-editing/04-export-and-qa.md)

**Time:** 35 minutes

## Goal

Export a file that the platforms will display cleanly, and run a short quality check before posting.

## Export settings

Platforms re-compress what you upload, so give them a clean file. Exact requirements change; treat these as safe defaults and verify against the platform's current guidance.

| Setting | Safe default |
|---|---|
| Aspect ratio | 9:16 (vertical) |
| Resolution | 1080 x 1920 |
| Frame rate | Same as the project: 30 fps |
| Container | MP4 |
| Video codec | H.264 |
| Bitrate | A high-quality preset in your editor; for H.264 around 8-16 Mbps for 1080p is a common range |
| Audio codec | AAC, 44.1 or 48 kHz, stereo |
| Audio bitrate | 128-192 kbps |

Avoid exporting at lower resolution than the original unless the file is too big.

### Watermarks and borders

Instagram lists a visible watermark from another app, borders and low resolution among things that reduce Reels reach ([source](https://about.instagram.com/blog/announcements/instagram-ranking-explained)). Therefore:

* Export from your editor **without** a watermark. Some free editors add one unless you change a setting or pay.
* Don't re-upload a video you downloaded from another platform with its logo.
* Fill the frame; avoid black bars or decorative frames.

## Loudness

Different parts of the internet use different loudness standards. For short social video, a commonly used target for overall loudness is around -14 to -16 LUFS integrated, with peaks not above -1 dB. This is general practice, not an official platform rule. Many editors have a loudness meter or a normalize function. With ffmpeg, one pass can approximate it:

```
ffmpeg -i in.mp4 -af loudnorm=I=-16:TP=-1.5:LRA=11 -c:v copy out.mp4
```

This copies the video and normalizes the audio. Check by ear that the voice is clear and not distorted.

## The cover

The cover (thumbnail) is the image shown on your profile grid and in some placements. Choose a frame with a clear face or clear text, good light and a closed mouth. Add short text only if it helps. With ffmpeg you can extract a frame:

```
ffmpeg -ss 00:00:03 -i out.mp4 -frames:v 1 cover.jpg
```

Some platforms allow selecting a frame inside the app.

## Quality check

Before every post, go through this list. Watch on your phone, full screen, with headphones, then again muted.

**Picture**

* [ ] Vertical, fills the frame, no black bars or foreign watermark.
* [ ] Face is sharp and well lit; exposure is stable.
* [ ] Nothing in the background reveals private details (lesson 2.3).
* [ ] Cuts are clean; no flash frames.

**Sound**

* [ ] Speech is clear and the right volume.
* [ ] No clicks at cuts, no distracting hum.
* [ ] Music is quiet and legal.

**Text**

* [ ] Captions are correct and in the safe zone.
* [ ] On-screen text is readable and stays long enough.

**Content**

* [ ] The hook is in the first second.
* [ ] One promise, delivered.
* [ ] The ending is clean; no dead air or long outro.
* [ ] Length is intentional.

**Legal and honesty**

* [ ] I have the right to use all footage, music and images.
* [ ] If it is an ad, partnership or gifted product, I will label it (lesson 9.2).
* [ ] The claims in it are true.

## The cooling-off rule

If you can, wait 30 minutes between finishing the edit and posting. Come back and watch once more. This catches mistakes that tired eyes miss: a typo in a caption, a private detail on a screen, a flat ending.

## Archive

After export, keep:

* The final video.
* The project file.
* The raw footage (until you are sure you won't need it).
* A line in your log: date, title, hook, length.

You'll need these when you review your analytics.

## Common mistakes

* **Exporting at low quality to save space.**
* **Leaving the editor's watermark.**
* **Skipping the muted check.**
* **Posting directly after editing.**
* **Not keeping a log.**

## Exercise

1. Create an export preset with the defaults above.
2. Export your reel. Check specs (use your editor's info panel or ffprobe).
3. Run the quality check and fix at least one issue.
4. Extract or choose a cover.

## Daily practice

* **Minimum (keeps the streak):** a voice note of any length.
* **Today's take (about 30 seconds):** Film, export with your preset and run the quality check.
* Weeks 1-2 everything stays private; from week 3 follow your publishing plan.
* Don't watch the take right away (lesson 4.1). Tick the day in your tracker.

## Checklist

* [ ] I have a saved export preset.
* [ ] My export has no watermark or borders.
* [ ] I ran the quality check.
* [ ] I have a cover and a log entry.
* [ ] I recorded today's voice note and take.

## Sources

* Instagram: [ranking explained](https://about.instagram.com/blog/announcements/instagram-ranking-explained)

---

[← 6.3: Captions, music and sound design](../06-editing/03-captions-music-sound.md) | [Course index](../README.md) | [7.1: Posting mechanics →](../07-publishing/01-posting-mechanics.md)
