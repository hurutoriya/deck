---
marp: true
class: invert
paginate: true
---

![bg opacity](https://yhatt-marp-cli-example.netlify.com/assets/gradient.jpg)

# Introducing "Challenges and research opportunities in eCommerce search and recommendations"

Speaker: [@hurutoriya](https://shunyaueta.com/) 🎰
Date: 2021-07-07

---


# What & Why this paper?

This paper is SIGIR Forum Article. Authors are organizers of SIGIR eCom. It well summalized research history at eCommerce search & recommendation domain.

> SIGIR eCom will bring together practitioners and researchers from academia and industry to discuss the challenges and approaches to product search and recommendation in eCommerce.

[Paper link in Amazon Science](https://www.amazon.science/publications/challenges-and-research-opportunities-in-ecommerce-search-and-recommendations)


---

# Aspects of eCommerce search and discovery

1. Customer goal
2. Business goal
3. Data logistics 

# Three eCommerce research areas

1. Matching and ranking
2. Coversational search
3. Fairness, confidentiality and transparency

We focus on `Matching and ranking` in this talk.

---
# Unique points of product search

Product search has two main stakeholders whose interests cooprate but also compete.

1. Customers
    - `Cooperation`: Need what businesses offer
    - `Compete`: Want to find the best quality at the cheapest price
2. Business owners
    - `Cooperation`: Need cistomer purchases to survive
    - `Compete`:  Want to maximize profit


---
# Customers

Customers visit eCommerce sites to accomplish a goal.

## Goals

1. `simple`: e.g. buying a coffee machine
2. `complex` e.g. fixing a hole in the wall

saerch queries and interactions → Customer intents → Customer Journeys

---
# Query intent

## web search queries intent

navigational, informational, transactional

## eCommerce search queries intent
-  [User Intent, Behaviour, and Perceived Satisfaction in Product Search](https://dl.acm.org/doi/10.1145/3159652.3159714), WSDM2018
    -  target finding, decision making, and exploration.
-  [A Taxonomy of Queries for E-commerce Search](https://dl.acm.org/doi/10.1145/3209978.3210152), SIGIR2018 by walmart
    - shallow exploration, targeted purchase, major-item shopping, minor-item shopping, and hard-choice shopping

---
# On-site customer journey

- Customers journey via funnel
    1. broad queries
    2. refinements queries
    3. examining multiple products before decision making

>  [Returns to Consumer Search: Evidence from eBay](https://dl.acm.org/doi/10.1145/2940716.2940754), Economics and Computation 2016

- Large portion of eCommerce customer journeys are initially exploratory, recommendations are valuable.
- Search becomes more important once the customer has shaped their view of what they want.

---
# Global customer journey

- The customer journey can span multiple sites and offline interactions

- Propose a substitute product system to avoid a zero hit result
    1. Access to knowledge outside of what is available in the catalog
    2. Access to the global state of customer journey
 
 >  [Leading Conversational Search by Suggesting Useful Questions](https://www.microsoft.com/en-us/research/publication/leading-conversational-search-by-suggesting-useful-questions/), WWW2020

---
![bg opacity](https://yhatt-marp-cli-example.netlify.com/assets/gradient.jpg)

# Business

Customer satisfaction is important for business, but is only one of the many criteria that a business needs to track towards the goal of optimizing profit 💰

---
# Sales strategies and short- and long-term effects

- `cross-selling`: Enticing customers to buy additional products
- `up-selling`: Tempting customers to buy a more profitable version of a product
- `down-selling`: Encouraging customers to buy by matching their budget

e.g. Business Push the down-sell to sell the items which is lower-quality and cheaper.

- short term: earn the profit
- long term: mayy customers not to return in the future.

## cross-sell approach

backfill the SERP with recommendations result that related to saerch result.

---
# Brand image and inventory.

e.g. example of Amazon

> An interesting challenge in the Fashion Store is the discrepancy between what the majority of customers actually buy and what they want to see on top of the page. The item most commonly bought for the query ”diamond ring” might be a cheap zirconium ring. However, if we show the zirconium ring as a first result, our search will be perceived as broken. Besides, our Fashion Store would look like a flea market, instead of a classic department store where the latest collections meet you at the entrance.

> To approach this problem, we identify strategic categories of fashionable customers — customers who bought or added to cart fashion brand products — and significantly amplify their influence while designing the training set.

> [Amazon Search: The Joy of Ranking Products](https://www.amazon.science/publications/amazon-search-the-joy-of-ranking-products), RecSys2016

---
# Online marketing and ranking

- eCommerce search engines include business logic that reflects marketing decisions

# Offline marketing and ranking

- eCommerce businesses having both online and physical presences creates a unique blend of organizational and infrastructure challenges.

---
# Regulatory and business restrictions

Regulatory and business constraints govern which products can be shown to which customers. 

-  most eCommerce sites have business logic at the time of checkout
to determine whether a product can be purchased and shipped to a given customer

e.g. 
- only adults can view or buy certain products.

---
![bg opacity](https://yhatt-marp-cli-example.netlify.com/assets/gradient.jpg)

# Data logistics

Data plays a key role in product search and recommendations. Services where the eCommerce website has multiple vendors bring in dynamics with regards to quality and consistency of the content, fraud detection, and pricing

---
# Third party content.

- Some eCommerce sites such as Amazon, Taobao, and eBay serve as a place for other companies to sell products.
- The data for the third party
products may need to be reformatted or supplemented before indexing.

e.g. 
- if the brand of the product is not provided as structured data by the vendor, it may be possible to extract it from the product title

---
# Volatile inventory

- One of the biggest challenges of eCommerce search and recommendation is that the inventory is constantly changing.

e.g. eBay
- new item need to be added quickly in the index.
- offline store inventory and online inventory must be synced in real-time
- Query suggestions are also affected by volatile inventory as they may suggest queries that no longer return results, creating a frustrating user experience.

> [The Architecture of eBay Search](http://sigir-ecom.weebly.com/uploads/1/0/2/9/102947274/ebay_search_architecture.pdf), SIGIR eCom2017.

---
# Multi-modal documents

In eCommerce search, the indexed documents, i.e., 
the products customers are looking for, are combinations of images, unstructured text such as titles, descriptions, and reviews, and structured data such as price, brand, ratings, and seller location

![bg right 90%](./imgs/etsy.png)

---
![bg opacity](https://yhatt-marp-cli-example.netlify.com/assets/gradient.jpg)

# eCommerce research area deep dives

1. design of matching and ranking for eCommerce search.
2. deep dive into conversational eCommerce that has promise to enable the smooth shopping experience provided by expert shop assistants
3. We discuss issues of fairness, confidentiality and transparency which are at the heart of maintaining customer trust while providing personalized eCommerce experiences.

---
![bg opacity](https://yhatt-marp-cli-example.netlify.com/assets/gradient.jpg)

# 1. Relevance: Matching and ranking
---
# Matching

- Navigational ones (a serial number)
    - Need exact matches to product serial numbers, product titles or category names
- Long informational ones (are batteries included with this watch)
    - Need semantic parsing and more elaborate indexing before they can be answered
- Some queries may require a different user interface; for example a tabular layout is better for answering comparison queries
---
# Relevance
- Origin of definition: Relevance was considered a universal, dimensionless quantity
- Now: Not to be universal but instead user dependent

eCommerce relevance is context-dependent and it has four dimensions

1. customer
2. time
3. query
4. contect (e.g. category)


---
# Matching queries and products

- eCommerce search is as much about exploration as it is about finding the best exact match
- may need careful crafting of synonyms to match a customer’s vocabulary to that of the business

>  - [A Taxonomy of Queries for E-commerce Search](https://dl.acm.org/doi/10.1145/3209978.3210152) WSDM2018 by walmart/
>  - [Why Do People Buy Seemingly Irrelevant Items in Voice Product Search?](https://www.amazon.science/publications/why-do-people-buy-irrelevant-items-in-voice-product-search), WSDM2020 by Amazon

 - all types of search, tokenization, including word breaking, decompounding, and punctuation handling, lemmatization or stemming, and stopword identification are important for identifying relevant products
 - Removing the vocaburary gap is challanging research topic.

> [Remedies against the Vocabulary Gap in Information Retrieval](https://arxiv.org/abs/1711.06004)

---
# Query understanding

- Pseudo-relevance feedback
    - [The Impact of Query Suggestion in E-Commerce Websites](https://link.springer.com/chapter/10.1007/978-3-642-29873-8_23)
- Queryclick graphs
    - [ContextAware Query Suggestion by Mining Click-through and Session Data](https://www.cs.sfu.ca/~jpei/publications/QuerySuggestion-KDD08.pdf)
    - [Exploiting query reformulations for web search result diversification](https://dl.acm.org/doi/10.1145/1772690.1772780), WWW2010
    - [Mining E-Commerce Query Relations using Customer Interaction Networks](https://dl.acm.org/doi/10.1145/3178876.3186174), WWW2018


---
# Query understanding

- Word embeddings
    - [Query Expansion Using Word Embeddings](https://dl.acm.org/doi/10.1145/2983323.2983876), CIKM2016
- Multi-modal methods that combine text and visual cues
    -  [ViTOR: Learning to Rank Webpages Based on Visual Features](https://arxiv.org/abs/1903.02939), WWW2019
    - [Improving Outfit Recommendation with Co-supervision of Fashion Generation](https://arxiv.org/abs/1908.09104), WWW2019
---
# Query intent engines

parse the query to extract catalog specific attributes
- [Learning Query Intent from Regularized Click Graphs](https://dl.acm.org/doi/10.1145/1390334.1390393), SIGIR2008
- [JointMap: Joint Query Intent Understanding For Modeling Intent Hierarchies in E-commerce Search](https://arxiv.org/abs/2005.13783), WWW2019

e.g.
- query "red sneakers" which converted to ...

```
{"color":"red", "shoe type":"running", "category":"shoes"}
```
---
# Query intent engines

- simple matching of query terms to a predefined set of product attributes to
more elaborate semantic methods
    - [Query Understanding through Knowledge-Based Conceptualization](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/paper_msr.pdf)
    - [Semantic Query Understanding](https://dl.acm.org/doi/10.1145/3077136.3096472)
    - [Deeper Text Understanding for IR with Contextual Neural Language Modeling](https://arxiv.org/abs/1905.09217)

Ultimate goal of a query intent engine is to return structured, personalized queries for all customer queries.

---
![bg opacity](https://yhatt-marp-cli-example.netlify.com/assets/gradient.jpg)
# Ranking

- How to rank the results shown to customers is one of the most complex issues in eCommerce.
- Practitioners have put effort into deriving a single ranking function that
mixes boolean or tf.idf-based ranking algorithms with other signals, such as recency or popularity

e.g.

- Query: "striped t-shirts"
- May rank highly striped products other than t-shirts
- Since `striped`'s `IDF` score is higher than `t-shirts`

Number of signals is increasing to improve the ranking but...

---
# Extending the product representation.

- Documents have many features beyond how closely they match the query terms
    - how many times they have
been purchased
    - how many times they have been clicked
    - the ratio of clicks versus purchases


---
# Ranking signals and optimization criteria ⚡️

- eCommerce search and recommendation systems must optimize for multiple criteria
    > [Multi-objective ranking optimization for product search using stochastic label aggregation](https://www.amazon.science/publications/multi-objective-ranking-optimization-for-product-search-using-stochastic-label-aggregation), WWW2020 by Amazon
    - one encoding customer preferences and one encoding business preferences.

---
# Ranking signals and optimization criteria

- Customer satisfaction is measured over multiple signals.
    > [Tutorial on Online User Engagement: Metrics and Optimization](https://dl.acm.org/doi/10.1145/3308560.3320087), WWW2019
    - click-through rate, hover and dwell time, satisfied clicks, query reformulations, session length, number of queries before checkout, add-to-baskets, purchases, time-to-next-visit, product returns, and calls to customer service
- Business success is measured over several KPIs
    -  inventory-oriented measures,  revenue-oriented measures, profit-oriented measures, visitor-oriented measures, basket-oriented measures, 

---
# Not all signals are equal ⚡️
Objective functions over multiple signals can bias towards more abundant signals.

e.g.  purchase is a more explicit preference indicator than a click but it is much less frequent. A purchase that was not returned is a stronger signal than a purchase but again is less frequent

#### Objective functions should take into account this difference in signal strength versus signal abundance


Tips: normalization of signal's volume is one solution

>  [News Comments:Exploring, Modeling, and Online Prediction](https://link.springer.com/chapter/10.1007/978-3-642-12275-0_19), ECIR2019

---
# Positive, negative, and delayed feedback loops

- Creating feedback loop is reinforcement learning paradigm

>  [Reinforcement Learning to Rank in E-Commerce Search Engine: Formalization, Analysis, and Application](https://dl.acm.org/doi/10.1145/3219819.3219846), KDD2018 by Alibaba

-  longer feedback loops where the feedback occurs well after the system
has shown results to the user
    - delayed feedback, cold-start problem.


> [Learning Latent Vector Spaces for Product Search](https://dl.acm.org/doi/10.1145/2983323.2983702), CIKM2016
> [On Application of Learning to Rank for E-Commerce Search](https://arxiv.org/abs/1903.04263), SIGIR2017
> [A Comparison of Counterfactual and Online Learning to Rank from User Interactions.](https://arxiv.org/abs/1907.06412), SIGIR2019


--- 
# Practical limitations of Learning to Rank

Most eCommerce search engines based on LtR work in two steps.

1. recall-oriented step
2. precision-oriented step

This implementation of LtR has
proven to be effective in terms of IR and business metrics

> [Promoting Relevant Results in Time-Ranked Mail Search](https://dl.acm.org/doi/10.1145/3038912.3052659), WWW2017
> [Learning to Rank for Freshness and Relevance](https://dl.acm.org/doi/abs/10.1145/2009916.2009933), SIGIR2011
> [On Application of Learning to Rank for E-Commerce Search](https://arxiv.org/abs/1903.04263), SIGIR2017

--- 
# Practical limitations of Learning to Rank

## challange in LtR

1. broad exploratory queries
2. LtR’s issue with the discontinuity in usefulness of SERP