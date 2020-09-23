# The Story of Zagat

- Collected opinions about restaurants
- Published summary and scores
- Became large restaurant review and rating empire
- Idea is to take contribution from all people


# Computing The Scores

- What should they mean
    - Popularity
        - McDonalds
    - Average Rating
        - Eating at home is really wonderful
    - Probability of You Liking
- How to compute
    - Frequency
    - Average
    - More complicated
- Mean of rating


# Breaking it Down

- Popularity in an Important Metric
- Averages can be misleading
    - can adjust by summing % who like
    - can adjust by normalizing user ratings
        - if somebody's all rating are low and other person's all ratings are high
    - consider credibility of individual raters (history of rating)
        - if somebody created account for promoting something
- More data is better to a point
    - Average, count, distribution


# What's missing here

- Who you are
    - when looking for a popular songs I may not looking for popular songs among 15-year-old girls
- Context
    - if ordering an ice-cream and want a recommendation for a sauce do I want to hear that ketchup is the most popular sauce


# Back to Zagat

Zagat getting worse

- Too many mediocre restaurants with good scores
- Too many excellent restaurants with mediocre scores

What's happening here

- Self-selection bias
    - only rates where you go
    - if previous year you went to restaurant and rated low you won't go there this year and rate for this year will be higher
- Increased diversity of raters
    - many people have different tastes


# Some take-away lessons

- Non-personalized popularity statistics or averages can be effective in right application
    - need to understand relationship between average and user need
    - correct average
- In many cases it can be best to show count, average and distribution together
- For ranking, one alternative to average is the percentage who score above a treshold
    - how many people who like this
    - or below
        - avoid items that have poor ratings
- Personalization can address many limitations
