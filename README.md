#TITLE

Module 1 Challenge: Using Excel to Analyze & Visualize Kickstarter Fundraising Data

##AUTHOR

Colin Brineman, M.A.

##OVERVIEW

###OBJECTIVES

The challenge for Module 1 is to analyze and visualize data from Kickstarter fundraising campaigns for Louise, a playwright, so that she can better understand the determinants of efficacy for Kickstarter fundraising campaigns in the “theater” category. The purpose of the challenge is to develop and demonstrates skills in Microsoft Excel, including but not limited to:
  - creating pivot tables and data visualizations,
  - filtering and formatting data, and
  - using functions to slice and summarize data.

###DELIVERABLES

The deliverables for the Module 1 challenge include the following:
  1. a table and accompanying chart showing how many Kickstarter campaigns in the “theater” category were either “successful,” “failed,” or “canceled,” broken down by months of the year;
  2. a table and accompanying chart calculating the percentages of Kickstarter campaigns in the “plays” subcategory of “theater,” which were either “successful,” “failed,” or “canceled,” broken down into 12 brackets of initial fundraising goals; and
  3. a written summary of findings concerning the determinants of the efficacy of Kickstarter campaigns, building upon the analyses and visualizations produced during Module 1, including coursework completed prior to the production of the student challenge.

##FINDINGS

###OUTCOMES BASED ON LAUNCH DATE

The line chart produced as part of Deliverable 1 (see: Figure 1) is informative. While the number of failed and canceled fundraising efforts is nearly constant throughout the year, once can clearly conclude that:
1. fundraising efforts started in May are the most likely to succeed and
2. fundraising efforts started in December are the most likely to fail.

FIGURE 1: THEATER OUTCOMES BASED ON LAUNCH DATE
![FIGURE 1: THEATER OUTCOMES BASED ON LAUNCH DATE](/resources/Theater_Outcomes_vs_Launch.png)

###OUTCOMES BASED ON GOALS

The line chart produced as part of Deliverable 2 (see: Figure 2) is perplexing. One should expect there to be a negative relationship between fundraising goals and success rates, given that it is easier to raise less, as opposed to more, money. Therefore, the wild oscillations in the higher goal brackets (>$10,000) defy explanation. There does appear to be a negative correlation between fundraising goals and success rates in the lower brackets ($0 to $10,000), however. Therefore, one may preliminarily conclude that projects with lower fundraising goals have a higher likelihood of success. 

FIGURE 2: OUTCOMES BASED ON GOALS
![FIGURE 2: OUTCOMES BASED ON GOALS](/resources/Outcomes_vs_Goals.png)

##DIFFICULTIES

###OUTCOMES BASED ON LAUNCH DATE

The primary difficulties for Deliverable 1 were:
  1. generating and formatting a pivot table and
  2. generating and formatting a pivot chart.

####GENERATING AND FORMATTING A PIVOT TABLE

Generating one's desired pivot table in Excel involves learning which elements of a dataset belong in 4 “PivotTable Fields," namely, “Filters,” “Columns,” “Rows,” and “Values." One must also ensure that the data in the final pivot table are sorted and filtered appropriately. No aspect of designing and customizing a pivot table in Excel is intuitive. Fortunately, however, Googling solutions to common pivot table problems is not especially difficult.

#####GENERATING AND FORMATTING A PIVOT CHART

######CUSTOMIZING CHART TYPE

When one asks Excel to generate a pivot chart from a pivot table, the result is not always the desired chart type. The initial chart Excel generates from the pivot table in sheet "Theater Outcomes by Launch Date" is a bar graph (see: Figure 3.1), whereas the objective for Deliverable 1 is to generate a line graph.

FIGURE 3.1: AUTOMATICALLY GENERATED BAR CHART
![FIGURE 3.1: AUTOMATICALLY GENERATED BAR CHART](/resources/Automatically_Generated_Bar_Chart.png)
 
######CUSTOMIZING CHART DESIGN

Once one has selected the appropriate chart type, one must then navigate the process of improving the design of the chart, including adding a title, customizing the data markers, and changing the color of the lines to be more visually appealing. A comparison between the line chart which Excel initially generates (see: Figure 3.2) to the final chart for Deliverable 1 demonstrates the degree of customization which can be utilized to produce a more eye-catching and user-friendly visualization.

FIGURE 3.2: AUTOMATICALLY GENERATED LINE CHART
![FIGURE 3.2: AUTOMATICALLY GENERATED LINE CHART](/resources/Automatically_Generated_Line_Chart.png)

###OUTCOMES BASED ON GOALS

