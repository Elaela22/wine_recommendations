# Project Proposal
## Better Wine Recommendations
### Question/need:
* *What is the framing question of your analysis, or the purpose of the model/system you plan to build?*

My client is a wine store looking to increase customer retention through their personalized wine recommendations. Currently, their recommendations use a collaborative recommender system, to predict if a user will like a wine given ratings across the entire user base. That model isn't doing so well - when customers buy a recommended wine, they don't tend to buy it again, and they don't rate it very highly. This makes sense since wine is an industry with more niche tastes.

I propose creating a new content-based recommendation model based on a database of tasting notes, which include lots of information on how the wine actually tastes, to be more specific to each user, thus encouraging new favorites and more purchases from each customer.

* *Who benefits from exploring this question or building this model/system?*

The wine store will benefit from giving their customers more accurate personalized wine recommendations, since customers can buy wine anywhere - good recommendations make loyal customers and drive repeat purchases.

Validation of this model would include A/B testing the old model versus the new model, to compare the average number of purchases *per* customer (rather than total purchases across all customers).

-------

### Data description:
* *What dataset(s) do you plan to use, and how will you obtain the data?*

I'm using a Kaggle dataset with ~ 150k rows of wine reviews: https://www.kaggle.com/zynicide/wine-reviews

The data was scraped by a contributor from WineEnthusiast during the week of June 15th, 2017.

* *What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?*

The unit of analysis is each bottle of wine reviewed. I expect to use the textual data from each description, which includes flavors, dryness/sweetness, body, smells, and other information that sommeliers notice in a tasting.

* *If modeling, what will you predict as your target?*

This will be a content-based recommender system that will use a distance metric to predict the best options for a particular user, given a wine or wines that they've previously enjoyed.

-------

### Tools:
*How do you intend to meet the tools requirement of the project?*

* I'll use pandas and python for exploratory analysis
* Hoping to use more visually appealing visualization tools such as Tableau or Plotly; if not, seaborn and matplotlib
* Content-based recommender system modeling
* Preprocessing wine description text using nltk and other libraries

*Are you planning in advance to need or use additional tools beyond those required?*

Stanford POS tagging, which is more accurate than nltk's default pos tagging - I've already installed it and it's working well. This will help pull adjectives and nouns which tend to be the most useful in this context.

-------

### MVP goal:
* *What would a minimum viable product (MVP) look like for this project?*

A minimum viable product could consist of an exploratory visualization of which wines might be predicted for a particular user, given the wines they've rated highly.
