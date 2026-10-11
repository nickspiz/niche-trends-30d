# niche-trends-30d

**A skill for Claude Code that finds what worked in your niche over the last 30 days, and turns the shape of it into your own posts without borrowing anyone's facts.**

![License: MIT](https://img.shields.io/badge/license-MIT-green)
![Works with Claude Code](https://img.shields.io/badge/works%20with-Claude%20Code-d97757)

I'm not a developer. When I started posting about what I make, I wanted to know what actually works in my niche, not what a blog post from 2022 says. Looking through feeds by hand takes hours, and a post with 5,000 likes in someone else's niche tells me nothing.

This skill is a method for doing it with an agent. It looks at the last 30 days on X, Bluesky, Reddit, Hacker News and Instagram. It only looks at text, single images and carousels. It scores posts against the niche they came from, throws out the noise, and then, if you ask, rewrites the winning structure into a post of your own.

The part I care about most is the last one: **the agent may copy how a post is built, never what it says.** No borrowed numbers, no borrowed stories, no invented experience.

## What it does

1. Collects posts from the last 30 days that match your niche, from whichever sources you can legitimately use.
2. Filters out off-niche posts, rumours, developer internals (if your audience is not technical), drama, giveaways, ads, duplicates and video.
3. Scores each post against other posts in the same niche on the same network, not by absolute likes.
4. Finds patterns in topic and in structure, and says how many posts support each one.
5. Reports with links, the numbers behind each score, and an honest "not enough evidence" section.
6. Adapts a winner into your post using only your facts file, with a table showing which fact supports each sentence.

## Example

Niche: indie apps for small shops. Audience: not technical. Facts file: three lines about a made-up product, Pinecone Shop.

The report (shortened, with made-up numbers for illustration):

```
Winners
1. 91  Bluesky  <link>
   Numbers: 212 likes, 40 reposts, 31 replies, sample 38
   Topic: a small feature that saves customers a step
   Structure: one-sentence opening, two short lines, no ending, no image

Patterns
- "One small feature, plain words, no pitch": 4 items, 3 authors

Dropped: off-niche 22, rumour 9, internals 14, bait 6, duplicate 5, format 31
```

Adapted draft, with its fact table:

> Saved carts are live in Pinecone Shop. Close the tab, come back tomorrow, the cart is still there.

| Sentence | Test | Fact |
|---|---|---|
| Saved carts are live in Pinecone Shop. | Fact | F1, changelog |
| Close the tab, come back tomorrow, the cart is still there. | Fact | F1 |

If a sentence has no fact behind it, it comes out.

## Install

As a Claude Code plugin:

```text
/plugin marketplace add nickspiz/niche-trends-30d
/plugin install niche-trends-30d@niche-trends-30d
```

Or copy the folder into your project:

```bash
git clone https://github.com/nickspiz/niche-trends-30d
cp -r niche-trends-30d/skills/niche-trends-30d .claude/skills/
```

## Use it

```text
What worked in my niche in the last 30 days? Niche: indie apps for small shops.
Audience is not technical. My facts are in facts.md.
```

It will ask for what is missing: the niche in one sentence, a few words that are in and out of it, and your facts file.

## What it does not do

- It does not scrape. There are no scripts and no API keys in this repo. You supply the access: your own keys, your own logged-in view, an export, or a collector you already trust. See `references/sources.md`. Platform terms differ and change, and I haven't verified every one, so check before you automate.
- It does not treat social posts as proof. A viral post tells you what people care about. It does not tell you what is true. Reddit threads and screenshots never become sources for a claim.
- It does not invent. If a winner depends on a story or number you don't have, it says so and moves on.

## Works well with

- [last30days](https://github.com/mvanhorn/last30days-skill), which can do the collecting if you want a ready-made engine. Hand its results to step 2 here.
- [social-post-skills](https://github.com/nickspiz/social-post-skills), for the form of each network and the final check of a draft.

## Credit

The idea of reading the last 30 days across several networks and ranking by what people reacted to comes from Matt Van Horn's [last30days-skill](https://github.com/mvanhorn/last30days-skill) (MIT). This repo contains none of its code or text. It is a separate, much smaller method with a different goal: one niche, text and image posts only, scoring relative to the niche, and a guard against invented claims. See [NOTICE](NOTICE).

## Questions and ideas

Have a question or an idea? Start a [discussion](https://github.com/nickspiz/niche-trends-30d/discussions). For mistakes, open an [issue](https://github.com/nickspiz/niche-trends-30d/issues/new/choose). See [CONTRIBUTING.md](CONTRIBUTING.md) before sending a pull request.

## Privacy

The plugin is plain-text instructions. It has no scripts and no hooks. The plugin itself reads no files, calls nothing and makes no network requests. It writes nothing and sends nothing to the author. Whatever Claude does while following it, such as searching the web or reading a file you point to, happens through the tools and permissions you already have in your session.

## Support

Questions or bugs: [GitHub Issues](https://github.com/nickspiz/niche-trends-30d/issues) or hello@nickspiz.com.

## License

MIT. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
