# MVP
## Wine Recommendation Clusters

### Background
My client is a wine store looking to boost customer happiness (and therefore customer retention) by implementing a better wine recommendation model.

### Impact hypothesis
By identifying clusters of features (tasting keywords, dryness, body) that can accurately encompass and predict customer preferences, the wine store will boost the number of bottle purchases made by existing customers.

### Data
I'm looking at data on red wines from TotalWine.com, which gives a lot of information on each bottle of wine. I've been able to scrape flavors, price, varietal, and customer reviews from over 3,000 listings.

* I'm using the tasting keywords themselves for certain analyses, but sometimes grouping them into broader categories for easier visualization and trend spotting.
* There are quite a lot of varietals, so for visualizations I limit the varietals to the most well-known.

### Exploratory findings
####Visualizations:
[Tableau dashboard, in progress](https://public.tableau.com/app/profile/emma3974/viz/Wine_Keywords/WineFlavors?publish=yes)

Each wine varietal has a broadly typical flavor profile (i.e. a Rhone Blend will often have spice notes), but there's also more granular variation by the bottle, which will be helpful in identifying unique flavors that a customer may be attracted to. As an example, a customer that preferentially buys or highly rates wines with high minerality may be prompted to buy more bottles with high minerality, even if it's a varietal they haven't yet encountered.

![](https://raw.githubusercontent.com/Elaela22/wine_recommendations/main/mineral_var.png)

### Recommendation
I propose building a clustering model using tasting keywords, varietal, sweetness/dryness, and body to encompass and predict customer preferences based on wines they've rated highly or purchased more than once.