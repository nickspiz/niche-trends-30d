---
name: niche-trends-30d
description: Find what actually worked in a niche over the last 30 days on X, Bluesky, Reddit, Hacker News and Instagram (text, image and carousel posts only), score it against the niche, drop off-topic noise, rumours and developer internals, and adapt the winning structures into new posts built only from the user's own facts. Use when asked what is trending or working in a niche, what to post about, or to turn a viral post's shape into our own post.
---

# Niche trends, last 30 days

Finds the posts that did unusually well in one niche, explains why they worked, and turns the shape of the best ones into your own posts without borrowing their facts, stories or words.

Social posts here are a signal of what people care about and how it was told. They are never a source of facts. A fact in your post comes from your facts list or an official source.

Read `references/sources.md`, `references/scoring.md`, `references/filters.md` and `references/adapt-guard.md` as you reach each step. If the `post-basics` skill from social-post-skills is installed, use it for the form and the final check.

## Inputs

Ask for these. Do not start without 1 and 3.

1. **Niche** in one sentence, plus 5-10 words that are in it and 5 that are not. ("Indie apps for small shops. Not: crypto, dev tooling.")
2. **Networks** to look at. Default: X, Bluesky, Reddit, Hacker News, Instagram.
3. **Facts file** about the user's own product: what is true, with sources. Needed for step 6 only, but ask now.
4. **Audience:** non-technical (default) or technical. It decides what counts as "dev internals".
5. **Window:** default the last 30 days. Today's date goes in the report.
6. Optional: seed accounts, communities and keywords to start from.

## Steps

### 1. Collect

Per network, gather posts from the last 30 days that match the niche. **Text, single image and carousel posts only.** Skip video, Reels, live and audio. Use the means the user actually has and is allowed to use (see `references/sources.md`). Do not bypass logins or limits. Aim for 30-100 items per network. Fewer is fine, and is reported as low confidence.

Record for each item: network, URL, author, date, format, the text, and every engagement number the network shows (likes, reposts, replies, upvotes, points, comments), plus the author's follower count if visible.

### 2. Filter

Apply `references/filters.md`. Drop and log, with a one-word reason: off-niche, rumour, dev internals (when the audience is non-technical), drama or outrage, bait and giveaways, ads, duplicates, wrong format.

### 3. Score against the niche

Apply `references/scoring.md`. Engagement is compared inside one network and one niche, never across networks and never in absolute numbers. A post with 400 likes can be ordinary in one niche and exceptional in another.

### 4. Find the patterns

For the top items, name what they have in common, in two layers:

- **Topic:** what people reacted to.
- **Structure:** opening type, number of beats, length, how it ends, whether it had an image and what kind, whether it asked a question.

Say how many items support each pattern. One post is an anecdote, not a pattern.

### 5. Report

Use the format in `references/adapt-guard.md`, section "Report". Include the filtered-out count and the low-confidence notes. If nothing clears the bar, say so plainly and stop. A thin month is a result.

### 6. Adapt (only when asked)

For each chosen winner, write our post:

1. Keep the **structure** (opening type, beats, length, ending type, image type).
2. Fill it with **our facts only**.
3. Run the invented-claims guard in `references/adapt-guard.md` and show the table mapping each sentence to a fact.
4. If the winner depends on a story, a number or an experience we do not have, **do not fake an equivalent**. Pick another winner or another structure.

### 7. Hand off

Pass the adapted drafts to the network skills for form, then the final human-writing pass. Competitor and trend posts are at most about 1 in 4-5 of the output; the rest of the content is about the product.

## Never

- Never copy wording. No run of five or more words from a source post, and no quoting except a short clearly attributed phrase with a link.
- Never use the winner's numbers, names, customers or story as ours.
- Never turn a hedge into a fact ("testing" into "launched").
- Never treat a viral post, a Reddit thread or a screenshot as proof of a claim.
- Never present adapted structure as an original idea in the report. Credit the pattern with the link.
- Never collect anything the user is not allowed to collect, or anything behind a login you were not given.
