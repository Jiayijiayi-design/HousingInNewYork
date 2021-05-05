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


---
<!-- : .wrap .size-40 -->

### **Configuration**

<!-- : .text-intro -->You can modify WebSlides settings directly from your project config.toml.

~~~toml
[params.webslides]
  banner = false
  slideshow = true
  vertical = false
  autoslide = false
  changeOnClick = false
  disableLoop = false
  minWheelDelta = 40
  disableNavigateOnScroll = false
  scrollWait = 450
  slideOffset = 50
  hideIndex = false
~~~


---
<!-- : .wrap -->

|||v

### **All from one markdown file**

Use three dashes "<code>-</code>" to create a separate slide page.

|||

~~~md

Slide1

---

Slide2

~~~

---
<!-- : .wrap -->


|||

~~~
content
├── home
│   ├── home1.md (weight: 1)
│   └── home2.md (weight: 2)
└── _index.md (initial page)
~~~

|||

### Or not.

You can combine and arrange files with the weight parameter in front matter, and categorize .md files into different folders.

---
<!-- : .aligncenter -->

## Simple Class Assignment

Assign class to a block by using the following notation without quote.

<code><span><!-</span>- : .class -<span>-></span>Content</code>

---
<!-- : .wrap -->

### You can assign class to many elements

<!-- : .flexblock -->
- {{< flexblock "Slides" 6 >}}
<span><!-</span>- : sectionClass .divClass ..subClass -<span>-></span><br>
Content
~~~html
<section class="sectionClass">
  <div class="divClass">
    <div class="subClass">
    Content
    </div>
  </div>
</section>
~~~
{{< /flexblock >}}

- {{< flexblock "Headers and Paragraphs" 6 >}}
<span># <!-</span>- : .hClass -<span>-></span>Header<br>
<span><!-</span>- : .pClass -<span>-></span>Paragraph
~~~html
<h1 class="hClass">Header</h1>
<p class="pClass">Paragraph</p>
~~~
{{< /flexblock >}}

- {{< flexblock "Lists" 6 >}}
<span><!-</span>- : .listClass -<span>-></span><br>
<span>-</span> list1<br>
<span>-</span> list2
~~~
<ul class="listClass">
  <li>list1</li>
  <li>list2</li>
</ul>
~~~
{{< /flexblock >}}
