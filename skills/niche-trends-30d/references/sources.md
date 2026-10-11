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
| Hacker News | Top and front-page stories from the window, plus "Show HN" | points, comments | Self-posts and linked articles both count. |
| Instagram | Hashtag and account views for the niche, in your own view | likes, comments, saves if shown | Single images and carousels only, no Reels. Check what Meta's current API allows for hashtag search; if it does not fit your case, use route 3 or 4. |

## Public access, in general terms

This is a pointer, not a summary of the terms. Read the platform's current API terms before collecting, and check what applies to your account and your use.

- **X:** the X API is documented at https://docs.x.com. Access, pricing and the Developer Agreement and Developer Policy are described there.
- **Bluesky:** the AT Protocol is an open protocol with public documentation at https://docs.bsky.app. Different services have different rate limits, so read the current rate-limit page.
- **Reddit:** access to Reddit data through the API requires approval under Reddit's Responsible Builder Policy (https://support.reddithelp.com/hc/en-us/articles/42728983564564-Responsible-Builder-Policy); commercial use needs separate written approval. Data API Terms: https://redditinc.com/policies/data-api-terms.
- **Instagram:** Meta's Instagram API offers hashtag search to apps with the required access and permissions, with query limits. Read https://developers.facebook.com/docs/instagram-platform/instagram-graph-api/reference/ig-hashtag-search.
- **Hacker News:** public data API at https://github.com/HackerNews/API; a search API is documented at https://hn.algolia.com/api.

## Window

Last 30 days by default. Use the date of the post, not the date it was last seen. A post that peaked three months ago and was reshared yesterday is not a 30-day winner.

Checked 11.10.2026 against: https://docs.x.com/developer-guidelines, https://docs.bsky.app/docs/advanced-guides/rate-limits, https://support.reddithelp.com/hc/en-us/articles/42728983564564-Responsible-Builder-Policy, https://developers.facebook.com/docs/instagram-platform/instagram-graph-api/reference/ig-hashtag-search, https://github.com/HackerNews/API
