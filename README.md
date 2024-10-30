# Maven Tech Sales Insights - Project Overview
## The goal of this project is to investigate the quarterly performance of sales teams at Maven Tech in order to track their sales opportunities.
For the Maven Sales Performance Project, I played the role of a BI Developer for MavenTech, a company that specializes in selling computer hardware to large businesses. They've been using a new CRM system to track their sales opportunities but have no visibility of the data outside of the platform.

## Dataset Structure
The dataset contained records exported from MavenTech's CRM from October 2016 to December 2017. It held details of opportunities with associated information such as product, account, and whether the sale was won or lost.

<img width="451" alt="Screenshot 2024-10-29 at 16 11 07" src="https://github.com/user-attachments/assets/178e6486-1cd9-4214-a482-dad19e4299af">

## Key Assumptions
When creating an interactive dashboard, I always like to chat with the users to make sure I truly understand the intended purpose and the questions they seek to answer with the dashboard. In the absence of being able to chat with the sales managers, I made the following key assumptions which I used to guide my dashboard design.

* **The main goal for sales managers is viewing the current state of play for their team, and obtaining actionable information.** The key questions they want to answer are:
  * How is my team (as a whole and individual team members) tracking against our key KPIs?
  * Are there team members who require extra support in certain areas?
  * Where should I focus my efforts for the rest of the quarter to improve performance?
  * Is my team performing above average compared to the rest of the business?
* Their main KPI is **the dollar value of sales made**, however related metrics such as **number of sales**, **conversion %**, and **average sales value** are also important and help to understand their total sales value.
* They may also at times want to dive deeper and look at their team's performance over the year or in comparison to the other sales teams.
* As the dashboard is intended for the sales managers, the most important view to them is to see their own team, rather than an Exec dashboard with higher level team comparisons. They may however like to look at other sales teams in more detail and there is no requirement for row level security to prevent them access to other team data.
* It is assumed that the "Current quarter" is Q4 2017, which is the latest time period recorded in the dataset.
## Key Metrics
* Total Sales: The cumulative revenue generated from all completed sales in Q4 2017.
* Avg.Sale Value: The average monetary value of the selected sales team.
* Avg.Weeks to Close: The average weeks it takes to close a sale in the sales pipeline(Prospecting > Engaging > Won) .
* New Opportunities: The number of potential sales leads generated in Q4 2017.
* Potential to Close: Potential sales values for records in Prospecting or Engaging stages.
* Conversion %: The percentage of opportunities that convert to actual sales.

## The Dashboard

Based on the dashboard, here're the insights for Sales manager Celia Rouche.

**Current Quarter Performance**

