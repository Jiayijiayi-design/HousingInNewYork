+++
title = "Housing in New York"
+++
<!--: .wrap .size-70 ..aligncenter bgimage=images/BoroughsNotext.png -->

## **Housing in New York**

<!--: .text-intro --> This website is created as the final project in the course Social data analysis and visualization (02806) The focus here is to analyse the housing prices in New York to find out which factors are affecting them. And where to live is the big question !! Please scroll down and follow the findings we have made.

By: Yue Dong s202730, Line Grove Vognsen s164227, Jiayi Han s164229

---
<!--: .wrap -->


![berit](/images/Berit.png)



---
<!--: .wrap -->

## **The problem solvers**


|||v

![us](/images/buisness.png)

|||

Luckily we are here to help Berit. We have analysed two datasets:  NYC Citywide Annualized Calendar Sales Update and NYPD Arrest Data (Year to Date), both  from NYC OpenData.  
The analysis output is visualized on a map, using Geographical data.
Keep scrolling if you have the same dilemma as Berit, or you want to know more about NYC from a housing and crime perspective.


---
<!--: .wrap -->

## **The Housing prices in entire NYC**

|||v

![price](/images/house/histogram_price.png)

|||

First we take a look at just the house sale prices in the period of 2018-2019 in the entire NYC.
The distribution of prices are mostly concentrated in the left side of the figure, where 90% of the house sale prices in NY cost under 2 million dollars. In other words, if Berit has 2 million dollars, she will have 90% chance of getting a house in NYC, assuming sales prices represent the maximum of individuals' financial capacity.


---
<!--: .wrap -->
## **Opportunities in the boroughs**

|||v

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/images/house/bokeh_prices.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>

|||

If Berit wants to increase her chance or has financial limitations, she will have to limit her search area to more specific boroughs. Here you will find that Queens (97,63%) Richmond/Staten Island (99,35%) and Bronx has ( 95.49% ) of their house prices under 2 million. Whereas in Manhattan the chance is  74.12% and Brooklyn is 89.94%
In other words, your chances of getting a house under 2 million increase if you’re looking in Queens Richmond/Staten Island or Bronx.

<small> Click on legend to learn about which borough will be more suitable for you </small>

---
<!--: .wrap -->
## **See sales in your favorite neighbourhood**

|||v

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/images/house/map_NYC_prices.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>

|||


Is there another price limit than 2 million dollars? Here’s the overview of the sales in 2019 and their prices.
The icon in right upper corner allows you to choose which price category you want to explore. If you zoom and click on a marker you can see the sale price for that specific place.



---
<!-- : .aligncenter -->
## **Does lower price compromize safety?**
![weight](/images/weight.png)

---
<!--: .wrap -->
## **Where does crime occur?**


|||v

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/images/crime/map_NYC_arrest.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>


|||

First, we investigate if it is equally safe to live over all the precincts. We assume that the amount of arrests is a good indication for the safety in the areas. Berit does not know where the different precincts lies or which boroughs it belongs to. So, to help her we have made an interactive map, that shows the number of arrests in each precinct and the belonging boroughs, if you hover the mouse above.
Some areas are safer to live than others, for example almost all precinct in Bronx has a high occurrence of arrests. But precincts 50 in Bronx (upper left corner) have a low arrest occurrence compared to the rest of Bronx.

---
<!--: .wrap -->

## **Who is arrested?**

Apparently does the police tag the races of who commits the crime. Black is clearly the races with highest arrest number, it stands for 47.8 % of the total arrest. The next races is white hispanic which are 25.2 % of all the arrests.
If we look closer to each borough then are the races represented differently.
For Berit race does not matter but it is an interesting that police register this.


![arr](/images/crime/combined_bar_crime.png)


---
<!--: .wrap -->
## **What kind of crimes?**

|||v

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/images/crime/marker_cluster_arrest.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>

|||


There are many kind of crime types, we have selected three that also affect the house prices. The crime types are: felony assault, robbery and assault & related offence. If you look at the interactive map, then you can choose in the upper corner which crime type you want to see and if you click on a marker you get the crime type and race of the arrested.

