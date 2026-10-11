# Filters

Run these before scoring. Log each dropped item with one word: `off-niche`, `rumour`, `internals`, `drama`, `bait`, `ad`, `duplicate`, `format`. Report the counts.

## Off-niche

Compare each item with the niche sentence and the in-and-out word lists from the inputs. A post that went viral on an adjacent topic does not belong, however big it is. When in doubt, drop it. A mislabelled viral post wrecks a pattern more than a missing one.

## Rumour

Drop posts whose main content is:

- a leak, an "insider says", "reportedly", "sources say", "I heard", with no official source linked;
- a single user's complaint about a product, presented as a general fact;
- a prediction stated as news;
- screenshots of something with no link to the original.

Reddit complaint threads are in this group by default. They can show that a topic is discussed. They cannot support a claim.

A post that links an official announcement, documentation, a pricing page or a published study is not a rumour. Keep it, and note the source.

## Developer internals (audience: non-technical)

Drop posts whose point depends on code, tooling or infrastructure: framework choices, config, prompts-as-code, deployment, tool comparisons for developers, "my stack", benchmarks only developers read. Keep posts about outcomes, decisions, money, customers and process that a non-developer understands.

If the audience is technical, skip this filter, but keep the rumour filter.

## Drama and outrage

Drop pile-ons, personal feuds, politics, and posts whose engagement is anger at a person. They score high and teach the wrong lesson.

## Bait and giveaways

Drop "comment X to get Y", follower-for-follower threads, giveaways, "like if you agree", engagement pods, and anything that clearly asks for the engagement it received.

## Ads and promo

Drop paid posts and obvious promotion of the author's own product, unless the user asked to study competitors, in which case keep them labelled `competitor`.

## Duplicates

When the same text appears more than once, keep the earliest and drop the rest. When many people repost one idea in their own words, keep the best one and note the count as cross-source evidence.

## Wrong format

Drop video, Reels, live, audio-only, and posts where the text does not carry the idea without the missing media. Keep text, single image and carousel.

## Also drop

Deleted or unavailable posts, posts older than the window, anything adult or unsafe, anything that requires a login you were not given.

## False positives

Do not drop a post only because it contains a hard word, a number, or a link. Do not drop a post because it criticises something, if the criticism is a reasoned one about a confirmed fact.
