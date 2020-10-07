# Demographics: What and Why?

- Motivation
    - popularity may not represent tastes
    - user may be part of group with different tasted
        - age
        - gender
        - race / ethnicity
        - socio-economic status
        - location
    - including non-demographics that may be predictive


# How

- Identifying available demographics and correlates
    - many will require processing or bucketing
    - age divided into groups
    - postal codes can be transformed into socio-economic status, urban / rural, dominant ethnicity, etc
- Explore correlation between data and demographics
    - scatterplots, correlations


# If found relevant demographics

- **Step 1:** break down summary statistics by demographic
    - e.g. most popular item for woman, for men
    - maybe even factorial (most popular item for men 45-60)
- **Step 2:** consider a multiple regression model
    - predict items based on demographic statistics
        - linear regression for multi-valued (e.g. rating) data
        - logistic regression for 0 / 1 (e.g. purchase) data


# Important

- You need defaults for unknown demographics
    - may be overall preferences
    - may reflect expected demographics of newcomers
    - may be modeled separately
- If demographics is useful, getting data on users is key
    - data got from registration
    - various sources of data, from advertising networks to loyalty club sign-ups and surveys
    - in some cases, demographics can be predicted from the data


# Power and Limits

- In many cases, demographics work because products or content is created to reach them:
    - television programs
    - magazine articles and advertisements
    - personal products
- Products simply naturally appeal to different groups
- Demographics fail miserably for people whose tastes don't match their demographics
    - products appeal to all demographics
    - never perfect
