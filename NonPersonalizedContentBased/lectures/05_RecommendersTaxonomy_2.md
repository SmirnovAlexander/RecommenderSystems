# Basic model

- Users
    - attributes (demographic)
    - model (what book user like)
- Items
    - attributes (who was the author of book)
- Ratings
    - users meet items
- (Community)
    - space where all this opinions make space


# Non-Personalized Summary Stats

- External community data 
    - best-seller
    - most popular
    - trending hot
- Summary of community ratings
    - best liked
- Examples
    - billboard music rankings
    - tripadvisor hotel ratings
- Don't need info about users


# Content-Based filtering

- User Ratings x Item Attributes => Model
- Model applied to new items via attributes
- Knowledge-based
    - item attributes form model of item space; users browse that space
- Examples
    - i like movie1 and don't like movie2 => extracting attributes from items that you like and don't like (like genre action and lower score from romance; fan of some actor)
    - read news about vikings => get a lot of articles about vikings
- When user place a rating, user model updates in way which properties user liked / disliked (user model consists of items attributes)
- When it's time to recommend items we compare user model vector with items' vectors


# Personalized Collaborative Filtering

- Use opinions of others to predict / recommend
- User model -- set of ratings
- Item model -- set of ratings
- Common core: sparse matrix of ratings
    - fill in missing values (predict)
    - select promising cells (recommend)


# Collaborative Filtering Techniques

- User-user
    - select nighborhood of similar-taste people
        - variant: select people you know / trust
    - use the ratings from those like-minded users to calculate a prediction for the active user
    - "if there are other people who share my taste I will probably like items that they liked"
- Item-item
    - pre-compute similarity among items via ratings
    - find most similar items to already rated items
    - "people who rate item X highly, like you, also tend to rate item Y highly, and you haven't rated item Y yet, so you should try it"
- Dimensionality reduction
    - intuition: taste yields a lower-dimensionality matrix
    - compress and use taste representation
    - whole matrix reduced to much smaller (user's ratings vectors reduced to short taste vectors, every movie would be represented as a taste vector, we can match those vectors)


# Note on Evaluation

- Significant amount of time on evaluation
- Accuracy of prediction
- Usefulness of recommendation
    - correctness
    - non-obviousness
    - diversity
- Computational performance


# Other Approaches

- Interactive recommenders
    - critique-based
    - dialog-based
        - "hey, what you think about this item?"
        - "compare this items"
- Hybrid of various techniques
