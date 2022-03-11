# Written Description

## Abstract
I analyzed wine descriptions and varietals using a Kaggle dataset of 119,000 reviews, and created a new content-based recommender model for a wine retailer to uncover niche preferences and thus increase customer loyalty. Each varietal (such as Cabernet Sauvignon, Malbec, etc.) has its own high level flavor profile, with important variations in secondary characteristics (such as earth notes, minerality, herbs, etc.), which must be captured by a high quality filtering system. My model makes use of 130 clusters of wines generated using the KMeans algorithm and recommends wines from a relevant cluster to any user with at least one 'liked' wine in the system. The wine store can evaluate the success of the new model by looking at repeat purchases and purchases per customer.

## Components
### Design

My client is a big wine retailer (in-store and online) that suffers from a lack of customer loyalty and a low number of repeat purchases. They currently use a purely collaborative recommending system that isn't working well.

I developed a *content-based* recommending system using concrete information from the wine's description: flavors, dryness/sweetness, body, mouthfeel, etc. I combined this with another column of data to grab the specific varietal, which is instrumental in categorizing wines. This new model organizes wines into 130 clusters, using unsupervised machine learning on the textual data to learn groupings that make sense and take niche preferences into account. Then, I wrote a function that uses these clusters to find wines a customer is likely to enjoy.

#### Success Metrics

* Number of repeat purchases per customer
* Number of customers making repeat purchases
* Percentage of customers that return

#### Risks and Assumptions
* The data must be accurate, with reliable descriptions of sufficient length
* Rating a wine highly or making a repeat purchase will be the indicators that a customer likes a wine
* Customers must be signed up in the client's system to get recommendations at all
* The model should take price into account as the final filtering step for recommendations
* The final function that outputs recommendations from clusters should be fine-tuned with the help of the marketing team (i.e. # of recommendations per email, # of clusters represented in each email)

### Data
I downloaded a Kaggle dataset (https://www.kaggle.com/zynicide/wine-reviews) of 119,000 wine descriptions through 2017. Each row of data represents one bottle of wine. I used the textual data in the descriptions (written by expert wine reviewers) as well as the specific varietal as features in my model. The target is the list of recommended wines for a particular user based on their 'liked' bottles.

### Tools
* Pandas and python for initial data cleaning and exploration
* NLTK for preprocessing and POS tagging (before switching to spaCy)
* Text preprocessing pipeline from spaCy, including lemmatization and POS tagging
* Vectorization using TFIDF vectorizer
* PCA for dimensionality reduction
* SciKitLearn pairwise distances for original recommender system attempt
* KMeans algorithm for generating clusters
* Python for recommender system using prepared clusters
* Visualizations using stylecloud

### Communication
* 5 minute slide presentation to client (wine store) with proposed model to increase repeat purchases and customer loyalty
* This description / abstract
