# Coupon-Acceptance-Analysis
Distinguish between customers who accepted coupons to those who did not using UCI ML repository data

## Analysis File Location
Coupon Acceptance Analysis/prompt.ipynb

## Findings

### Overall
- The data contains 12,684 rows and 26 columns. The 'car'column is sparsely populated and was dropped before analysis. 
- Overall, about 57% chose to accpet the coupon.
- Coffee House coupons were handed out the most.
- There were more coupons distributed in higher temperature as more people are out then.
- Coffee coupons occured more frequently at higher temperatures mostly at 80F. But at 30F it was carry out coupons that had the highest count(781) and coffe house coupons were about 300.
- Another intersting findings related to temperature was that at 80F the coupon acceptance rate overall went up to 60% whereas it is around 53% at other temperatures.

### Bar Coupons
- 59% of bar coupons were accepted which is slightly more than overall rate.
- Bar Coupon acceptance rate for people who went to bars more than 3 times was about 77% whereas those who went less than that the acceptance rate was only 37%.
- Those over 25 who went to the bar more than once had a acceptance rate of about 70% as opposed to others who had 34% acceptance rate. Using both chi squared and t-test, we could reject the null hypothesis that the acceptance rates for the two groups were the same.
- The bar coupon acceptance rate for the group with no kid passengers, go to bars more than once and work in an industry other than Farming, Fishing and Forestry is 71.32%. The acceptance rest of bar coupons for all others is 29.6%.
- The bar coupon acceptance rate for drivers who go to bar more than once, have no kid passengers and are not widowed or who go to bar more than once and are under 30 or who eat at cheap restaurants more than 4 times and earn less than 50k is 58.89%.

### Coffee Coupons
Since Coffee House coupons are so prevelant in the data, I examined them in addition to bar coupons.
- Those who went to coffee houses 4 or more times accpeted coffee house coupons at 67.5% whereas those who went less ( non/light coffee drinkers) accepted only 44.96% of times.
- The acceptance rate for males is 48.46% whereas for females it is 34.06%.
- Acceptance rate for people over 30 is 46.81% whereas for those under 30 is 53.43%.
- In conclusion, we can say that males under 30 are more likely to accept coffee coupons(about 53% acceptance rate) compared to the rest (about 48% acceprtance rate)
- We can also examine realtionship with other factors/variables in future analysis

## Data

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).


### Data Description

The attributes of this data set include:
1. User attributes
    -  Gender: male, female
    -  Age: below 21, 21 to 25, 26 to 30, etc.
    -  Marital Status: single, married partner, unmarried partner, or widowed
    -  Number of children: 0, 1, or more than 1
    -  Education: high school, bachelors degree, associates degree, or graduate degree
    -  Occupation: architecture & engineering, business & financial, etc.
    -  Annual income: less than \\$12500, \\$12500 - \\$24999, \\$25000 - \\$37499, etc.
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater
    than 8
    -  Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or
    greater than 8
    -  Number of times that he/she eats at a restaurant with average expense less than \\$20 per
    person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8

2. Contextual attributes
    - Driving destination: home, work, or no urgent destination
    - Location of user, coupon and destination: we provide a map to show the geographical
    location of the user, destination, and the venue, and we mark the distance between each
    two places with time of driving. The user can see whether the venue is in the same
    direction as the destination.
    - Weather: sunny, rainy, or snowy
    - Temperature: 30F, 55F, or 80F
    - Time: 10AM, 2PM, or 6PM
    - Passenger: alone, partner, kid(s), or friend(s)

3. Coupon attributes
    - time before it expires: 2 hours or one day
