# Short summary

**English** | [Русский](ru/summary.md)

This is a cheat sheet. The full material is in the [course](course/README.md).

## 1. Accounts and niche

* For Instagram an account of the Creator type fits: analytics, scheduling posts, the full music library. Business accounts are limited to commercially licensed music. Source: [Buffer](https://buffer.com/resources/instagram-account-type/).
* Start with one platform for 3-4 weeks, then add a second.
* A niche for a personal brand does not have to be one topic. You need a recurring thread that tells the viewer why to watch you in particular. Pick one angle for the first 10 videos and see what lands.
* For monetization a small devoted audience can be enough: Kevin Kelly's essay [1000 True Fans](https://kk.org/thetechnium/1000-true-fans/).

## 2. Ideas and video structure

The platforms say what they measure.

* [TikTok](https://newsroom.tiktok.com/en-us/how-tiktok-recommends-videos-for-you/): a strong interest signal is watching a longer video from beginning to end. Follower count and past high-performing videos are not direct factors.
* [Instagram](https://about.instagram.com/blog/announcements/instagram-ranking-explained): for Reels the system predicts whether people will watch to the end, like, share or visit the audio page. Reach is reduced by low resolution, watermarks, no sound, borders, mostly text, and content already posted on Instagram.

How to find ideas:

1. Collect 20 videos in your topic that you clicked and watched to the end.
2. For each, write down the first line, first frame, promise to the viewer, the turn and the ending.
3. Pick 3-5 recurring patterns and rework them with your own story.
4. Do not copy someone else's video word for word.

## 3. Filming on iPhone and editing

* Recording format: Settings - Camera - Formats. High Efficiency (HEVC) saves space, Most Compatible (H.264) is more widely compatible. Source: [Apple](https://support.apple.com/en-us/HT207022).
* When importing to a computer, files may be converted to H.264. To keep originals, turn on Keep Originals in the photo settings.
* iPhone video is often recorded with variable frame rate, which causes sync drift in editing. Convert to constant frame rate before editing. This is general practice, not from official documentation. Example:

```
ffmpeg -i in.MOV -c:v libx264 -crf 18 -r 30 -c:a aac out.mp4
```

* General practice: vertical 1080x1920, 30 fps, light from a window in front or to the side, a lavalier mic or a quiet room.
* Editing: CapCut, DaVinci Resolve, ffmpeg, Instagram's built-in editor.

## 4. Posting and analytics

* Keep the caption short and on topic. Hashtags are there to signal the topic. Work out how many to use from your own data.
* TikTok counts captions, sounds and hashtags as information about the video.
* Keep other platforms' watermarks out of the frame: Instagram says they reduce reach.
* Look not at total views but at where people drop off: retention in the first 3 seconds, average watch time, completion rate, shares, saves.
* Keep a table: hook, length, retention, completion.

## 5. Monetization

* Ways to earn: sponsored integrations, your own products and services, platform bonuses and subscriptions (on Instagram for Creator accounts).
* Do not sell ads until views are stable. Price by the rates of comparable creators and by the expected views of your last 10 videos.
* Taxes depend on the country and the form of business. For Poland there are overviews: [Solidna Księgowa](https://solidnaksiegowa.com/ryczalt-dla-tworcy-internetowego/) and [iFirma](https://www.ifirma.pl/blog/rozliczenie-podatkowe-influencera/). According to them, barter (goods or services instead of money) counts as income, and the ryczałt rate for advertising services can differ from the rate for other services. This is a summary of articles, not tax advice: check your own case with an accountant.

## 6. Being on camera

Speaking on camera is trained by the number of takes.

1. Do 3-5 takes of each line and use the last one: the first takes are almost always stiff.
2. Write talking points (3-4 items), not a script. Memorized text sounds unnatural.
3. Talk to one person: picture an acquaintance who needs this.
4. One take solves one problem. Do not think about light, speech and angle all at once.

These are general techniques, not from a specific method.
