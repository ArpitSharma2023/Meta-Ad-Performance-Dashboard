# Meta-Ad-Performance-Dashboard
This is a Meta Ad Performance Dashboard that tracks the effectiveness of ad campaigns across key KPIs such as impressions, clicks, engagements, conversions, and budget. It provides a complete funnel view—from awareness to engagement to purchases—along with demographic, geographic, and time-based insights." 
## Project Explanation in Interview 
Step 1: Give a High-Level Overview 
"This is a Meta Ad Performance Dashboard that tracks the effectiveness of ad campaigns across key KPIs such as impressions, clicks, engagements, conversions, and budget. It provides a complete funnel view—from awareness to engagement to purchases—along with demographic, geographic, and time-based insights." 

Step 2: Walk Through the Funnel Metrics 
"At the top of the funnel, the ads generated 216K impressions and 25.4K clicks, giving a very high CTR of 11.76%. This is well above the industry average, which tells me the ad creatives and targeting were very effective in attracting attention. 
The engagement rate is also strong at 13.56%, showing users are interacting with the content. However, when we move down the funnel, only 1.3K purchases were made, giving a conversion rate of 5.21% from clicks and a purchase rate of 0.61% from impressions. This indicates a big drop in efficiency from engagement to purchase." 
Key takeaway you highlight to interviewer: “The ads are good at generating awareness and engagement, but the purchase funnel is leaking heavily—likely due to landing page experience, audience mismatch, or weak offers.” 

Step 3: Break Down by Audience 
"Looking at demographics, females (43%) engage more than males (22%), and the 18–30 age group drives the majority of interactions. This shows the core audience is young females. 
From a geographic perspective, India and Brazil are the biggest engagement markets, while Germany and the UK likely represent higher-value audiences with stronger purchasing power. So, campaigns should be tailored differently for high-volume vs. high-value regions." Data Tutorials YT 

Step 4: Time & Seasonality 
"The dashboard shows consistent weekly engagement, but hourly trends peak in the afternoon and evening hours. This suggests that ads should be scheduled and budget-weighted towards those times to maximize ROI. 
The calendar highlights certain days (19th–21st, 25th–27th) with spikes in engagement, which could be linked to promotions or campaign launches. This indicates that event-based campaigns drive higher performance." 

Step 5: Ad Type Performance 
_"When we compare formats, Video ads perform best, with the highest CTR, conversion rate, and engagement rate. Stories ads also perform strongly, while images and carousels lag slightly in conversion efficiency. 
This suggests that the budget should be shifted more towards video and story ads, as they generate the best return per dollar spent."_ 

Step 6: Wrap Up with Insights & Recommendations 
"In summary: 
1.	Strong awareness & engagement, but low purchase efficiency → optimize landing pages, retargeting, and offers. 
2.	Target audience = young females, 18–30, in India & Brazil → refine campaigns accordingly. 
3.	Best formats = Video and Stories → increase spend here. 
4.	Best times = afternoons & evenings → schedule ads accordingly. 
5.	Geography → volume from India/Brazil, value from Germany/UK → segment strategies.
   
## About the Data 
This dataset represents Meta Ads Performance Data, covering campaigns, ads, user demographics, and ad interaction events. It is modelled after how Facebook/Instagram (Meta) ad platforms capture data. 
The purpose of this dataset is to analyse advertising performance, optimize targeting, and measure ROI (Return on Investment) through KPIs such as: 
•	Impressions (how often ads are seen) 
•	Clicks (engagement with ads) 
•	Purchases (conversions) 
•	CPM, CPC, CTR, and ROAS (efficiency metrics) 
•	Audience insights (demographics, location, interests) 

This dataset is ideal for building a Power BI Dashboard to evaluate campaign effectiveness, budget utilization, and user engagement patterns. 
## Use of Each Table 
Table 1: ad_events 
•	Stores event-level logs (like impressions, clicks, purchases). 
•	This is the fact table in the model because all KPIs are derived from events. 
•	Used to analyze when and how users interact with ads. 

Table 2: ads 
•	Contains details of each ad creative. 
•	Defines targeting criteria and which campaign an ad belongs to. 
•	Used for platform-level and creative-type-level analysis (e.g., Facebook Video Ads vs Instagram Image Ads). 

Table 3: campaigns 
•	High-level campaign strategy and budget allocation. 
•	Provides timeframe and budget for ads. 
•	Used to calculate cost-based KPIs (CPC, CPM, ROAS). 
Table 4: users 
•	Stores demographic and interest information of users who interact with ads. 
•	Used for audience segmentation (gender, age, country, location, interests). 
•	Helps analyze targeting efficiency (are ads reaching the right audience?). 

