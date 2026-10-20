# Housing Market Analysis: COVID-19 and the Sales Ratio

**HS Data Science and Analytics — Fort Worth, Texas, 2025 (Team 2164-1)**

---

Introduction and Data Overview:

	The housing market is a significant topic in our society due to its continuous fluctuations and various implications for property ownership. Hence, it is essential to monitor and evaluate possible adversities that can affect the housing market. One major world event that affected the socio-economic balance of the world was COVID-19. It has brought various implications to our world within various facets. Hence, we wanted to see if it significantly impacted the housing market by analyzing how the average sales ratio of real estate transactions differs from pre to post-COVID-19. The findings will be critical in understanding to what extent COVID-19 impacted the housing sector and evaluate how future pandemics may have similar impacts; it is essential to understand this in order to see the significance of the pandemic and if preventive measures are needed.    

The sample data collected for the analysis was approximately a quarter million real estate transactions from a population of approximately 1 million from nonfederal data by The Office of Policy and Management. The original population was collected from Connecticut from real estate transactions with a sales price of greater than two thousand dollars within a two-month span of every year between the periods of 2001-2022.  For each sale record, the data was stored in a tabular data structure with a column that included a multitude of variables such as the date of sale, property type, sales ratio, etc (see Appendix A). The sample was later stored in Excel with a similar data structure (see Appendix B). We evaluated both categorical and quantitative data by collecting the integer of the year of sale and the float of the sales ratio and comparing them. We also collected the total real estate transactions, mean sales ratio pre and post-COVID, and the standard deviation of the sales ratio in order to calculate the significance test for the difference of means, specifically a Paired T-Test for pre and post-COVID (see Appendix C). 

Data Dictionary:

Figure 1. The following is the Data Dictionary of the data points used

Purpose:

	As we currently understand, COVID-19 has led to long-lasting implications in a variety of sectors around the world, which has been expressed in current literature. One common conclusion that has been expressed about the real estate market can be seen from the following literature: Stanford’s Economic and Policy Research, National Library of Medicine, and Bank Rate. From their research, we can understand a common theme that COVID has largely reshaped the housing market in a variety of ways. It had effects on property devaluation in urban sectors and led to a shift from urban to more suburban sectors especially with increased remote work as people did not need to live near urban industries now; this led to suburban home prices rising. Similarly, the University of Michigan's Economic Research Department also expresses concerns due to rising prices and the supply of housing being limited due to COVID; as buyers left the market to wait for a price drop, it led to high mortgage rates, which discouraged resale and lowered demand. This conclusion seems to elaborate further on the implications of COVID-19, which decreased the rate of suburbanization. 

Overall, COVID-19 showed a large shift in increased suburban demands due to remote working, which largely increased the prices of homes. However, this demand begins to fight with increasing mortgage rates, which decreases demand. As expressed by the current literature, we can see major shifts and fluctuations in property demand, property value within urban sectors, and overall price increases within the housing market being impacted by COVID. Due to these fluctuations and changes in property value and price, it seems critical to evaluate the sales ratio of the housing market which is dependent on the relationship of initial housing value and final house sale value. Hence, we should evaluate how the sales ratio changed over pre and post-COVID and see if there were any significant changes during this shift in time period. 

Methods:

In order to conduct an effective data analysis, we first had to collect the data from a credible source that came from a large population. Hence, we collected the data from “Data.gov”, which is the U.S. government’s open data source site. Then we found data from a large data set of approximately 1 million real estate transactions from a 20-year time period within the state of Connecticut. Then we upload the CSV file of the entire data set into Excel and then only collect the data for a 6-year period from 2017-2019 (pre-COVID) and 2020-2022 (post-COVID). Afterward, we created formulas in Excel to manipulate the large sample size and collect significant information to conduct a significance test for the difference of means using a Paired T-Test. We wanted to see how the sales ratio changed over pre and post-COVID by comparing their means. Hence, we mainly focused on gathering information for the sales ratio and the time periods; in this data set a sales ratio lower than 1 is beneficial towards the homeowner selling and above being worse in comparison of the house valuation to the final sales price. We came up with a null hypothesis of  “There is no significant difference in the means of sales ratio between pre and post-COVID” and an alternative hypothesis of  “There is a significant difference in the means of sales ratio between pre and post-COVID”; we want to see if our results reject or fail to the reject the null. We also checked the necessary conditions to conduct the significance test such as randomness, normality, and independence. We created formulas to find major information for the test such as total sample size, standard deviation of sales ratio, and total and average sales ratio within each year and within pre and post-COVID. Then we used these values within the Paired T-Test to find our results.

Results:

Again, after gathering and formulating raw data by using formulas in Excel, we were able to get a data summary of vital information that would help us conduct a significance test for the difference of means using a Paired T-Test to compare the data pre and post-COVID to see if there was a statically significant difference between the two time periods.

Figure 2. The following gives the data summary from the raw data collected

