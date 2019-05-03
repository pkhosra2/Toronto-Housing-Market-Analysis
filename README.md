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

Below we can see the full map exported into an HTML file using the plotly library tool

![World Map](https://user-images.githubusercontent.com/39222728/57117614-6d858900-6d2b-11e9-98d1-099c062cd35f.JPG)

From this plotly map we can see a clear distinction in the majority of Asian immigrants in Toronto, compared to the rest of the world. 

## Toronto Age & Gender Diversity 

![Toronto_Ages_2016](https://user-images.githubusercontent.com/39222728/57117611-6cecf280-6d2b-11e9-8955-6a54e1af039d.JPG)

## Toronto Household Incomes

![TorontoHousehouldIncomeHeatmap](https://user-images.githubusercontent.com/39222728/57117613-6d858900-6d2b-11e9-916e-c0b651cd460e.JPG)

## Toronto Housing Prices 
![Toronto Shapefile](https://user-images.githubusercontent.com/39222728/57117609-6cecf280-6d2b-11e9-8be9-89c6bb4a5c69.JPG)
![Toronto Wards](https://user-images.githubusercontent.com/39222728/57117610-6cecf280-6d2b-11e9-9afb-aaf85e6d34a5.JPG)
![Toronto Housing Prices Map](https://user-images.githubusercontent.com/39222728/57117607-6cecf280-6d2b-11e9-9a49-5fe02d7e1222.JPG)

## The Housing Index 

![Toronto Housing Index](https://user-images.githubusercontent.com/39222728/57117606-6cecf280-6d2b-11e9-969e-5414d7db9582.JPG)

## Conclusion 

