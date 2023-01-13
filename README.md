# Amazon Vine Analysis
## Overview
The purpose of the Amazon Vine analysis is to analyze Amazon reviews written by paid Amazon Vine program members and determine if there is any bias toward favorable reviews from Vine members in a selected dataset.  As part of the project access was granted to approximately 50 datasets; the dataset chosen for this analysis was Clothing Apparel. [^1]

In order to perform the analysis, we will utilize PySpark to extract the dataset, transform the data and load into PgAdmin via AWS RDS connection. Once we had the final data results, we utilized PySpark via Google Colab to analyze the data to determine if there is any bias between Vine and Non-Vine members.


## Results
The Vine dataset contained over 5 million records, as such we narrowed our focus to the records that had a total vote greater than or equal to 20 and the percentage of helpful votes where greater than or equal to 50%.

Analysis results:
Vine members accounted for 0.07% of the reviews and non-Vine members accounted for 99%. 

### Total Number of Reviews
- #### Vine Reviews

![vine_paid_reviews](https://user-images.githubusercontent.com/112449480/212217290-f76ab81f-4d7b-427e-a3fe-ada502f903fd.png)

- #### Non-Vine Reviews

![vine_nonpaid_reviews](https://user-images.githubusercontent.com/112449480/212217844-2d0452b3-4d78-40f3-8881-2ac56c261bfc.png)

### Total 5-Star Reviews
- #### 5-Star Vine Reviews

![vine_paid_5star_reviews](https://user-images.githubusercontent.com/112449480/212217304-539d864a-3cb5-4045-9069-15e443203ee8.png)

- #### 5-Star Non-Vine Reviews

![vine_nonpaid_5star_reviews](https://user-images.githubusercontent.com/112449480/212218052-417b39f8-e4ee-4b60-8c5c-efb300d2f91c.png)


### Percentage 5-Star Reviews
- #### Percentage 5-Star Vine Reviews

![vine_paid_5star_percent](https://user-images.githubusercontent.com/112449480/212217379-1313984a-d520-4b54-8db5-defa146e3264.png)


- #### Percentage 5-Star Non-Vine Reviews

![vine_nonpaid_5star_percent](https://user-images.githubusercontent.com/112449480/212218236-2ba20e82-3ceb-4761-946b-c739fef5f908.png)

## Summary
In reviewing the results, 45% of Vine members reviews were 5-star and 52% were Non-Vine members.  As Vine members reivew were 6% lower than Non-Vine member, there is not bias towards Vine members.  However further analysis would need to be conducted to support the answer; as less than 1% were Vine members.

The suggested analysis would be to review the all 5-Star ratings for Vine and Non-Vine members. In addition, the analysis could be performed using a another dataset to support our answer. 


[^1]: Utilize some of description from Module 17 work to assist in writing my background for the Challenge
