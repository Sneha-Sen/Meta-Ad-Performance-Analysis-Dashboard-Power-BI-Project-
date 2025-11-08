# Meta Ad Performance Analysis Dashboard (Power BI Project)
# Project Overview

This Power BI project analyzes Meta (Facebook + Instagram) Ad Campaigns to evaluate performance across awareness, engagement, and conversion stages.
The goal is to identify which ad types, audiences, platforms, and timings deliver the best ROI and engagement results — helping optimize digital marketing strategy and ad spend allocation.

The dashboard provides a funnel-based view of the marketing performance, allowing decision-makers to see where users drop off and how different demographics respond to ad content.

# Dataset Information

The dataset models real-world Meta Ads performance data, including campaign, ad, event, and user-level details.

**Tables Used**:

**ad_events**	Stores user interaction events (impressions, clicks, shares, purchases).	event_id, ad_id, user_id, timestamp, event_type
**ads**	Contains  ad-level details (type, platform, targeting).	ad_id, campaign_id, ad_platform, ad_type, target_gender, target_age_group
**campaigns**	High-level campaign data (budget, duration, goals).	campaign_id, name, start_date, end_date, total_budget
**users**	Stores user demographics and interests.	user_id, gender, age_group, country, interests

# Data Model:
A Star Schema was created:

Fact Table: ad_events

Dimension Tables: ads, campaigns, users

# Data Modeling & KPIs

Key measures were created in Power BI using DAX to track marketing performance:

CTR = DIVIDE(SUM(Clicks), SUM(Impressions))
Engagement Rate = DIVIDE(SUM(Engagements), SUM(Impressions))
Conversion Rate = DIVIDE(SUM(Purchases), SUM(Clicks))
Purchase Rate = DIVIDE(SUM(Purchases), SUM(Impressions))
Avg Budget per Campaign = DIVIDE(SUM(Total Budget), DISTINCTCOUNT(CampaignID))

Main KPIs:

Impressions: 216K

Clicks: 25.4K

CTR (Click-Through Rate): 11.76%

Engagement Rate: 13.56%

Purchases: 1.3K

Conversion Rate: 5.21%

Purchase Rate: 0.61%

Total Budget: 2.5M

Average Budget per Campaign: 50.7K

# Dashboard Features

1. KPI Overview Section:
Highlights the core performance metrics and conversion funnel.

2. Demographic Analysis:

Gender: Females (43%) engage more than males (22%).

Age Group: Highest engagement among 18–30 years.

3. Geographic Insights:

Top engagement from India, US, Brazil, Germany, UK.

India/Brazil for volume, Germany/UK for high-value audiences.

4. Time Analysis:

Hourly: Peak user activity during afternoons & evenings (3 PM – 8 PM).

Calendar View: High engagement on 19–21 & 25–27 June, likely during promotions.

# Business Impact

Improved understanding of customer behavior and ad engagement patterns.

Data-driven strategy to increase conversion rate and ROI.

Actionable insights for audience targeting, budget optimization, and creative direction.

# Learnings

Data modeling with fact-dimension structure in Power BI.

Building advanced DAX measures for marketing KPIs.

Creating interactive visuals for storytelling and business decision-making.

Understanding of digital marketing metrics (CTR, ROAS, CPM, CPC, etc.).

# Tools & Technologies Used

Microsoft Power BI — dashboard design & DAX modeling

Power Query Editor — data transformation

MS Excel / CSV — data source

DAX (Data Analysis Expressions) — calculated measures and KPIs