---

<!--: .wrap -->
## **Distribution of arrests in boroughs**

|||v

![com](/images/crime/arrest_b_p.png)

|||

After some [**research**](https://journalistsresource.org/economics/the-impact-of-crime-on-property-values-research-roundup/), we found that not all crime types have an impact on house prices, violence, assault and robbery have a negative impact on house prices, we filtered the relevant crime types and examined their distribution in different areas. It is important to note, that when binning the distributions of crime into boroughs they seems similar. But looking at the precinct on the next page, there is more variance between precincts.

---
<!--: .wrap -->
## **Is it cheaper to live where it is unsafe**

|||v

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/images/crime/specific_cluster_arrest.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>

|||

To get a more visual perspective, we give a map of the distribution of the relevant crime types, which when compared to the house price map shows that the two are basically opposite trends, with high house prices and low crime numbers in Manhattan and low house prices and high crime numbers in the Bronx.
Thus, for random crimes such as robberies and assaults, choosing areas with high house prices can be avoided to some extent.



---
<!--: .wrap -->
## **We combine the most interesting features of each data set**

|||v

![com](/images/com.png)

|||


In order to give Berit an overview of possibilities and if the crime is related to the housing prices. We tried to gather the interesting information into one data set and applied unsupervised learning
This means we took at a part of the data from the arrest and house sale dataset and gathered it into one.
In the arrest data only the three crimes types 'assault 3 related offence, robbery and felony assault is used as they affected the housing prices. The dataset is merged based on the longitudes and latitudes of the arrest and house sale as it is the most precise of the areas.
This big data set we then tried to split into 6 different groups based on their features. The data in each group should then have some similar traits for example the price range or where it happens.

---
<!--: .wrap -->
## **Do you get more room if you paid more ?**
If you look at the brown boxplot to the left, it shows the price range of group 5 and the plot to the left shows gross square feet of the sale. This brown boxplot lies generally a bit higher than the others but still in the same range. So even though Berit is paying more for the apartment does it not necessarily means that she gets more space according to our analysis.  It shows that even through the sales prices differs a lot then the square feets span over a wide range.

|||v

![com](/images/machine/box_plot_price_cluster.png)

|||

![com](/images/machine/box_plot_size_cluster.png)

---
<!--: .wrap -->

## **What about crimes ?**


|||v

![machine](/images/machine/bar_chart_cluster_crime.png)

|||

In order to narrow down, the figure here shows only the clusters that represent the lowest, and the highest house sale price. Comparing the two clusters, it reveals that the cluster with the highest price has a higher risk of robbery and lower in Assault 3 and related offenses. As the difference between the clusters with regards to these types of crime is not significantly large. Which means it is not possible make any final conclusions.

---
<!--: .wrap -->
## **Where are the cheapest and most expensive clusters?**


|||v

![machine](/images/machine/bar_chart_cluster_borough.png)

|||


The most expensive group has none of the residents in Richmond /staten island, most of the occusence is in Brooklyn, Manhattan and Bronx. If one would like a cheaper residents then Bronx, Brooklyn and Queens seems like a good option according to our cluster.

---
<!-- : .aligncenter -->
![machine](/images/SLUT_1.png)



---
<!--: .wrap -->
## **Our recommendation**

|||v

![machine](/images/SLUT_2.png)

|||

- If Berit wants to live as cheap as possible the chances of getting an apartment are highest in Queens and Bronx.

- If Berit wants to go with Queens and Bronx, she will have chance of robbery compared to expensive areas. At the same time she should be prepared for higher risk of assault.



---
<!--: .wrap .fadeInUp bg=bg-black bg=aligncenter bgimage=images/G.jpg -->

# {{< svg fa-heart-o >}} Here is the link to Explainer notebook

[**CLICK HERE**](https://drive.google.com/drive/folders/1zsXw7st3AIx1puCNJzNkrASYqK2j78r5?usp=sharing)