The primary difficulty for Deliverable 2 was generating a table using the "COUNTIFS()" function. The “COUNTIFS()” function can be clumsy, if one does not include additional reference cells as inputs to the function. There are trade-offs, however, to including or exluding reference cells.

####ADVANTAGES OF USING REFERENCE CELLS WITH "COUNTIFS()" FUNCTIONS

Using reference cells (see: Figure 3.3) requires a much simpler formula for the table in “Outcomes Based on Goals” than hardcoding values in the absence of reference cells. A version with reference cells of the formula in cell “B1” of the “Outcomes Based on Goals” sheet would be as follows:
  =COUNTIFS(Kickstarter!$F:$F,"="&J$1,Kickstarter!$R:$R,"="&$I$1,Kickstarter!$D:$D,"<"&$J2)
Not only is this formula simpler than one without reference cells, but it is also more repurposable should the end-user desire to break the relevant data down into goal brackets of their own choosing.

FIGURE 3.3: OUTCOMES BASED ON GOALS TABLE WITH REFERENCE CELLS
![FIGURE 3.3: OUTCOMES BASED ON GOALS TABLE WITH REFERENCE CELLS]
 
####DISADVANTAGES OF USING REFERENCE CELLS WITH "COUNTIFS()" FUNCTIONS

The formula used in cell "B1" of the "Outcomes Based on Goals" sheet is less elegant and adaptable than it would have been with the use of reference cells:
  =COUNTIFS(Kickstarter!$F:$F,"="&"successful",Kickstarter!$R:$R,"="&"plays",Kickstarter!$D:$D,"<"&1000)
However, one can reasonably expect the end-user would prefer the cleaner look of the “Outcomes Based on Goals” sheet without reference cells. Possibly even more important, however, is the fact that hardcoding values into the "COUNTIFS()" ensures that the end-user cannot break the table and its dependent chart by accidentally clearing the reference cells. 

##LIMITATIONS TO FINDINGS

###OUTCOMES BASED ON LAUNCH DATE

A visualization of the full Kickstarter dataset shows that May is generally a good time to start a fundraising campaign and that December is generally a bad time to start a fundraising campaign (see: Figure 4.1). Thus, the relationship between launch date and efficacy of fundraising efforts is not unique to theater fundraising campaigns. Without additional information, it is impossible to provide insight into causality, thus limiting the usefulness of the findings for Deliverable 1, however robust they may be. Some potential explanations, which would require investigation beyond the confines of the Kickstarter dataset, could be that:
  (1) prospective donors tend to have more cash-on-hand in May and less in December, perhaps due to the timing of the fiscal year, or
  (2) prospective donors perceive the kinds of campaigns which are launched during December vs. May to differ in quality.

FIGURE 4.1: FUNDRAISING OUTCOMES BASED ON LAUNCH DATE
![FIGURE 4.1: FUNDRAISING OUTCOMES BASED ON LAUNCH DATE](/resources/Fundraising_Outcomes_Based_on_Launch_Date.png)

###OUTCOMES BASED ON GOALS

The line chart of “Outcomes Based on Goals” does a poor job of representing the determinants of fundraising success rates for plays, because the overall distribution of initial fundraising goals for plays is skewed heavily to the right. A cumulative line graph of fundraising efforts for plays shows that over 80% of all fundraising efforts for plays have initial goals of $10,000 or less (see: Figure 4.2). The seeming randomness of success rates for fundraising effots with initial goals over $10,000+ is, therefore, likely just noise. Thus, the preliminary conclusion that there is a negative relationship between fundraising goals and success rates appears more robust, with additional context, than the line chart for Deliverable 2 might suggest.

FIGURE 4.2 CUMULATIVE PERCENTAGE OF PROJECTS BASED ON GOALS
![FIGURE 4.2 CUMULATIVE PERCENTAGE OF PROJECTS BASED ON GOALS](/resources/Cumulative_Percentage_of_Projects_Based_on_Goals.png)

##CONCLUSION

The Module 1 challenge, using Excel to analyze Kickstarter fundraising data, demonstrates both the power and the limitations of Excel as a tool for data analysis and visualization. Fortunately, Louise came very close to meeting her $10,000 fundraising for her play 'Fever'. However, one would be remiss not to recommend that Louise commission additional research into the determinants of fundraising success rates, so that she can better understand both:
  1. the causal linkages between start date and success rates for fundraising campaigns (likely explicable through a subject matter investigation into prospective donors' capacities and perceptions) and
  2. how to effectively execute fundraising projects with larger initial goals.
