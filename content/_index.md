+++
title = "Housing in New York"
+++
<!--: .wrap .size-70 ..aligncenter bgimage=images/BoroughsNotext.png -->


## **Housing in New York**

<!--: .text-intro --> This website is created as the final project in the course Social data analysis and visualization (02806) The focus here is to analyse the housing prices in New York to find out which factors are influencing them. And where to live is the big question !! Please scroll down and follow the findings we have made.

---

<!--: .wrap -->

## **The data used in this project**
The data source is from [NYC OpenData](https://data.cityofnewyork.us/). And the aim of this website is to enlighten the reason to live one place over the other in New York. The analysis is based on the following datasets.

<!--: .flexblock gallery -->
- {{< gallery title="Housing Prices" href="https://data.cityofnewyork.us/City-Government/NYC-Citywide-Annualized-Calendar-Sales-Update/w2pb-icbu" src="images/House.jpeg" >}}NYC Citywide Annualized Calendar Sales Update{{< /gallery >}}

- {{< gallery title="NYC Arrest data" href="https://data.cityofnewyork.us/Public-Safety/NYPD-Arrest-Data-Year-to-Date-/uip8-fykc" src="images/Crime_Time.jpeg"  >}} NYPD Arrest Data (Year to Date) {{< /gallery >}}

- {{< gallery title="Fire Incident Dispatch Data" href="https://data.cityofnewyork.us/Public-Safety/NYPD-Arrest-Data-Year-to-Date-/uip8-fykc" src="images/fire.jpeg"  >}}Fire Incident Dispatch Data{{< /gallery >}}


---
<!--: .wrap -->

## **Housing prices in NYC**

The prices are shown in this map. However, it appears very clearly that Manhatten is very expensive. Each of the areas are divided into zip codes.

|||v

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/leaflet/map_NYC_prices.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>
<small> Note. This map does not include outliers, e.g too small or too large sale prices </small>

|||

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
  <iframe src="/leaflet/bokeh_prices.html" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border:0;" allowfullscreen title="NYC"></iframe>
</div>
<small> Note. This map does not include outliers, e.g too small or too large sale prices </small>
