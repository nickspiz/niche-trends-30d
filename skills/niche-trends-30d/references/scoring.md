# Scoring

Goal: find posts that did unusually well **for this niche on this network**, not posts that are famous.

## Per item

1. **Engagement raw** = the network's main signals added with weights that reflect effort:

   | Network | Formula |
   |---|---|
   | X | likes + 2 x reposts + 2 x replies + 2 x quotes |
   | Bluesky | likes + 2 x reposts + 2 x replies |
   | Reddit | upvotes + 2 x comments |
   | Hacker News | points + 2 x comments |
   | Instagram | likes + 3 x comments + 2 x saves (if shown) |

   Weights are a starting point. Change them if your niche behaves differently, and say you did.

2. **Engagement percentile** = where the item's raw engagement sits among all kept items from the same network, 0-100.

3. **Reach-adjusted percentile.** If follower counts are visible, divide raw engagement by followers (floor followers at 500 so tiny accounts do not explode the ratio) and take the percentile of that. A post that beat its author's usual audience says more about the post than about the author. If followers are not visible, use the engagement percentile again.

4. **Discussion depth** = replies or comments divided by likes or upvotes, as a percentile. Posts that start conversations are more useful as a model than posts that are only liked.

5. **Recency** = small bonus for the last 10 days. Never more than 5 points.

## Final score

```
score = 0.45 x engagement_pctile
      + 0.25 x reach_adjusted_pctile
      + 0.15 x discussion_depth_pctile
      + 0.10 x cross_source_bonus
      + 0.05 x recency_bonus
```

`cross_source_bonus` is 100 if the same topic (not the same text) shows up as a winner on a second network, 50 if it is above the median on a second network, else 0.

## Thresholds and confidence

- A **winner** is score at or above 80 and in the top 10% of its network's kept items.
- **Fewer than 20 kept items on a network:** do not compute percentiles. Rank by raw engagement, label the network "low confidence", and do not call anything a "pattern" from it alone.
- **A single huge account's post** that is far above everything else is an outlier. List it, but do not let it define a pattern alone.
- A pattern needs **at least 3 items** across at least 2 different authors.

## Show the work

In the report give each winner's raw numbers, the network sample size, and the final score. A reader must be able to see that "high" means "high compared to what".
