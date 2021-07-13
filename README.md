# Overview
The Amazon Vine program is a service that helps manufacturers and publishers garner reviews for the products. These companies are able to pay a small fee and provide reviewers with their products to Amazon Vine members in return for reviews.

We are interested in determining if there is a bias towards favourable reviews from these paid vine members. To investigate this, I have analyzed a dataset of reviews using PySpark to transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 

# Results
Analysis of the reviews left in software products by unpaid reviewers versus paid Vine reviews revealed the following:
- In total, 17,514 of the reviews were unpaid, while only 248 were from paid Amazon Vine reviews.
- Of the 248 Vine reviews, 102 were 5-star reviews. This consists of 41.13% of the total paid reviews.
- Of the 17,514 unpaid reviews, only 5,154 (29.43%) were five-star.

# Summary
These results show that paid reviewers are more likely to leave 5-star reviews than their unpaid counterparts. Given that this is purely observational analysis, these findings do not speak to causality. The observed findings could suggest that paid reviewers are biased towards positive reviews. They could also indicate that companies willing to offer free products to reviewers are more likely to offer their best products or that paid reviewers apply for the program because they feel a strong desire to receive products and are more positively receptive to items they purchased or those provided for free. 

I think the analysis of this set to compare their reviews of the products they paid for versus those they didn't would provide the most insight into whether or money spent or a norm of reciprocity leads to them leaving more positive reviews on items they received for free. In order to determine if this insight is possible to glean from the currently available dataset, one would have to group by customer id and see if there is data on both vine-associated reviews and unpaid reviews for the same customer. The dataset could then be filtered to only those customers who provided both paid and unpaid reviews. The average star rating and the number of helpful votes for each user could be aggregated. These measures could then be compared in a paired sample t-test for any statistically significant difference in means.
