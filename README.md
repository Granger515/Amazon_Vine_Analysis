# Amazon_Vine_Analysis

An analysis of Amazon review data on video games was conducted. The data was extracted. Four dataframes were created using Spark on Google Colab. These frames were  loaded into pgAdmin. Data from reviews were further divided using Spark into Vine reviews and other reviews. A brief analysis of positivity was completed.

## Initial extraction of Data

Four dataframes were created.

1. A Customers Table: containing customer IDs and frequencies

2. A Products Table: containing product IDs and product titles

3. A Review ID Table: containing revie IDs, customer IDS, Product IDs, product parent, and review dates

4. A Vine Table: containing review IDs, star ratings, help vote counts, total votes, whether it was a Vine review or not, and whether it was a verified purchase or not

##Exploration of Review data

The Vine Table was further parsed and analyzed

1. The Vine Table from the previous portion was filtered to only include reviews with 20 or more votes. It was further filtered to only include reviews with a helpful vote to total vote ratio of 0.50 or greater (50%).

2. The filtered Vine table was further filtered into two tables. One table contained only reviews by Vine members while the other table contained only reviews by non-Vine members.

3. A count of total reviews, a number of five-star reviews, and a percentage of five-star reviews of total reviews was obtained for both of the previous datasets.

##Results

1. Vine Reviews contained 94 reviews, of which 48 (51.1%) were five-star reviews.

2. Non-Vine reviews contained 40,471 reviews, of which 15,663 (38.7%) which were five-star reviews.

##Summary

The results suggest that Vine reviews are likely to be more positive than non-Vine reviews suggesting that paid reviews are, unsurprisingly, more likely to be favorable to the product. The analyses were very surface level and did not take into account any of the non-five star reviews. It would be more complete to analyze the data using a comparison of means analysis, such as a t-test. This in itself may also be incomplete as unsolicited reviews are often completed by those with much praise or much criticism. Looking at the frequency of each number of starred reviews using a Chi-square would provide even further depth the analysis.
