# Telecom-Churn Analysis

### TABLE OF CONTENT
- [PROJECT OVERVIEW](#Telecom Churn Analysis)
- DATA SOURCE
- TOOLS
- OBJECTIVES
- DATA UNDERSTANDING
- EXPLORATOTY DATA ANALYSIS
- DASHBOARD
- OBSERVATIONS
- RECOMMENDATIONS

### Project Overview
This Project analyzes customer churn behavior in a telecom dataset, focusing on how service features, pricing, and payment methods influence churn.
The goal is to identify high-risk customer segments, revenue exposure, and pricing patterns that contribute to customer attrition.

## Objectives
- Define and measure customer churn within the business context.
- Identify key customer behaviors and subscription patterns associated with churn.
- Provide actionable insights to support targeted customer retention strategies.

## Step 1: Data Understanding
The dataset contained 7,043 records and 21 variables such as: Demographics (gender, senior citizen, dependents),Subscription details (contract type, internet service, add-ons), Usage and billing data (tenure, monthly charges, total charges). Churn rate - 26.5%, Retention rate -73.5%

## Design & Color Logic
Color usage in this dashboard is intentional.
Red represents the category with higher churn impact, while green represents lower churn impact.
Tooltips and slicers are used across all visuals to dynamically check churn rate, revenue, average revenue, monthly charges, average monthly charges, and revenue lost to churn for deeper analysis.

## Exploratory Data Analysis (Overview Dashboard)
- Loss revenue from churn by dependents
Customers without dependents has the most loss revenue from churn, contributing  $115k compared to $24k from customers with dependents. This suggests that single-user customers are significantly more likely to churn and represent a higher revenue risk segment.

- Loss revenue from churn by contracts
Month to Month contract has a higher loss of $121k, followed by one year which had $4k and 2 year which had $2k meaning more early customer churn faster than those that stays longer.

- Average Monthly Charges(churn vs retention) by dependents
Across both dependent and non-dependent segments, churned customers pay higher monthly charges than retained customers, suggesting pricing is a key churn problem.

- Average tenure (churn vs retention) by dependents
Customers with dependents tend to have longer tenures. Even when they churn, they do so later compared to customers without dependents.
This suggests dependents are associated with more stable customer behavior, not higher churn risk.

- contract performance overview
This visual compares customer contract types by average tenure, while revealing deeper performance metrics through interactive tooltips. 
Longer-term contracts(2 years) show significantly higher customer retention and lower churn rates.
Although month-to-month contracts may generate frequent transactions, they experience earlier churn and higher revenue loss.

<img width="1262" height="710" alt="Screenshot 2026-01-30 140127" src="https://github.com/user-attachments/assets/0936d121-a230-4ce9-b298-43f13389ef85" />

### Insight Dashboard
The insight dashboard consist of using services features to analyze where the problem is coming from using a slicer that dynamically helps you check through churn rate, revenue, avg revenue, monthly charges, avg monthly charges, loss revenue from churn.

- Streaming Movies 
* What happened: Customers subscribed to Streaming Movies recorded a higher churn rate (29.9%) compared to those without the service (24.4%). Despite this, Streaming Movies users generated significantly more revenue ($10,274 vs $5,782).
* Why it happened: Streaming Movies users also had much higher average monthly charges ($88.48) compared to non-users ($49.73), indicating that churn in this segment is likely driven by higher price rather than low engagement.
* What this means: High-value customers are churning due to high cost. Retention strategies for this group should focus on pricing incentives, bundled discounts.

- Online Backup
This is a value-added service that stores customer data securely in the cloud, increasing service dependency and switching costs.
* What happened:Customers without Online Backup churn significantly more (29.2%) than those with Online Backup (21.5%). Also, customers with Online Backup generate higher total revenue ($9.4M vs $6.65M) and higher average revenue per customer.
* Why it happened: Customers with Online Backup pay higher average monthly charges ($83.08 vs $55.12) yet still churn less.This indicates that customers are willing to tolerate higher costs when they receive services they perceive as valuable.
* What this implies: This is not a case where higher price reduces churn.The perceived value of Online Backup offsets price sensitivity, making it a strong retention feature.

- Tech Support
Tech Support gives customers access to assistance for service and connectivity issues, reducing frustration and service disruption.
* Insight: Customers with Tech Support churn less (15.2%) despite higher average monthly charges ($80.68),Customers without Tech Support churn more (31.2%) and contribute most to revenue lost from churn ($2.04M).
* What this implies: This indicates churn in this segment is driven more by lack of support than by pricing, access to support significantly reduces churn and protects revenue.

- Device Protection
This covers damage, loss, or replacement of customer devices, reducing risk and service disruption.
* Insight: Customers without Device Protection churn the most (39.1%), while those with Device Protection churn significantly less (22.5%), despite paying higher average monthly charges ($84.82). Customers with no internet service show very low churn (7.4%) but also contribute minimal revenue.

- Multiple Lines
This allow customers to manage more than one phone line under a single account, increasing account complexity and usage.
* Insight: Customers with Multiple Lines generate the highest revenue ($10.47M) and pay higher average monthly charges ($82.04) but also churn slightly more (28.6%). Customers without Multiple Lines churn less (25.0%) and contribute far less revenue.
* What this implies: Multiple Lines increase customer value but also amplify churn risk due to higher costs.Retention strategies in this segment should focus on pricing stability and bundled incentives.

- Streaming TV
Streaming TV provides access to television content over the internet as an add-on service.
* Insight: Customers with Streaming TV churn more (30.1%) than those without (24.3%), despite generating significantly higher revenue ($10.17M vs $5.89M) and paying much higher average monthly charges ($88.74).
* What this implies: Higher churn among Streaming TV users is strongly linked to higher monthly charges rather than low engagement.

- Payment Method
* Insight: Customers using Electronic Check churn the most (45.3%), far higher than all other payment methods, despite generating the highest revenue ($4.9M) and having the highest average monthly charges (76). Automatic payment methods (Bank Transfer and Credit Card) show the lowest churn (16.7% and 15.2%), even with similar revenue levels.

- Internet Service
* Insight: Fiber Optic customers churn significantly more (41.9%) than DSL (19.0%) and No Internet Service customers (7.4%), despite generating the highest revenue ($9.9M) and paying the highest average monthly charges (92). DSL customers show a balanced profile of moderate pricing and much lower churn.
N.B: Higher churn among Fiber Optic users is closely linked to higher pricing, not low usage.

<img width="1255" height="717" alt="Screenshot 2026-01-29 222756" src="https://github.com/user-attachments/assets/2d65ab5b-23f9-46c3-909f-4d428ba1f3f8" />

### Churn dashboard
- Churn Rate by Monthly Charge Group
Churn increases as monthly charges rise.
High ($70–90): 38.0%,Very High (>$100): 32.9%,Medium ($50–70): 20.2%,Low (<$50): 15.7%
* Insight: Customers paying the most are more likely to churn than those on cheaper plans.

- Churn Rate by Paperless Billing
Customers using paperless billing churn at 33.6%, compared to 16.3% for non-paperless users.
* Insight: Customers on paperless billing churn more because they are typically more digital and less tied to one provider, making it easier for them to switch.

- Churn Rate by Tenure Group
Churn declines consistently as tenure increases:
(0–12 months: 47.4%, 13–24 months: 28.7%, 26–48 months: 20.4%, 49+ months: 9.5%)
* Insight: Most customers who leave do so in their early months. Customers who stay longer are more likely to be stable and loyal.

- Churn Rate by Online Security
Customers without Online Security churn at 31.3%, while those with it churn at 14.6%.
* Insight: Online Security is a clear retention feature. Customers who opt in are significantly more stable, even though such services comes with higher monthly charges(78.84 vs 59.10) they are less likely to churn.

<img width="1265" height="685" alt="Screenshot 2026-01-30 122058" src="https://github.com/user-attachments/assets/6af87237-01ce-4657-aa99-e1648bb78301" />


## Business Recommendations
- Focus retention efforts on early-tenure customers especially those with high monthly charges.
- Review pricing and onboarding experience because early dissatisfaction is a major churn driver.
- Promote Value-added services like Online Backup, Tech Support and Device Protection.
- Encourage longer-term contracts.
- Adopt the use of automatic payment methods.
- Focus on digital experience improvements for paperless billing and streaming services.






