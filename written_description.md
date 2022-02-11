# Written Description

## Abstract
I analyzed wine tasting notes and varietals using scraped data from TotalWine.com, in order to propose a new recommender model for a wine retailer. Each varietal (such as Cabernet Sauvignon, Malbec, etc.) has its own general flavor profile, with variations in important secondary characteristics (such as earth notes, minerality, herbs, etc.). A collaborative recommending system would overlook those characteristics, but a content-based model would uncover these unique preferences. The wine store can evaluate the success of the new model by looking at repeat purchases and purchases per customer.

## Components
### Design

My client is a big wine retailer (in-store and online) that suffers from a lack of customer loyalty and a low number of repeat purchases. They currently use a *collaborative* recommending system that isn't working well.

I propose developing a *content-based* recommending system using concrete features found on the label that relate to the wine's actual taste: tasting keywords, varietal, dryness/sweetness, and body. This model will take niche preferences into account, for true customer-centricity.

#### Success Metrics

* Number of repeat purchases per customer
* Number of customers making repeat purchases
* Percentage of customers that return

#### Risks and Assumptions
* The data must be accurate, with reliable tasting keywords
* The new model will have less data to draw on, because it's not looking at the total user base to make a recommendation
* Rating a wine highly or making a repeat purchase will be the indicators that a customer likes a wine
* The new model will perform better the more customers rate and purchase
* Customers must be signed up in the client's system to get recommendations at all
* One option to consider will be a hybrid model (collaborative filtering and content-based filtering together)

### Data
I scraped information on 3,500 bottles of red wine from TotalWine.com, using Selenium to scrape and then BeautifulSoup to parse. After removing rows with null values, I still ended up with almost 3,000 rows. The features I scraped included tasting keywords, customer reviews, price, and varietal, though tasting keywords and varietal were my primary objects of analysis. I used customer ratings to verify that highly rated wines have nearly the same tasting note distribution as the wines do overall, indicating a need for a more customer-centric approach.

### Tools
* Scraping using Selenium
* Parsing using Beautiful Soup
* Exploratory data analysis in Google Sheets, including one hot encoding for categorical features that needed summing
* Visualizations and analysis in Tableau, including grouping notes into tasting categories to better conceptualize and visualize a long list of keywords

### Communication
* 5 minute slide presentation to client (wine store) with proposal to increase repeat purchases and customer loyalty
* This description / abstract
* [Tableau dashboard](https://public.tableau.com/app/profile/emma3974/viz/Wine_Keywords/WineFlavors)
