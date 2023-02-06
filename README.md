# Amazon_Vine_Analysis

## Overview

- The purpose is to analyze Amazon reviews written by members of the paid Amazon Vine program to determine if there is any bias toward favorable reviews from Vine members in the dataset.

## Sources

- Data Source: AWS [AWS_Data](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Books_v1_02.tsv.gz)

- Softwares: 

	1. Google Colab
	2. PGAdmin
	3. Jupyter Notebook

- Scripts:

	1. Amazon_Reviews_ETL [Amazon_Reviews_ETL](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Scripts_Codes/Amazon_Reviews_ETL.ipynb)
	2. SQl_Schema [Amazon_review_schema](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Scripts_Codes/Amazon_review_schema.sql)
	3. Vine_Review_Analysis [vine_review_analysis](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Scripts_Codes/vine_review_analysis.ipynb)

## Results

### Phase 1

- Using Pyspark, load the data file in to a dataframe. The dataframe is shown below:

![DataFrame](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/dataframe.png)

- From the above dataframe extract the customer dataframe. The Customer DataFrame is shown below:

![customer_df](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/customers_df.png)

- Extract the products dataframe from the main dataframe. The Products DataFrame is shown below:

![products_df](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/products_df.png)

- Extract the review dataframe from the main dataframe. The Review DataFrame is shown below:

![Review_id_df](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/review_id_df.png)

- Extract the Vine dataframe from the main dataframe. The Vine DataFrame is shown below:

![Vine_df](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/vine_df.png)


### Phase 2

- Load the Vine DataFrame. The dataframe is shown below:

![vine_data_df](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/Vine_data.png)

- Checking data for paid vine program reviews. The image is as shown below:

![vine](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/vine_paid_reviews_Y.png)

- Filter the dataframe for the total votes greater than 20. The dataframe is as shown below:

![total_votes_20](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/tital_votes_greater_20.png)

- Filter the above dataframe for votes greater than 50%. The dataframe is as below:

![more_than_50%](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/more_than_50%25.png)

- Count the number of paid reviews in the Vine Program.

![No_reviews_paid](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/no_reviews_paid.png)

- Count the number of unpaid reviews in the Vine Program.

![reviews_unpaid](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/unpaid_reviews.png)

- Filter the number of 5 star reviews.

![5star_reviews](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/5star_reviews.png)

- Calculate the percentage of 5 star reviews.

![percent_unpaid](https://github.com/manasidek/Amazon_Vine_Analysis/blob/main/Images/percent_unpaid.png)


## Summary

- There are only 2 paid reviews in this dataset and both have fewer than 20 votes. So, we do not have enough paid reviews in this dataset to arrive at any conclusions on the positivity bias for reviews in the Vine program.

- Another analysis that could be done using this dataset would be to compare a summary of reviews across verified and non-verified purchases.

