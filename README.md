# Amazon_Vine_Analysis

## Overview
The Amazon Vine program provides members with products free of charge, and in exchange members must document and publish a product review.  Since this differs from typical customers who pay for the same products, there is the potential for positive review bias to influence the reviews of vine members.  In order to test this, a dataset of watch reviews from both program and non-program individuals was analyzed using PySpark in Google Colab.

## Results

#### Vine Program Reviews
![v-prog](https://github.com/Mots94/Amazon_Vine_Analysis/blob/main/Images/vine_program.PNG)  

#### Non-Vine Program Reviews
![no-v-prog](https://github.com/Mots94/Amazon_Vine_Analysis/blob/main/Images/non_vine_program.PNG)

* The vine program had a total of 43 reviews in this dataset, 14 of which were five star reviews.

![v-count](https://github.com/Mots94/Amazon_Vine_Analysis/blob/main/Images/v_program_counts.PNG)

* There were 7,720 non-vine program reviews and 4018 of those reviews received five stars.

![non-v-count](https://github.com/Mots94/Amazon_Vine_Analysis/blob/main/Images/no_v_program_counts.PNG)

* Of the total vine program reviews, 32.56% were given a five star rating.  The non-vine program reviews had about 52.05% of the reviews rated with five stars.

![v-perc](https://github.com/Mots94/Amazon_Vine_Analysis/blob/main/Images/v_program_perc.PNG)

![non-v-perc](https://github.com/Mots94/Amazon_Vine_Analysis/blob/main/Images/no_v_program_perc.PNG)

## Summary
According to these results, there does not appear to be a noticeable positive review bias of vine program reviews compared to non-vine program reviews.  However, the sample of 43 vine reviews is much smaller than the sample of 7,720 non-vine reviews.  It is possible that the small sample of vine reviews does not accurately capture how vine reviewers typically rate watch reviews.  In order to test if there really is no bias, I would decrease the ratio of helpful votes to total votes metric to allow for reviews that were not rated highly on the helpful_votes variable.  There may be other vine reviews in this dataset with high positive reviews that were not rated as very helpful by customers because of a number of things.  One possibility is that the review was simply done in haste without providing much detail.  Adding more data to the vine reviews filtered dataframe may reveal other patterns.