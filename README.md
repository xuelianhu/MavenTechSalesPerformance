# Maven Tech Sales Insights - Project Overview
## The goal of this project is to investigate the quarterly performance of sales teams at Maven Tech in order to track their sales opportunities.
For the Maven Sales Performance Project, I played the role of a BI Developer for MavenTech, a company that specializes in selling computer hardware to large businesses. They've been using a new CRM system to track their sales opportunities but have no visibility of the data outside of the platform.

## Dataset Structure
The dataset contained records exported from MavenTech's CRM from October 2016 to December 2017. It held details of opportunities with associated information such as product, account, and whether the sale was won or lost.

<img width="451" alt="Screenshot 2024-10-29 at 16 11 07" src="https://github.com/user-attachments/assets/178e6486-1cd9-4214-a482-dad19e4299af">

## Key Assumptions
When creating an interactive dashboard, I always like to chat with the users to make sure I truly understand the intended purpose and the questions they seek to answer with the dashboard. In the absence of being able to chat with the sales managers, I made the following key assumptions which I used to guide my dashboard design.

* The main goal for sales managers is viewing the current state of play for their team, and obtaining actionable information. The key questions they want to answer are:
  * How is my team (as a whole and individual team members) tracking against our key KPIs?
  * Are there team members who require extra support in certain areas?
  * Where should I focus my efforts for the rest of the quarter to improve performance?
  * Is my team performing above average compared to the rest of the business?
* Their main KPI is the dollar value of sales made, however related metrics such as number of sales, conversion %, and average sales value are also important and help to understand their total sales value.
* They may also at times want to dive deeper and look at their team's performance over the year or in comparison to the other sales teams.
* As the dashboard is intended for the sales managers, the most important view to them is to see their own team, rather than an Exec dashboard with higher level team comparisons. They may however like to look at other sales teams in more detail and there is no requirement for row level security to prevent them access to other team data.
* It is assumed that the "Current quarter" is Q4 2017, which is the latest time period recorded in the dataset, however in reality this dashboard would continuously update over time as new data is added.

## The Dashboard
As the dashboard is interactive, I also focused on making it user friendly for audiences who may not use Power BI every day. If the sales managers don't feel comfortable using the dashboard, there's no value to be gained. For this reason, I added a help page covering basic dashboard functionality and defining how the key metrics were calculated. This ensures sales managers canconfidently navigate the dashboard, and clearly interpret the information they are seeing and answer their key questions.

The dashboard sections are explained further below.

**Current Quarter Performance**

![Current Quarter Performance](https://github.com/user-attachments/assets/a4708276-68db-46f2-a1d9-b511d1440e10)

This is the main page of the report, containing the most critical information for sales managers. Users select their name from the sales manager filter, and this populates all pages of the dashboard with their team's information.

The key KPIs are shown clearly at the top of the page, with figures for the previous quarter and the average figure across all sales team for each metric provided below for additional context. This allows the sales manager to see their own figures and understand generally how they are tracking against the remaining teams and towards their own goals.

Users can click the question mark to view more information about the dashboard, and see a definition of how each metric has been calculated, to assist with interpreting the dashboard.

From the total sales card, users can click the arrow to dive deeper into the sales breakdown for the current quarter. This helps them to understand where they've had success and even see itemised sales data if required.

![Current Quarter Sales](https://github.com/user-attachments/assets/ad72c717-9adb-44cf-a664-fbaf7c3f36ce)


From the potential to close card, managers can also dive deeper into all opportunities labelled as engaging for their team. They can use this detail to prioritise actions such as following up offers to close before end of quarter, and CRM cleanups e.g., opportunities that have been open for too long and need to be marked as lost.

![Open Opportunities Report ](https://github.com/user-attachments/assets/205c4cdf-8bb7-4b01-968c-00343c32c861)

The current quarter performance page then steps deeper into the data, with the key KPIs listed against each individual sales agent, and conditional formatting highlighting in red which team members may be struggling in a particular area. This allows the sales manager to identify both areas they can focus on to improve the performance, and individuals who may require additional support. The product level breakdown also helps identify specific areas of improvement for the team as a whole and individuals.

**Performance by Team**

While it's not the most important goal for the sales managers, they would also like to be able to see how their team is performing in comparison to the remaining sales team. The current quarter performance by team page allows them to do this, by ranking all sales teams across the key metrics, and highlighting the selected team so managers can easily see where they stand.

![Current Quarter  Performance by Team](https://github.com/user-attachments/assets/e66a49f5-0d63-49a5-a25a-afacd276f25e)

**Performance Over Time**

The final page of the dashboard allows sales managers to view their team's performance over the previous quarters to identify trends.

![Performance Overtime](https://github.com/user-attachments/assets/7b56eb1c-f83f-4a10-a3a9-18d385a3caf5)


The dashboard can be found in Tableau Public [here]([https://public.tableau.com/app/profile/xuelian.hu/viz/RowHealthDashboard_17263079833780/Dashboard?publish=yes](https://public.tableau.com/app/profile/xuelian.hu/viz/MavenTechSalesPerformance_17302157889770/CurrentQuarterPerformance?publish=yes)). 
