---

Date: September 30, 2025
Task: Cleaning region_parent_name column

Today, I cleaned the region_parent_name column in our Airbnb dataset, removing "County Council" and "City Council" to get just the county names (e.g., "Dublin" from "Dublin City Council"). I used a simple pandas script with str.replace(), checked the results with unique(), and saved the cleaned data as a CSV. I pushed the code to our GitHub repo and updated the README.
