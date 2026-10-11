# Sources

This skill ships no scrapers and no API keys. It is a method. You supply the access. Use official routes and your own account's view first, and check each platform's terms for what you are allowed to do with the data. Terms and rate limits change, and I have not verified the current terms of every platform, so confirm before you automate anything.

## Ways to get items, in the order to try them

1. **A collector you already have.** If you have [last30days](https://github.com/mvanhorn/last30days-skill) installed (MIT), let it run the niche query and give its output to step 2 of this skill. It already handles several of these networks. Keep only text, image and carousel items.
2. **Official APIs or search you have access to,** with your own keys.
3. **The platform's own search in your own logged-in view,** read manually or pasted by you. Sort by top or popular and set the date range if the network offers it.
4. **An export or a report you already have** (your analytics, a saved list).
5. **A licensed data provider,** if you use one.

If none is available for a network, say so in the report and skip it. Do not invent items, and do not fill the gap with remembered posts.

## Data-access terms by platform

| Platform | Public API | Restrictions | Notes |
|---|---|---|---|
| **X (Twitter)** | X API v2 | Academic Research tier requires non-commercial affiliation with academic institution; Commercial/Premium requires paid Developer account; free tier very limited | Post IDs may be shared for peer review of academic research only with X written approval |
| **Bluesky** | AT Protocol (free) | Rate limits: 5,000 points/hour, 35,000 points/day per account; OAuth recommended | No cost, points-based system, all data is publicly accessible |
| **Reddit** | Closes March 31, 2027 | Public API ending 2027; requires OAuth 2.0; Data API requires paid agreement for commercial use or ML training | New access stopped Oct 31, 2026; unregistered apps lose access Jan 12, 2027; migration to paid platform required |
| **Instagram** | Graph API (limited) | Requires App Review; hashtag search restricted to 30/rolling 7 days, last 24 hours only; no arbitrary hashtag or user search | Only for business/creator accounts; Business/Creator Instagram account required tied to approved Meta App |
| **Hacker News** | Free search API | No authentication required; points and comment counts available | Self-posts and linked articles both count; published research available |

## Window

Last 30 days by default. Use the date of the post, not the date it was last seen. A post that peaked three months ago and was reshared yesterday is not a 30-day winner.

Checked: X API docs (developer.x.com), Bluesky AT Protocol docs, Reddit API announcement (Oct 2026), Instagram Graph API docs, Hacker News API
