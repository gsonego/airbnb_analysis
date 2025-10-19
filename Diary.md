# Group Project Diary: Progress and Interactions

## Overview

This diary summarizes the key project-related discussions and progress between group members Niall and Guilherme, focusing on the Airbnb Ireland dataset analysis for the Data Visualisation group project. Entries are chronological and include only relevant interactions, decisions, and tasks related to data selection, cleaning, exploration, and dashboard development. As per Jacks recommendation, we are using a shared project diary file as no situation exists for a individual diary file.

## 24/09/2025

- Discussed initial data cleaning approaches for the Airbnb dataset.

- Agreed to retain rows with missing `last_review` values, as they contain valuable information and are explained by the `number_of_reviews` column (e.g., new listings without reviews).

- Decided to keep missing `host_name` values and replace them with "unassigned," since `host_id` is present for all rows.

- Niall noted minimal overall cleaning needed based on initial exploration.

- Niall shared additional notes: Consider removing very old "last_review" entries if they indicate non-operational listings; convert `price` to numeric for statistical calculations; identify and potentially cap/remove `price` outliers using box plots; prepare for linear regression by encoding categorical variables like `room_type` (e.g., one-hot encoding into `room_type_shared`,`room_type_apartment`, etc.).

## 25/09/2025

Conducted a call to discuss dataset and cleaning ideas.
Shared updated dataset link via SharePoint for collaboration.
Confirmed access to the dataset.

## 28/09/2025

Guilherme requested the official source of the dataset for documentation.
Niall provided the link to Inside Airbnb, specifying the Ireland dataset (third from the bottom).

## 30/09/2025

- Discussed parsing a new `county` column from `region_parent_name` for cleaner analysis—agreed this is straightforward.

- Reviewed unique counties extracted: ['Wicklow' 'Cork' 'Limerick' 'Galway', etc..].

- Agreed to merge "South Dublin" and "Dun Laoghaire-rathdown" into "Dublin" for consistency, resulting in: ['Wicklow' 'Cork' 'Limerick' 'Galway' ... 'Dublin' ...].

- Guilherme shared GitHub repo containing: Dataset in XLSX and CSV formats; initial notebooks for investigation and cleaning (Airbnb_Customer.ipynb and Airbnb_Investor.ipynb, tailored to different user angles); cleaned datasets (Ireland_Airbnb_Listing\_\_Detailed\_\_Customer.csv and Ireland_Airbnb_Listing\_\_Detailed\_\_Investor.csv).

- Niall outlined data cleaning priorities: Replace missing `reviews_per_month` with 0 (logical for no-review listings); handle "price" outliers post-box plot analysis (to discuss further); encode categorical variables for regression (e.g., one-hot for "room_type"); remove "$" from "price" and convert to numeric (optionally to Euros using static rate); discuss feature selection for irrelevant columns on next call.

# 02/10/2025

Agreed to use Jupyter notebooks for data cleaning scripts (exportable to PDF for submission), with separate ones for customer and investor perspectives.
Guilherme updated the GitHub repo with cleaned datasets incorporating initial transformations.

Niall planned to build Power BI dashboard over the weekend and Tableau the following week.

# 05/10/2025

Niall shared a mock Power BI dashboard link for design feedback.
Guilherme requested and received access; provided screenshot feedback.

# 08/10/2025

Niall proposed adding a `number_of_amenities` column by counting items in the `amenities` column to enhance recommendation features (e.g., for customer budget/location-based top listings).
Agreed to implement; Niall to provide code.

# 10/10/2025

Niall shared KPI and metric ideas for dashboards, derived from key variables:

- Price: Average Daily Rate (ADR)
- Number_of_reviews: Total Listings Count
- Number_of_reviews_ltm: Average Reviews (Last 12 Months)
- Review_scores_rating: Average Guest Rating
- Availability_365: Average Occupancy Rate
- Host_is_superhost: Superhost Percentage

Noted flexibility to test other review variables.
Guilherme raised concerns about `price` outliers (e.g., dataset shows 50k+ but actual Airbnb site listings are 1203€, 609€, 574€); suggested removing outliers or invalid entries.
Agreed to sync on Sunday for dashboard support; Niall offered to help with Tableau.

# 11/10/2025

Guilherme questioned handling of price discrepancies (dataset vs. actual site prices); proposed removing outliers.

# 13/10/2025

Scheduled call for after 8pm the next day to discuss new code adjustments for data cleaning.
Guilherme shared class resources: YouTube video on Tableau; townlands.ie download link; Shiny lecture PDF.

# 14/10/2025

No new project decisions; confirmed ongoing work on data cleaning code.

# 19/10/2025

Project deadline
