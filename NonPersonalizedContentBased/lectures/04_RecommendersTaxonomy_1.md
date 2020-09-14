# Domains of Recommendation

- Content to commerce and beyond
    - news, information, "text"
    - products, vendors, bundles (we can give you a deal if you buy X, Y together)
    - matchmaking (other people)
    - sequences (e.g. music playlist, order matter)
- One property
    - New items (never experienced before, e.g. movies, books)
    - Re-recommend old ones (e.g. groceries, music)


# Purpose of Recommendation

- The recommendations themselves 
    - sales
    - information
    - we want to consume, buy, listen, etc
- Education (how important is to learn commands in program depending on commands usage frequency by others' users, hotel rates website helps making decision)
- Building community (by helping become loyal to source)


# Recommendation Context
    
- What is the user doing at the time of recommendation
    - shopping
    - listening to music
    - hanging out with other people
- How does context constrains recommender
    - bad example is if after every song pop ups a recommendation
    - if system knows that you are hanging out with other people it may make recommendation for groups


# Whose Opinion

- Recommender systems in a broad sense based on somebody's opinion
    - experts
    - everybody
    - people like you


# Personalization Level

- Generic / Non-Personalized
    - everyone receives same recommendations
- Demographic
    - matches a target group
- Ephemeral
    - match current activity
- Persistent
    - match long-term interests


# Privacy and Trustworthiness

- Who knows what about me?
    - personal information revealed
    - does it have to know who I am, identity
    - is there is a way I can deny these preferences
- Is the recommender honest?
    - biases built-in by operator
        - "business rules", does not recommends things that are out of stock and says "hey, go to this shop this item is in stock there"; don't sell a thing without a high markup; don't recommend something that person will buy anyway
    - vulnerability to external manipulation (hacking ratings; objectivity of ratings: e.g. new movie have high scores because people who reviewed movie as soon as it was released were really waiting for it so it is most likely that they will leave positive review)
    - transparency of recommenders
    - reputation


# Interfaces

- Types of output 
    - predictions
    - recommendations
    - filtering
    - organic vs. explicit presentation
        - systems presents itself as an agent
        - acting as search engine or a tool
- Types of input
    - explicit
    - implicit


# Recommendation Algorithms

- Non-Personalized summary statistics
- Content-based filtering
    - information filtering
    - knowledge-based
- Collaborative filtering
    - user-user
    - item-item
    - dimensionality reduction
-Others
    - critique / interview based recommendations
    - hybrid techniques
