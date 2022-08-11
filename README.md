# amazon_vine_analysis

## Purpose

To analyze amazon review data to determine if there is review bias amongst vine members.

## Resources
- python
- pyspark
- sql
- pgadmin
- amazon aws
- amazon s3
- google colab

## Analysis Results

For this analysis we chose amazon video game reviews.  From this, we consolodated the games with only 20 or more reviews.

This resulted in:
Vine Reviews: 90
Non-Vine Reviews: 37831

<img width="199" alt="Screen Shot 2022-08-11 at 5 14 56 PM" src="https://user-images.githubusercontent.com/6634774/184243516-c6e496a9-3be8-47b3-b3fb-97b5e850e05b.png">

This is a drastic difference in the number of reviews.  Based on this disparity, it will be hard to draw any bias conclusions.  We then took the video games with 20 or more reviews, and split these into 2 separate data frames, those reviews made by members of vine, and those who are not members.  We were able to draw the above counts from those dataframes. 

We also filtered and counted the number of 5-star reviews from both types. 

<img width="525" alt="Screen Shot 2022-08-11 at 5 17 09 PM" src="https://user-images.githubusercontent.com/6634774/184243863-f1504228-fdbb-43b2-a6c0-bc298837585e.png">

From this we were able to take the percentage of 5 star reviews from the total reviews of each category. 

<img width="593" alt="Screen Shot 2022-08-11 at 5 17 49 PM" src="https://user-images.githubusercontent.com/6634774/184243968-0b2ef6f7-63e8-4a4a-9068-639ee965e7ec.png">

## Summary

From the data shown above, it seems as if vine members rated games with 5 stars, nearly 10% more than non-vine members do.  Based on this alone, we coulud theoretically draw the conclusion that members of vine are bias towards rating games higher; however, based on the data avaialable, this is logically a hard theory to support.

1. Number of reviews.  Vine had 90 reviews and Non-vine had 37000, this is a huge disparity, and without more vine reviews it is not reasonable to say that vine members review games higher. 

2. Average reviews.  We have no basis of comparison.  What are the average number of stars for each category?  This would provide slightly more light as to how each group is rating games, and if there is a positivity bias for either group.  

3. Positivity Bias? At this point it is uncertain.  It would feel irresponsible to say there is (or isn't) a bias based on the limited selection of vine-member reviews.  

## Additional Study

1.  Firstly, we would want to look at the average review score for each membership type accross all games.  Comparing that average would give us slightly more leverage to pursue a yes/no in the positivity bias conversation.

2.  Normalize/consolodate data.  Seeing as how there are vastly more non-vine reviews; we may be able to run a t.test to see any trends within either data sample.  Taking a (smaller) random sampling from the non-vine members and comparing that mean to the population, as well as, to the vine members, would allow us to pursue a positivity bias recommendation for vine vs non-vine members.

3.  Visualize/Contextualize.  Breaking this data down further into game genres, looking at what time of year the reviews were made and removing any non-verified reviews, would allow us to give a better analysis recommendation based on this data. 



