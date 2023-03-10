# Amazon_Vine_Analysis

## Overview of Project
As a data expert I've been teamed with an account manager at BigMarket to analyze big data for the client SellBy.  Since our initial work was extremely successful we've been tasked with a second large project that involves analyzing Amazon reviews written by members of the paid Amazon Vine program.

### Purpose
The purpose of the project is to determine if there is any bias toward favorable reviews from Vine members in a Amazon review dataset for outdoor products.  PySpark will be used to perform ETL and the data will be loaded into pgAdmin tables.  Next, PySpark will be used to perform calculations and analysis to determine if there is bias or not. 

## Results
An initial step for the PySpark analysis was filtering the dataset first by retrieving all rows where the total_votes count is equal to or greater than 20, and second by taking the first filtered set and filtering to retrieve all rows where the number of helpful_votes divided by total_votes is equal to or greater than 50%.

![filter_total_votes_20](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/filter_total_votes_20.png)

![filter_helpful_50percent](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/filter_helpful_50percent.png)

* How many Vine reviews and non-Vine reviews were there?

![num_paid_reviews](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/num_paid_reviews.png)
![num_unpaid_reviews](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/num_unpaid_reviews.png)

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

![num_5star_paid_reviews](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/num_5star_paid_reviews.png)
![num_5star_unpaid_reviews](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/num_5star_unpaid_reviews.png)

* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

![percent_5star_paid_reviews](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/percent_5star_paid_reviews.png)
![percent_5star_unpaid_reviews](https://raw.githubusercontent.com/JBro-Birds/Amazon_Vine_Analysis/master/support_images_readme/percent_5star_unpaid_reviews.png)

## Summary
For the outdoor product category there is not positive bias for reviews made by members of the Vine program.  This is evident by comparing the percent of 5 star reviews by Vine members vs. reviews by non-Vine members which is almost identical; 52.3% for Vine members and 52.7% for non-Vine members.  To further enhance the bias analysis a comparison could be performed to show by each number of stars category the percentage of Vine reviews vs. non-Vine reviews.  This analysis would show if the non-bias claim holds true across more than a single star category. 
