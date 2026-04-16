---
name: Visualizaitons
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
<div>
<vegachart schema-url="{{ site.baseurl }}/assets/json/final_pie.json" style="width: 100%"></vegachart>
<p>
In this visualization I created a pie chart that seperates each slice by license status. I picked license status because when looking at the dataset it had several variations, which I figured could be interesting. I chose a pie chart because it shows the ratio of each status compared to all statuses. The color scheme I am using seperates each license status by color. The biggest pie section colors are brown for NOT RENEWED, navy for ACTIVE, and purple for INACTIVE. I orignally had the pie chart seperated by color only, with zero inactivity, however I noticed there were several duplicates of certain colors with no way to tell what each slice was for. To solve this issue, I used a similar approach to my solution in my second diagram. So now when you click on each slice it pops up with which status it represents. I had a small issue with this at first. Originally all of the statuses were displayed, several overlaping due to the amount of different status. It was nearly impossible to see the names of the smaller slices. This interactivy makes the chart way more clear now without the status label it would be almost impossible to decide the difference in in slices sharing the same color without looking at the dataset.
</p>

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>
<vegachart schema-url="{{ site.baseurl }}/assets/json/interactive_bar_chart.json" style="width: 100%"></vegachart>
<vegachart schema-url="{{ site.baseurl }}/assets/json/final_line.json" style="width: 100%"></vegachart>
<p>
There are three different steps to the final bar chart. The first graph is just a plain bar chart seperate each license type and showing how many records are recorded for each. The second bar chart has a small amount of interactivity. It allows the user to click on each bar and it changes the color. The bars are all purple, then when one is selected, the selected on remains purple while the rest change to green. I wanted to change the colors, just so I could add a little more creativity into the chart. I just like the colors purple and green, there was no specific reason. For the license type I used nominal data, and for Original Issue date I used time. I picked nominal for license type because each possible type is its own distinct catgory, and original issue date is seperated by year. I asked Google Gemini for ways to make the bar chart interactive and I found one of the options very interesting. It came up with idea to link a histogram and the bar chart. When you click on a license type it also shows a histogram of the issue dates according to records. It is super interesting looking at because each license type has a different year where the amount of license spike. For example there were a spike in amount of dental licenses in 1997/1998 while design firm license had a spike in 1995.
</p>
</div>