---
date: "2016-11-05T18:25:22+05:30"
draft: false
image: img/portfolio/BFAS1.jpg
showonlyimage: true
title: Animal Society No-Kill Shelters and Counties in US
weight: 0
---
## A look at the demographics of current no-kill counties  


General Overview:

Top Left:
Education levels from No High School Diploma to Post Graduate Degree.
The highest number of participants are in the High School diploma group. 

Top Right:
Population Race Demograhics:
Demographics tend to be largely white with a lower proportion of other racial demographics

Lower Left:
Population size:
There are some larger county size represented here, but they are largely under 250,000.

Lower Right:
Income Range:
The counties with no-kill shelters are primarily in the ranges of $50k and below.



![Screenshot_BFAS][1]

> The Big Oxmox advised her not to do so, because there were thousands of bad Commas, wild Question Marks and devious Semikoli, but the Little Blind Text didn't listen. She packed her seven versalia, put her initial into the belt and made herself on the way.

## Limitations of a descriptive data set for actionable insights

Actionable insights for purely demographic data can be limiting.

For example, in the descriptive analysis on the previous slide, we can see that the demographics of counties with no-kill shelters are the following:  
* At least a High School diploma  
* Predominantly White  
* Populations under 250k  
* Income ranges at $75k and under  	


The caveat here is that we are only looking at communites that already have no-kill shelters. How are we to know what counties to target if we can only see those counties that are already on our list? How are we to know which of these characteristics is actually significant in the research of where to target our legislation to promote and create no-kill shelters?

Currently our variables are:  
* Education  
* Race  
* Population Size  
* Income Range  

Are all of these significant? Are some of these heavier in significance? How would that affect our targets for no-kill by 2025?  

Let’s find out.  


I pulled demographic data for all US counties from the ERS USDA data portal

This allowed me to compare no-kill county demographics from the Best Friends data set to all US counties

This was necessary to build any models


My goal is obtaining this data was to be able to look at the demographics of counties in the US that contained no-kill shelters as well as those counties in the US that did not contain no-kill shelters.  

The data needed to be cleaned and organized so that I would be able to join the Income, Education, and Demographic data and then compare the data between them.
I also added a response field in the data that flagged the state/county as being a county that contained a no-kill shelter.
From there, I could find which of those demographics was significant, either positively or negatively, and lay out the targets for counties that match demographically to counties that contain no-kill shelters.
 

![Screenshot1_BFAS][2]

Logistic regression predictions  
A logistic regression helps us to understand the influence of these variables on the probability of a county being designated as no-kill.

The most important factor was the percent of residents in a given county that had not received a high school diploma. The higher this value, the less likely a county would be listed as no-kill. An increase in high school graduations to ~ 40% can double the likelihood of a county being designated as no-kill.


![Screenshot1_BFAS][3]






Random forest importance


A random forest (ML) model highlights the most important variables in determining whether counties are listed as no-kill. 

The most important variables for this data set focus on education levels.

Important to note that the education levels are not independent. Increases in one group must involve decreases to another group.


![Screenshot1_BFAS][4]





Counties predicted to be no-kill, which currently are not. These are good targets for outreach efforts.

The listed counties are US counties that my model gave a 40% or greater probability that should be counties that contain no-kill shelters.

This means that the model found that these counties closely resemble the no-kill counties based on their current demographics and should be no-kill counties already; however, they are not. 

If the demographics of education, income, race, and population size are important, the listed counties are good targets for further research and implementation of no-kill shelters. 

Top Three Counties that resemble current no-kill counties:

Hunterdon County, NJ
Summity County, UT
Fairfax County, VA


![Screenshot1_BFAS][5]


[1]: BFAS1.jpg
[2]: BFAS2.jpg
[3]: BFAS3.jpg
[4]: BFAS4.jpg
[5]: BFAS5.jpg