After conducting the Paired T-Test by using vital information from the data summary, we found a t-statistic of 787.52 and a degree of freedom of 124,999 from the pairs of pre and post-COVID data. Then we used the two to formulate a p-value of 0.0 which is significantly smaller than the standard threshold of 0.05. However, we noticed a possible outlier with the data collected during 2018. Hence we conducted a 1.5IQR test to see if it was an outlier. The threshold found for an outlier would be an average sales ratio above 4.3 and 2018 was at 9.351. Hence, 2018 was an outlier in the data set. 

Figure 3. The following shows the average sales ratio over time

Due to 2018 being an outlier, we decided to conduct another Paired T-Test to see if there would be a difference in significance. After conducting the test, we found a new t-statistic of 160. Then we used this new t-statistic to formulate a new p-value which still came out to almost 0.0; removal of 2018 made the difference smaller, but still highly significant.

 

Conclusion:

From the results gathered, we can conclude to see if there is a significant difference between pre and post-COVID sales ratio. Since our p-value is less than the standard threshold of 0.05 for both Paired T-Tests, we can reject the null hypothesis. We can conclude that there is a statistically significant difference between the pre and post-COVID sales ratio. This suggests that the sales ratios have changed significantly after COVID; the statistical significance shows us that the difference between the time periods is not just by chance, rather, the decline in sales ratio is a real effect, not by random fluctuation. Hence, the lower sales ratio post-COVID can bring various implications.

This suggests that while there were adverse effects on the socioeconomic status of the nation during COVID-19, the significant drop from 4.27 to 1.08 sales ratio alludes to the fact that sales efficiency and profitability have improved after COVID-19 despite its adversities. There could be a variety of factors that caused this such as behavioral changes, market changes, and new adaptations that could lead to this increase. While 2018 was a significant outlier that led to this increase in sales ratio, there was a sharp decline during 2019 (before COVID). Hence, this shows that changes began well before COVID-19 started. This suggests that not all improvements in the sales ratio were not due to COVID alone and instead, other factors contributed to this. Hence, while we can conclude that there was a significant difference in sales ratio between pre and post-COVID, we cannot show COVID-19 as a direct causation towards the improvement of the housing market.  

Next Steps:

The results and conclusions we gathered suggested meaningful changes in the sales ratio that warrant further investigation into the factors that contributed to this improvement; we need to look at how we can further investigate our findings. Primarily, we need to understand why there was an improvement in the sales ratio for homeowners. While we can assume this is due to the high demand for suburban housing, we cannot lead to this conclusion especially due to the high mortgage rates as understood by the literature. Hence, this calls for further research to understand why this improvement occurred. This can be done by analyzing other possible factors that affected the housing market; we saw from our literature that various factors led to housing fluctuations that derived from COVID, so to get a more holistic understanding of the change in housing sales ratio, we need to examine these factors and possible extraneous variables. We also saw in our conclusion that improvement began well before COVID during 2019 from the spike in sales ratio in 2018; while the time period shift from pre to post-COVID has shown a statistically significant impact on sales ratio, it also seems imperative in understanding what caused such a major spike in sales ratio during 2018 and what caused the following downward trend during 2019.  

Digital Scientific Poster:

Bibliography/references:

data.gov. “Real Estate Sales 2001-2020 GL.” Data.gov, data.ct.gov, 9 Aug. 2023, catalog.data.gov/dataset/real-estate-sales-2001-2018.

Beck, Rae Hartley. “Covid’s Impact on the Housing Market.” Bankrate, 7 Sept. 2022, www.bankrate.com/real-estate/covid-impact-on-the-housing-market/.

Gupta, Arnav. “Lasting Effects of COVID-19 on the National Housing Market – Michigan Journal of Economics.” Michigan Journal of Economics, 24 Apr. 2023, sites.lsa.umich.edu/mje/2023/04/24/lasting-effects-of-covid-19-on-the-national-housing-market/.

Ramani, Arjun, and Nicholas Bloom. “The Donut Effect: How COVID-19 Shapes Real Estate | Stanford Institute for Economic Policy Research (SIEPR).” Siepr.stanford.edu, Jan. 2021, siepr.stanford.edu/publications/policy-brief/donut-effect-how-covid-19-shapes-real-estate.

Schwartz, Amy Ellen, and Susan Wachter. “COVID-19’S IMPACTS on HOUSING MARKETS: INTRODUCTION.” Journal of Housing Economics, 13 Dec. 2022, p. 101911, https://doi.org/10.1016/j.jhe.2022.101911.

Appendices:

Appendix A. Original Data Population

 

Appendix B. Excel sample data collected

Appendix C. Data Summary and significant formulas used

Appendix D. Visualizing the data formulated

Citations:

TSA LOGO AND CITATION:

Wikipedia Contributors. “Technology Student Association.” Wikipedia, Wikimedia Foundation, 29 Jan. 2020, en.wikipedia.org/wiki/Technology_Student_Association.

CSV DATA SAMPLE SCREENSHOT:

data.gov. “Real Estate Sales 2001-2020 GL.” Data.gov, data.ct.gov, 9 Aug. 2023, catalog.data.gov/dataset/real-estate-sales-2001-2018.

EXCEL GRAPHS:

“Excel.” Cloud.microsoft, 2024, excel.cloud.microsoft/.

Student Copyright Checklist and Self Evaluation:

Consent and Release Forms:

N/A
