# Toronto-Housing-Market-Analysis

## Project Objective

The purpose of this project is to understand the history, current state, and potential future of the overall Toronto housing market using publicly available CENSUS data sources 

## Gathering Our Data

To first understand the market we need to understand what kind of questions we want answered. We know that we want to understand the housing market in Toronto, but how exactly can we do that? One approach is by asking a variety of questions that will help us split up the population of Toronto in such a way that we can accurately diversify the data.

For this project we will attempt to answer the following questions:

1. What is the past population of Toronto compared to the rest of the GTA?
2. What are the age groups by gender in Toronto?
3. Which geenration of immigrants is the most prevelant?
4. Where are citzens of Torotno immigrating from?
5. How much does a household make annually per ward/district?
6. How much are house prices per ward/dsitrcit?
7. How is the Toronto housing index performing? 

The data sources used for this project will be Concensous Canada, Statistics Canada, and the City of Toronto Data Archives 

## Toronto Population History

For this analysis we will collect daata based on the total population of the GTA region, which is made up of the 5 regions:

1. Toronto
2. York
3. Durham
4. Peel
5. Halton

Below we can see the transition of Population percentage for the city of Toronto fomr the years 1996-2016:

![GTApop1996](https://user-images.githubusercontent.com/39222728/57117390-b2102500-6d29-11e9-8bdb-832a6c1f33fd.JPG)
![GTApop2001](https://user-images.githubusercontent.com/39222728/57117391-b2102500-6d29-11e9-8022-ff7f71cada86.JPG)
![GTApop2006](https://user-images.githubusercontent.com/39222728/57117392-b2102500-6d29-11e9-8f9e-77e1bc7e281f.JPG)
![GTApop2011](https://user-images.githubusercontent.com/39222728/57117393-b2102500-6d29-11e9-9812-5ec63809bd27.JPG)
![GTApop2016](https://user-images.githubusercontent.com/39222728/57117394-b2102500-6d29-11e9-938f-8634c47a26b7.JPG)

From the trasnition between the chart above we can see a clear decrease in popuation for the city of Toronto, contrasting the steady increase in population for the ork region. This can be due many factors that are in play. One of which can be case-by-case family situations. From simple intuition, Toronto as a region is less popular for larger families to settle, given its small homes and fast-paced atmosphere, while York offers a more suburb touch, inviting more families into its area. 

Below we can see a better representation of this shift in population between the two regions.

![percentchangepopGTA](https://user-images.githubusercontent.com/39222728/57117563-05cf3e00-6d2b-11e9-912b-daea088221a7.JPG)

This shift in population could mean a change in how families are chooosing where to raise their children. These families can be citizens native to Toronto or they can be immigrants. We will explore this next.

## Toronto Generations

Next we look to find which generation of immigrants seem to be more preveleant above all others. The chart below lets us see this comparison:

![torontogenerations2016](https://user-images.githubusercontent.com/39222728/57117612-6cecf280-6d2b-11e9-8dc1-9b68da895d06.JPG)

We can clearly see that first generation immigrants represnt the majority of the Toronto imimgrant community. From this analaysis, we can conclude that alot of these immigrants from first geenrations can potentially be responsible for the sudden increase in population in the York region we observed from our previous visualization. But, where specifically are all of these immigrants coming from? Our next visualization lets us see this.


## Immigrant Map

Using the same CENSUS data, we can represent the entire Toronto immigration population using a clorepath map using the geopandas and pyshape Python libraries 

It is important to note that the data used to creat our cloreopath was taken form a data set that looked at the countreis from which the immigrants were born. 

Below we can see the full map exported into an HTML file using the plotly library tool, with example code:

![Capture](https://user-images.githubusercontent.com/39222728/57169365-3a4b0480-6dd4-11e9-9b3b-218b5aebda46.JPG)

This line lets us export our geo pandas file into an HTML document displaying the map shown below:

![World Map](https://user-images.githubusercontent.com/39222728/57117614-6d858900-6d2b-11e9-98d1-099c062cd35f.JPG)

From this plotly map we can see a clear distinction in the majority of Asian immigrants in Toronto, compared to the rest of the world. 

## Toronto Age & Gender Diversity 

The next analysis we will look at it the gender and age diversity amongst all of Toronto's citeizens. Below we can see the results 

![Toronto_Ages_2016](https://user-images.githubusercontent.com/39222728/57117611-6cecf280-6d2b-11e9-8955-6a54e1af039d.JPG)

From this plot we can see that the most prevelant age range is between the years 25-30 years old, and the majoirty of the age ranges have women with the higher population, compared to men. 

Next we will take a look at all of the household incomes 

## Toronto Household Incomes

using the custom seaborn library we will implement a heat map using household income in intervals of $5-10k per ward. This plot can be see below

![TorontoHousehouldIncomeHeatmap](https://user-images.githubusercontent.com/39222728/57117613-6d858900-6d2b-11e9-916e-c0b651cd460e.JPG)

We can see that the top ward incomes are:

1. Ward 16 ------> Don Valley East
2. Ward 25 ------> Scarborough Rouge Park
3. Ward 27 ------> Centre-Rosedale

We can see that all of these wards seem to have a lot of household that have an average income of $150k/ year

## Toronto Housing Prices 

This method of data visualization will be the one of the most difficult because it involes using a shapefile of Toronto's district/wards using latititude and longitude coorinates.

Luckyily, the Toronto Database archives provies a shapefile of Toronto broken up into its ward which we can plot using the shapely Python library. This shapefile can be seen below:

![Toronto Shapefile](https://user-images.githubusercontent.com/39222728/57117609-6cecf280-6d2b-11e9-8be9-89c6bb4a5c69.JPG)

Now that we have our shapefile, we need to establish which ward is which using another document found on the city of Toronto government website

Thie image shows us the numbers of all the Toronto wards by number

![Toronto Wards](https://user-images.githubusercontent.com/39222728/57117610-6cecf280-6d2b-11e9-9afb-aaf85e6d34a5.JPG)

Once we have our shapefile ready to populate with data, we can incorporate our dataset into it. This specific dataset was taken off another Kaggle project. It list the prices of all homes in the Greater Toronto Area that were sold over the year 2016. however, our concern is only with the homes that were sold in only the Toronto region.

We can use their lines of code below to match the geometry of our shapefile to that of our housing coordinates.

![Capture](https://user-images.githubusercontent.com/39222728/57187864-8fb20f00-6ec3-11e9-9f10-eefcf200932d.JPG)

Below we see the final resulting visulaization

![Toronto Housing Prices Map](https://user-images.githubusercontent.com/39222728/57117607-6cecf280-6d2b-11e9-9a49-5fe02d7e1222.JPG)

## The Housing Index 

Finally we take a close look at the Toronto Housing Index. As a background to its significance, the housing index serves as a tool to  estimate the current direction of the housing market for a particular city by averaging the prices of single-family home prices. 

Using the matplotlib library we can plot a imple line graph to show the direction for the Toronto housing market over the last 20 years. 

![Toronto Housing Index](https://user-images.githubusercontent.com/39222728/57117606-6cecf280-6d2b-11e9-969e-5414d7db9582.JPG)

From the plot above we can clearly see that the index has grown significantly since the 1980's. However, we take notice that it is also overextended, mainly for the last yeo years, and is currently exepreince a common consolidation period. We can infer that the housing market has potentially become saturated with buyers and is currently awaiting to see a potential shift in direction.



## Conclusion 

