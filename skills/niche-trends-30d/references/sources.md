# Sources

This skill ships no scrapers and no API keys. It is a method. You supply the access. Use official routes and your own account's view first, and check each platform's terms for what you are allowed to do with the data. Terms and rate limits change, and I have not verified the current terms of every platform, so confirm before you automate anything.

## Ways to get items, in the order to try them

1. **A collector you already have.** If you have [last30days](https://github.com/mvanhorn/last30days-skill) installed (MIT), let it run the niche query and give its output to step 2 of this skill. It already handles several of these networks. Keep only text, image and carousel items.
2. **Official APIs or search you have access to,** with your own keys.
3. **The platform's own search in your own logged-in view,** read manually or pasted by you. Sort by top or popular and set the date range if the network offers it.
4. **An export or a report you already have** (your analytics, a saved list).
5. **A licensed data provider,** if you use one.

If none is available for a network, say so in the report and skip it. Do not invent items, and do not fill the gap with remembered posts.

## What to collect per network

| Network | Look at | Engagement numbers to record | Notes |
|---|---|---|---|
| X | Search for niche keywords, top or popular, plus a few seed accounts | likes, reposts, replies, quotes, views if shown, follower count | Skip video. Quote posts count as the quoting text. |
| Bluesky | Keyword search and feeds for the niche | likes, reposts, replies | Smaller numbers than X, so compare only inside Bluesky. |
| Reddit | Top of the month in niche communities | upvotes, comments, upvote ratio if shown | Text and image posts only. Use for topic and structure, never as a source of facts. |
| Hacker News | Top and front-page stories from the window, plus "Show HN" | points, comments | HN has a free search API with points and comment counts. Self-posts and linked articles both count. |
| Instagram | Hashtag and account views for the niche, in your own view | likes, comments, saves if shown | Single images and carousels only, no Reels. There is no general public search API for this, so expect to use route 3 or 4. |

## Window

Last 30 days by default. Use the date of the post, not the date it was last seen. A post that peaked three months ago and was reshared yesterday is not a 30-day winner.