![Current Quarter Performance](https://github.com/user-attachments/assets/a4708276-68db-46f2-a1d9-b511d1440e10)

* **Key Insights**
   * **Overall Sales Decline:**
     * Total sales for the quarter are €430K, down by 12.3% compared to the last quarter. Average sale value also decreased to €2,403, down 14.7%.
     * New opportunities dropped significantly to 179 (a 54.6% decrease from last quarter), suggesting a potential issue with lead generation or sales outreach efforts.
   * **Agent Performance:**
     * Vicki Laflamme leads with the highest number of sales (68) and total sales value (€139,082), despite having a relatively low average sale value of €2,045.
     * Elease Gluck has the highest average sale value at €3,792, though with fewer sales overall (23).
     * Markita Hansen has the lowest conversion rate (50.7%) and a low average sale value of €1,580, indicating a potential area for improvement in her sales strategy.
   * **Product Performance:**
     * MG Advanced is the top-performing product in total sales (€174,791) with the highest conversion rate (70.8%), indicating a strong product-market fit.
     * GTX 500 also shows high total sales (€83,377) but with a significantly lower conversion rate (60%) and only 3 sales. This suggests a high-value product with fewer transactions.
     * GTX Plus Basic and GTX Basic have low total sales despite reasonable conversion rates, implying they may not be as appealing or have lower market demand.

![Current Quarter Sales](https://github.com/user-attachments/assets/ad72c717-9adb-44cf-a664-fbaf7c3f36ce)

* **Key Insights**
  * **Sector Performance**:
    * Retail leads with €85K in sales, followed by Finance** (€65K) and Entertainment (€63K). These three sectors contribute a significant portion of the total sales, indicating strong demand.
    * Lower-performing sectors include Employment(€20K) and Marketing(€18K), suggesting these areas may have less market demand or need a tailored approach to increase sales.
  * **Top Accounts**:
    * Xx-holding is the top account with €63K in sales, followed by Cheers(€35K) and Singletechno (€23K). These key accounts represent valuable, high-revenue customers and should be prioritized for retention and upselling.

![Open Opportunities Report ](https://github.com/user-attachments/assets/205c4cdf-8bb7-4b01-968c-00343c32c861)

From the potential to close card, manager can also dive deeper into all opportunities labelled as engaging for their team. They can use this detail to prioritise actions such as following up offers to close before end of quarter, and CRM cleanups e.g., opportunities that have been open for too long and need to be marked as lost.

**Performance by Team**

While it's not the most important goal for the sales managers, they would also like to be able to see how their team is performing in comparison to the remaining sales team. The current quarter performance by team page allows them to do this, by ranking all sales teams across the key metrics, and highlighting the selected team so managers can easily see where they stand.

![Current Quarter  Performance by Team](https://github.com/user-attachments/assets/e66a49f5-0d63-49a5-a25a-afacd276f25e)

**Performance Over Time**

The "Performance Over Time" dashboard shows how Celia Rouche’s team performed across various quarters in 2017, with metrics on total sales, new opportunities, agent sales contributions, and conversion rates by product. Here’s an analysis along with recommendations:

* **Key Insights**
  * **Total Sales by Quarter**:
    * Sales peaked in Q2 with approximately €600K but declined slightly in Q3 and further in Q4. This trend suggests a strong start after Q1 but difficulty in maintaining momentum in the latter half of the year.
    * The steady drop in sales in Q3 and Q4 might indicate seasonal fluctuations or challenges in converting opportunities in the latter part of the year.

  * **Agent Performance**:
    * Markita Hansen leads with total sales of €329K, followed by Elease Gluck(€289K), Hayden Neloms(€272K), and Rosalina Dieter(€235K). These agents represent top performers who contribute heavily to overall sales.
    * There may be an opportunity to provide additional training or resources for other agents to help lift their performance to match that of the top agents.

  * **New Opportunities by Quarter**:
    * The number of new opportunities peaked in Q3, reaching 394, before a sharp drop to 179 in Q4. This decrease aligns with the decline in total sales, suggesting that fewer new opportunities contributed to lower revenue in Q4.
    * The drop in new opportunities from Q3 to Q4 could be due to market conditions, a reduction in lead generation, or lower engagement efforts toward the end of the year.

  * **Conversion by Quarter and Product**:
    * Conversion rates were highest in Q1 (85.6%) and dropped significantly in Q2 (61.2%) and Q3 (60.1%), with a slight recovery in Q4 (61.8%).
    * GTX Basic maintained a relatively stable conversion rate but declined over the year from 88.2% in Q1 to 62.5% in Q4.
    * GTX Pro and MG Advanced showed fluctuations but had stronger conversion rates in Q4, reaching 60.7% and 70.8%, respectively. Products like GTX Plus Basic and GTX Plus Pro had lower conversion rates, indicating potential difficulties in converting these specific products.
 
![Performance Overtime](https://github.com/user-attachments/assets/7b56eb1c-f83f-4a10-a3a9-18d385a3caf5)

## Recommendations
  * **Enhance Lead Generation and Opportunity Conversion:** Given the drop in total sales and new opportunities decline, consider ramping up marketing and outreach efforts to generate more qualified leads. Collaborate with the marketing team to assess lead generation channels and campaigns.
  * **Targeted Agent Training:** Provide tailored training to agents like Markita Hansen to improve conversion rates and average sale values. Review her sales tactics, product knowledge, and customer interaction strategies.
  * **Product Strategy Adjustment:** Evaluate the underperformance of products like GTX Plus Basic and GTX Basic. Consider marketing strategies to improve product appeal or adjust pricing based on market research.Focus on products like MG Advanced and GTX 500 which have shown strong sales, potentially increasing inventory or promotional efforts around these high-performing items.
  * **Quarterly Goal Adjustments:** Given the downturn in sales and opportunities, revise quarterly targets and forecasts for the next period. Set realistic, data-driven goals based on current trends and work closely with the team to strategize on achievable objectives.
  * **Increase Focus on High-Performing Sectors**:Prioritize sales and marketing resources in the Retail, Finance, and Entertainment sectors. Tailor messaging to these industries and consider account-based marketing strategies to strengthen relationships and increase sales.
  * **Account Retention and Growth Strategy**: 1)Focus on building strong relationships with top accounts, especially Xx-holding, Cheers, and Singletechno. Implement loyalty programs, offer exclusive deals, or involve them in product feedback loops to increase customer satisfaction and retention. 2) For smaller accounts, analyze their growth potential. If they show promise, develop targeted sales tactics to convert them into larger accounts.

The dashboard can be found in Tableau Public [here](https://public.tableau.com/app/profile/xuelian.hu/viz/MavenTechSalesPerformance_17302157889770/CurrentQuarterPerformance?publish=yes). 