## Table and Field Details 
Table 1: ad_events 
Purpose: Captures every interaction (event) between a user and an ad. Field 	Description 	Example 	Use in Analysis 
event_id 	Unique identifier for each event 	100234 	Used as primary key for the table 
ad_id 	Links to ads table 	501 	Join with ads → get ad_platform, ad_type 
user_id 	Links to users table 	U_1204 	Join with users → get demographics 
timestamp 	Exact time of event 	2025-03-12 14:30:00 	Build date hierarchy (Day, Week, Month) 
day_of_week 	Derived field: day of the week 	Tuesday 	To compare weekday vs weekend performance 
time_of_day 	Derived field: segment of day 	Afternoon 	See when users engage most 
event_type 	Type of event: Impression, Click, Share, Comment, Purchase 	Click 	Funnel analysis (Impressions → Clicks → Purchases) 

## DASHBOARD INSIGHTS 
KPI Metrics 
•	Impressions: 216K: Total times the ads were shown. Good reach. 
•	Clicks: 25.4K: Number of people who clicked on the ads. 
•	Shares: 1.3K, Comments: 2.6K: Indicators of organic engagement (beyond paid reach). 
•	Purchases (Conversions): 1.3K: Real customer acquisitions from ads. 
•	Engagements: 29K: Sum of clicks, likes, shares, comments. 
•	CTR (Click-Through Rate): 11.76%: Strong performance (above industry average ~1-2%). Ads are very attractive. 
•	Engagement Rate: 13.56%: Very healthy; content resonates with the audience. 
•	Conversion Rate: 5.21%: Out of all clicks, 5.21% converted into purchases. Good but could improve with landing page optimization. 
•	Purchase Rate: 0.61%: Out of impressions, only 0.61% resulted in purchases. Low conversion funnel efficiency (room to optimize). 
•	Total Budget: 2.5M: Total ad spends. 
•	Avg Budget per Campaign: 50.7K: Suggests multiple campaigns were run. 

Insight: Ads are performing strongly in visibility and engagement, but actual purchase efficiency is weak: need to optimize targeting/landing pages. 
•	High CTR (11.76%) and Engagement Rate (13.56%) → clearly indicate that the ad creatives, messaging, and targeting at the top of the funnel are very effective. People are interested enough to click, like, share, or comment. 
•	Low Purchase Rate (0.61%) and only 1.3K conversions out of 216K impressions → shows a sharp drop-off in the lower funnel. This is a classic case of "awareness and interest" being strong but "action (purchase)" being weak. 

Engagement Breakdown 
•	By Gender (Donut Chart) Female: 13K (43%) 
•	Male: 6K (22%) 
•	Other/Not Specified: 10K (35%) Females engage more than males; campaigns could be tailored toward female audiences. 
•	By Target Age (Bar Chart) Peak engagement: 20–30 age group (especially early 20s). 
•	Drops significantly after 35+. Primary audience = Young adults. 
Insight: Target ads towards females aged 18–30 for better ROI. 

Geographic Distribution 
	Top Engaged Countries US, India, Brazil, Germany, UK are major contributors.. 
Insight: Focus campaigns in India & US (high potential, high engagement), and premium campaigns in Germany/UK (better conversion potential due to higher purchasing power). 

Time-Based Trends 
•	Weekly Engagement Trend (Stacked Bar) Fairly consistent across weeks, with no sharp drop. 
•	Steady engagement shows ads maintain attention. 
•	Hourly Engagement Trend (Line Chart) Peaks around late afternoon & evening (~15–20 hours). 
•	Lowest engagement early morning (~0–5 hours). 
•	Insight: Schedule ad delivery during afternoons & evenings for maximum impact. Data Tutorials YT 

Calendar View 
•	Engagements are mapped to days in June. 
•	Certain dates (like 19th–21st, 25th–27th) show higher highlights. Campaign activity peaks on specific days, possibly due to launches/promotions. 
Insight: Weekly promotions/events significantly drive engagement. 

Analysis by Ad Type (Bottom-Right Table) Ad Type 	Impressions 	Clicks 	CTR 	Purchase Rate 	Conversion Rate 	Engagement Rate 
Carousel 	48K 	6K 	11.7% 	0.59% 	5.1% 	13.4% 
Image 	51K 	6K 	11.7% 	0.57% 	4.9% 	13.5% 
Stories 	72K 	8K 	11.8% 	0.65% 	5.2% 	13.6% 
Video 	46K 	5K 	11.9% 	0.62% 	5.2% 	13.7% 

