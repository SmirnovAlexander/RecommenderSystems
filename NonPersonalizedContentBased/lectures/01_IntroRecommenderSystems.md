# History
 
- Early recommender systems
    - Help you making choices based on someone else's experience
        - caveman not eating harmful plants;
    - Emergence of critics
- Information retrieval
    - Static content base
        - investing time in indexing content
    - Dynamic information need
    - Common approach TFIDF (e.g. BM25)
- Information filtering
    - Static information need
        - invest time in modeling user needs
        - hand-created "profiles"
        - feedback
    - Dynamic content base
    - Pass new content through filters
    - e.g. subscription on category
- Collaborative filtering
    - Do not only want content by topic but want those that are really good on this topic
    - Tapestry: adding comments so you can create queries like `SHOW news WITH TOPIC topic WHICH user RATED high`
    - Active CF: manually create distribution groups (subscribe and unsubscribe)
- Automated CF
    - First system known as recommender system
    - ACF for Usenet News
        - users rate items
        - users are correlated with others
        - personal predictions for unrated items
    - NN Approach
        - find people with history of agreement
        - assume stable tasted
    - Significantly more accurate than predicting average or modal rating


# Recommenders

- Tools for identifying worthwhile stuff
    - Filtering interfaces
        - e-mail filters, clipping sevices (subscriptions)
    - Recommendation interfaces
        - suggestion lists, "top-n" list, offers and promotions
    - Prediction interfaces
        - predicted rating (4.5 hotel score predicted)


# Vocabulary

- Rating: expression or preference
    - Explicit (direct from user, e.g. rate the film)
    - Implicit (inferred from user activity, e.g. stop watching movie after 5 min)
- Prediction: estimate of preference
- Recommendation: selected items for user
- Content: attributes, text, etc; everything about item
- Collaborative: using data from other users


# Recommendation approaches

- Non-Personalized and stereotyped
    - Popularity
    - Group preference (age / gender personalizations)
- Product association
    - People who liked X also liked Y
    - Not personalized
    - Shopping basket analysis
- Content-based
    - Learn what user liked in terms of attributes and match it to items that have these attributes
- Collaborative
    - Learn what user liked and use others' experience to recommend


# Designing a recommender

- Collect opinion and experience data
    - Purchasing behavior
    - User rates
    - Items tags
- Find relevant data for a purpose
- Compute recommendations
- Present data in a useful way


# Recommenders as big data

- Heavy emphasis on analysis and evaluation
    - Exploring data to determine best recommendation approaches
    - Choose metrics to measure efficiency
    - Metrics designed to improve business goals
    - Choose algorithms to optimize performance against metrics
- Continuing adoption of ML techniques
