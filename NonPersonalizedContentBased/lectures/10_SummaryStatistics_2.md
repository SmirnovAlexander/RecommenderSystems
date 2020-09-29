# Example -- Reddit

- Social news aggregator
- Non-personalized news recommender
- Users vote to determine top item
- Provide with fresh and individual posts

# Displaying aggregate preferences

- Average rating / upvote proportion
    - of people who vote, or who liked
    - doesn't show popularity
- Net upvotes / # of likes
    - shows popularity
    - no controversy (doesn't show number of dislikes)
- % of people who rated more 4%
- Full distribution
    - are people generally like item or people are bipolar about item

# Goal of display

- Help users decide to buy / read / view the item
- What will help user decide


# Why not rank by score

- Too little data (one 5-star rating)
- Score may be multivariate (histogram)
    - not very intuitive
- Business
    - item is old
    - item is 'unfavored'


# Ranking Considerations

- Confidence
    - how confident are we that this item is good?
- Risk tolerance
    - high-risk, high-reward
    - high chance that user might very like this thing but also a chance that user may dislike it
    - conservative recommendation, only recommend if confident that item is good
- Domain and business considerations
    - age
    - system goals


# Damped means

- Problem: low confidence with few ratings
- Solution: assume that, without evidence, everything is average
- Ratings are evidence of non-averageness
- $$k$$ controls strength of evidence required, if it bigger then scores will be nearer to average
- $$\frac{\sum_{u}r_{ui} + k\mu}{n + k}$$


# Confidence intervals

- From the reading: lower bound of statistical confidence interval (95%)
- Choice of bound affects risk / confidence
    - lower bound in conservative: be sure it's good
    - upper bound is risky: there's a chance of amazing
- Reddit uses Wilson interval (for binomial) to rank comments


# Domain consideration: Time

- Reddit: old stories aren't interesting
    - even if they have many upvotes
- eBay: items have short lifetimes


# Scoring news stories

- Hacker News
    - $$\frac{(U-D-1)^{\alpha}}{(t_{now} - t_{post})^{\gamma}} \times P$$
    - $$\alpha$$ -- small polynomial decay factor (0.8), first upvotes are more valuable
    - $$\gamma$$ -- small polynomial decay factor (1.8) (gravity), if affects how fast rating lowers depends on age
    - $$P$$ -- penalty term, if an item is a poll, owner does not want it to have high score so we penalize it a little
    - on old posts age does not have impact
    - net upvotes, polynomially decayed by age
    - old items mostly by vote
    - multiplied by item penalty terms
        - incorporate community goals into score
- Reddit
    - $$log_{10} max(1, |U-D|) + \frac{sign(U-D) * t_{post}}{45 000}$$
    - $$log$$ for first upvotes are more valuable
    - $$t_{post}$$ -- time in seconds passed from 2005
    - buries items with negative votes
    - scores news items, not comments


# Ranking Wrap-Up

- There are some theoretically grounded approaches (confidence interval, damping)
- Many sites use ad-hoc methods
- Most formulas have constants, will be highly service-dependent
- Can manipulate for 'good' or 'evil'
    - good or bad is depends on reaction
- Build based on domain properties, goals


# Predict with sophisticated score

- Theoretically a fine thing to do
- Be careful with transparency / scrutability
    - if you say 'average rating' for damped mean, and show ratings, users may be confused
    - most important case (low ratings) also easiest to hand-verify


# Conclusion

- Sparsity, inconsistency, temporal concerns make data messy
- Simple scoring doesn't necessarily match the domain or business
- There are good ways to deal with this (decay, time, penalties, damping)
- Will see more normalizations
