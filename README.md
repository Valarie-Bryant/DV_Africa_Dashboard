## Visualizing African Progress
December 2020


<iframe src="https://public.tableau.com/views/IRIS_16078811409990/Sheet1?:embed=yes&:language=en&:display_count=yes&:showVizHome=no" width = '650' height = '450' ></iframe>

## Background
The American public generally has a negative view of the African continent. Portrayals of Africa in movies and news media are often focused on violent conflict, hunger, poverty, and other serious problems; one study of media outlets found that Africa was often portrayed as ‘doomed, dark, and diseased’, and the problems of one country are used to represent the whole continent.[1] 
-	Moreover, Africa is sometimes referred to as being a ‘country’, despite containing 54 independent countries with significant diversity among them.[2]
-	One researcher has found that Americans have very little appreciation for the extent to which Africa has industrialized and made progress.[3] 
-	In general, Westerners are ignorant of the progress being made in the fight against poverty. One 2017 survey found that 51% of Americans thought that the percent of people worldwide living in extreme poverty had grown in the preceding two decades, when in fact it has fallen.[4] In a 2015 survey, only 6% of Americans thought that the world was, in general, getting better.[5]

Americans could be forgiven for this view, as African countries remain global outliers on a range of development metrics. *Figure 1* shows a global map, and it allows users to change the metric being shown. Africa is particularly noteworthy for poor scores in access to electricity, child mortality, and adolescent fertility.

<iframe src=" https://public.tableau.com/views/DVProject12_17/Figure1?:embed=yes&:language=en&:display_count=yes&:showVizHome=no" width = '650' height = '450' ></iframe>
 https://public.tableau.com/views/DVProject12_17/Figure1?:language=en&:display_count=y&publish=yes&:origin=viz_share_link


However, this view of African countries is often overly negative and oversimplified, and Americans’ understanding (or lack thereof) of the African content matters because it shapes policy responses to events there.
-	Dionne and Seay explain that American ignorance helped fuel the panic around the Ebola outbreak in 2014. Because Americans are used to thinking of the continent as one place (rather than 54 separate countries), there was public panic when someone fell ill who had been to ‘Africa’, even though the country they’d visited was thousands of miles away from the outbreak.[6] They also note that other countries far from the outbreak lost significant tourist revenue because of this oversimplified view. Politicians were also able to seize on this fear, and created partisan divides on the handling of the epidemic.
-	Elizabeth Schmidt has argued that, with negative stereotypes of Africa dominating the media, ‘Africans are regularly blamed for their plight, with few in the halls of power understanding the role the US government and its allies have played in generating and perpetuating many of the challenges facing the African continent today — and even fewer accepting US responsibility for righting the wrongs.”[7]
-	If we view African countries as hopeless, or not progressing, that is likely to lead to policy decisions built on despair. We will miss opportunities for partnership. If we view Africa too simplistically, as a single entity, we risk broad-brush approaches that also fail to handle challenges and opportunities in a targeted way.

So, let’s take some time to 1) appreciate the progress that African countries have made in the last few decades, and 2) to note the diversity within the continent.

*Figure 2* shows a map of how democratic each African country is, with -10 being fully autocratic and +10 being fully democratic. These numbers are from the Polity Project from the Center for Systemic Peace.[8]  South Africa and Kenya each have a score of 9, making them slightly higher than the United States, which only scored an 8 in recent years. Other countries remain deeply undemocratic, including Eritrea, Egypt, and Cameroon. Hovering over each country on the map reveals its history of democracy since the late 1990s. On the right side of Figure 2 we see a line chart that charts the average democracy score on the continent, which has been rising consistently.
 


*Figure 3* repeats the structure of the previous graphic, but this time works to challenge our assumptions of Africa as a war-torn continent, and it focuses on fatalities from conflict, as gathered by the ACLED project (see appendix). This map’s coloring shows the total conflict fatalities in these countries from 1997 to the present, and serves to show the diversity of outcomes; hovering over a country shows annual fatalities over time.
-	The worst conflict in recent history was in Angola, which has in total suffered around 144,000 deaths; however, these were heavily concentrated in the 1999 and 2000.
-	Some countries have been basically conflict-free, particularly in Southern Africa. Botswana has recorded just 10 fatalities from violence or unrest in the last 24 years.
-	Overall, conflict levels in Africa were highest in the late 1990s and have been lower, but steady, since.

 


