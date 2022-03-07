# MVP
## Wine Recommendations

### Background
My client is a wine store looking to boost customer happiness (and therefore customer retention) by implementing a content-based wine recommendation model.

### Impact hypothesis
By analyzing tasting notes that can encompass and predict customer preferences with some degree of accuracy, the wine store will boost the number of bottle purchases made by existing customers.

### Assumptions
I'm assuming:
1. Tasting notes are accurate enough to measure something real and valuable about customer preferences, since the notes include information on flavors, dryness/sweetness, body, varietal, nose, etc.
2. Using a preprocessing pipeline to lemmatize and otherwise pare down the textual data, a model can successfully draw useful information from a large dataset of tasting notes in order to predict wines a given customer is likely to enjoy. Nouns and adjectives contain the most useful information on a wine relative to other parts of speech; therefore a POS tagger is also helpful in reducing dimensionality.
3. A given customer has at least one liked wine in the database to predict preferences.

### Data
I'm looking at comprehensive wine review data in a Kaggle dataset (https://www.kaggle.com/zynicide/wine-reviews) that includes over 100K wines up to the year 2007.

### Exploratory findings
#### Visualizations:

I've created a content-based recommender model using cosine distances to predict the wines a customer is most likely to enjoy. Here's an example of what the model would predict given 4 known wine preferences:

![](https://raw.githubusercontent.com/Elaela22/wine_recommendations/main/Screen%20Shot%202022-03-07%20at%204.15.49%20PM.png)

Here's a word cloud to contextualize the unique preferences and recommendations for this user:

![](https://raw.githubusercontent.com/Elaela22/wine_recommendations/main/word_cloud_wine.png)

### Next steps
* Identify a concrete way to evaluate the model's success
* Currently I'm only using 10,000 rows of data because I kept killing the kernel with too much data. I'd like to figure out how to use all 129,000 rows without killing the kernel, perhaps by reducing dimensionality more effectively.
