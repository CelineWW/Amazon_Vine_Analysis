# Amazon_Vine_Analysis
## Overview 
The Amazon Vine program allows vendors and sellers to provide free or discount products to Vine members to recevie reviews for their products. SellyBy is a company considering to enroll in this program to reqiure reviews from Amazon Vine members. This project aims to analyze Amazon reviews to reveal if there is any difference between Vine reviews and Non-Vine reviews. The result will help SellyBy to check if there is any positivity bias for reviews in the Vine program, so the manager can make a decision on whether enrolling in Amazon Vine program or not.
- Use PySpark and Amazon RDS to perform ETL on Amazon office product reviews.
- Create table and Export data to local disk in PgAdmin.
- Read data into PySpark DataFrames.
- Perform anlysis on vine table by filtering PySparkDataFrame.

## Resources:
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Office_Products_v1_00.tsv.gz

## Tools:
Amazon RDS, Amazon S3 bucket, Google Colab notebook
PySpark, PgAdmin 


## Results:
- Raw data for Amazon office product reviews.
  - All in One DataFrame
  
   ![Amazon Review DataFrame](https://user-images.githubusercontent.com/105877888/189426978-b25ee1fb-983c-4ec3-a1de-f7fd8b850911.png)


  - Customers Information
 
    <img width="269" alt="Customers_table" src="https://user-images.githubusercontent.com/105877888/189424395-7e4684ea-8ee7-4dd6-9410-e61cd2a0e9e6.png">

  - Products Infomation
 
    <img width="308" alt="Products_table" src="https://user-images.githubusercontent.com/105877888/189424422-e7ed7342-2988-4aa0-baa2-fe323bff0f2f.png">
 
  - Review ID 
 
    <img width="582" alt="Review_id_table" src="https://user-images.githubusercontent.com/105877888/189424444-bffa35ec-cce6-41cb-a7c5-c86ed2bc5939.png">

  - Vine Reviews
 
    <img width="682" alt="Vine_table" src="https://user-images.githubusercontent.com/105877888/189424460-59341ec5-af1c-4137-8156-6ecdaa1e35c2.png">

- DataFrames Created From Vine Review Data Source
  - All Reviews
 
    ![All_Reviews](https://user-images.githubusercontent.com/105877888/189426024-6441c19b-72f1-4265-a5cf-5bb7e3b5b315.png)
    
  - Valid Reviews
  
   ![Valid_Reviews](https://user-images.githubusercontent.com/105877888/189426666-727a942a-ea0d-4bdb-a3b1-44807f66f9c6.png)

  - Helpful Reviews
  
    ![Helpful_Reviews](https://user-images.githubusercontent.com/105877888/189426692-34f1e2af-6e11-4290-9c87-bf23b70e9f41.png)

  - Paid Reviews
  
    ![Paid_Reviews](https://user-images.githubusercontent.com/105877888/189426718-cfb7fde9-6730-4f39-bd10-4344d5829aca.png)

  - Unpaid Reviews
  
    ![Unpaid_Reviews](https://user-images.githubusercontent.com/105877888/189426747-60fc5233-bc57-4f6f-8769-62d2aed1468c.png)

- Vine Table Analysis Summary

    ![Vine_Review_Analysis Summary](https://user-images.githubusercontent.com/105877888/189427264-f3ef1b60-5379-4b2a-862b-081d46b1f805.png)

    
      ```
      +------------------+--------------+------------------+
      |                  | Vine Reviews | Non-Vine Reviews |
      |------------------+--------------+------------------|
      | Total Reviews    |      969     |      43745       |
      |------------------+--------------+------------------|
      | 5-star Reviews   |      430     |      19233       |
      |------------------+--------------+------------------|
      | % of 5-star      |      44.38   |      43.97       |
      +------------------+--------------+------------------+
      ```


Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
The written analysis has the following:


The summary states whether or not there is bias, and the results support this statement (2 pt)
An additional analysis is recommended to support the statement (2 pt)