*Figure 4* shows the incredible progress that African countries have made in health and development in recent years. The user can animate the figure to move by year, and it shows African countries’ reductions in child mortality (on the horizontal axis) and adolescent fertility (on the vertical axis). The coloring of different sub-regions also show the significant variation, with North African countries having the best health metrics.
 


Appendix: Description of data sources and transformations/ technology used
Data Sources: 
*ACLED*: The first data source for this visualization is ACLED, which uses news reports to track major events around the world.[9] I am using a subset of the data for Africa, which has complete coverage from 1997 to the present. I summed counts of conflict fatalities in each country-year. Because ACLED relies on news sources to gather their conflict information, this can result in imperfect coverage of conflict information.

*World Bank*: I used a number of development indicators from the World Bank to show progress on metrics around health, development, and prosperity.[10] Most of these data have significant missingness in early years (the data begins in 1960). For the most recent year of data (2018), there are some variables with missing values, including GDP per capita (11% missing), child mortality (9%), life expectancy (8%), and adolescent fertility (9%).

*Polity Scores*: I acquired data on the democratic nature of countries from the Polity Project, published by the NGO Center for Systemic Peace[11]. They give a democracy score of -10 (full authoritarian) to +10 (full democracy) to every major country from 1800 through 2018. The goal with this dataset is to show the great diversity of democratic outcomes in Africa, and improvements and changes over time. The polity score has a missingness in 2018 observations of just .6%, and is present for all African countries.

*Transformations & Technologies*: The data wrangling for this visual was done using Python, primarily the Pandas package. The visual was created using Tableau. Python code is attached for review. The main steps of transformation were: 
-	Reading in all of the datasets from ACLED, the World Bank, and the polity scores.
-	For the ACLED data, I summed observations by the country-year, and kept counts of total events (which included battles, riots, protests, etc.), counts of battles or violence against civilians, and a count of total fatalities.
-	For the World Bank data, I created a log of GDP, to facilitate easier visualization in Tableau. Especially when showing GDP per capita in the whole world, logged variables better show the variation on the lower scale, where most of Africa is.
-	I combined the three datasets based on the year-country, using a three-letter country code. The Polity data contained a different three letter country code, requiring some fixing before it could be merged. I also had to correct a country name to one that Tableau would recognize.


*Bibliography*
1.	Nareissa Smith. “Why the global perception of Africa should matter to African Americans.” Atlanta Black Star. January 2018. https://atlantablackstar.com/2018/01/23/global-perception-africa-matter-african-americans/ 
2.	Harry Broadman. “Africa, the continent of economic misperceptions.” Forbes. March 2016. https://www.forbes.com/sites/harrybroadman/2016/03/31/africa-the-continent-of-economic-misperceptions/?sh=bf6df396c54a 
3.	Nareissa Smith. “Why the global perception of Africa should matter to African Americans.” Atlanta Black Star. January 2018. https://atlantablackstar.com/2018/01/23/global-perception-africa-matter-african-americans/
4.	Max Roser & Mohammed Nagdy. “Optimism and Pessimism” https://ourworldindata.org/optimism-pessimism#information-matters-we-are-not-only-pessimistic-about-the-future-we-are-also-unaware-of-past-improvements  
5.	Max Roser & Mohammed Nagdy. “Optimism and Pessimism”   https://ourworldindata.org/optimism-pessimism#1-misperceptions-about-specific-trends-reinforces-general-discontent-about-how-the-world-is-changing 
6.	Kim Deonne & Laura Seay. “American perceptions of Africa during an Ebola outbreak.” MIT Press. March 2020 https://covid-19.mitpress.mit.edu/pub/ialzqbqw/release/1 
7.	Elizabeth Schmidt “A progressive foreign policy for Africa.” Jacobin Magazine. December 2019. https://www.jacobinmag.com/2019/12/progressive-foreign-policy-africa-libya-somalia 
8.	The Center for Systemic Peace. Polity Project. https://www.systemicpeace.org/polityproject.html 
9.	ACLED. https://acleddata.com/#/dashboard 
10.	The World Bank. Indicators. https://data.worldbank.org/indicator 
11.	The Center for Systemic Peace. Polity Project. https://www.systemicpeace.org/polityproject.html
