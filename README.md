## Amazon_Vine_Analysis

Module 16  Big Data

Completed by Angela Kumar

### Purpose

Enter the world of Big Data as you perform ETL (Extract, Transform, Load) on a dataset from Amazon.

### Overview

We'll start by reviewing Hadoop and its ecosystem.

Within this big data and Hadoop context, we'll cover MapReduce and how it has improved the process for handling big data. We'll then move on to PySpark, which has become the leading technology for handling big data.

After diving into some of the technologies used with big data, we'll look at natural language processing (NLP) in relation to big data.

We'll close with an introduction to cloud services. Cloud services let us store large amounts of data at remote locations rather than locally, on top of many other services. This allows for more scalability and performance. We'll use the most popular cloud service available: Amazon Web Services (AWS).

### Resources

Data: challenge_schema.sql; Amazon_Reviews_ETL_Starter_code.ipynb converted to Amazon_Reviews_ETL.ipynb
Amazon Dataset https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt

Technologies: Google Colab;Pyspark; AWS RDS, PgAdmin4: Postgres SQL; VSCode;

### Background

Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. 
The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. 
Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. 
You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 
Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

### Deliverables

* Deliverable 1: Perform ETL on Amazon Product Reviews

Using your knowledge of the cloud ETL process, you’ll create an AWS RDS database with tables in pgAdmin, pick a dataset from the Amazon Review datasets (Links to an external site.), and extract the dataset into a DataFrame. 
You'll transform the DataFrame into four separate DataFrames that match the table schema in pgAdmin. Then, you'll upload the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded.

An Amazon Review dataset is extracted as a DataFrame 

The extracted dataset is transformed into four DataFrames with the correct columns 

All four DataFrames are loaded into their respective tables in pgAdmin 

* Deliverable 2: Determine Bias of Vine Reviews

Using either PySpark, Pandas, or SQL, follow the instructions below to complete Deliverable 2.

Filter the data and create a new DataFrame or table to retrieve all the rows where the total_votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful and to avoid having division by zero errors later on.

Filter the new DataFrame or table created in Step 1 and create a new DataFrame or table to retrieve all the rows where the number of helpful_votes divided by total_votes is equal to or greater than 50%.

If you use the SQL option below, you’ll need to cast your columns as floats using WHERE CAST(helpful_votes AS FLOAT)/CAST(total_votes AS FLOAT) >=0.5.
Filter the DataFrame or table created in Step 2, and create a new DataFrame or table that retrieves all the rows where a review was written as part of the Vine program (paid), vine == 'Y'.

Repeat Step 3, but this time retrieve all the rows where the review was not part of the Vine program (unpaid), vine == 'N'.

Determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).


* Deliverable 3: A Written Report on the Analysis (README.md)

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists and images of DataFrames as support, address the following questions:

How many Vine reviews and non-Vine reviews were there?
How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?


### Summary
Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
