# Coupon Dataset Analysis

Analysis of the UCI Machine Learning Repository Coupon Acceptance dataset.

Notebook can be found here: [Will the Customer Accept the Coupon?](https://github.com/afadlallah/UCB/blob/master/01%20Practical%20Application%20Assignment%205.1%20-%20Will%20the%20Customer%20Accept%20the%20Coupon/Practical%20Application%20Assignment%205.1%20-%20Will%20the%20Customer%20Accept%20the%20Coupon.ipynb)

## Features

Feature | Values | Description
| --- | --- | --- |
destination | Home, No Urgent Place, Work | Driving destination
passanger | Alone, Friend(s), Kid(s), Partner | Passangers in the car
weathe | Rainy, Snowy, Sunny | Weather conditions
temperature | 30, 55, 80 | Temperature in Fahrenheit
time | 7AM, 10AM, 2PM, 6PM, 10PM | Time of the day in Hour:Minute format
coupon | Bar, Carry out & Take away, coffeehouse, Restaurant(<20), Restaurant(20-50) | Coupon category - Restaurant(<20) and Restaurant(20-50) mean restaurants where the expense per person is less than $20 and between $20-$50 respectively
expiration | 2h, 1d | When does the coupon expire
gender | Female, Male | Driver's gender
age | below21, 21, 26, 31, 36, 41, 46, 50plus | Driver's age grouped in bins
maritalStatus | Divorced, Married partner, Single, Unmarried partner, Widowed | Driver's marital/relationship status
has_children | 0, 1 | Whether driver has children or not
education | Some High School, High School Graduate, Some college - no degree, Associates degree, Bachelors degree, Graduate degree (Masters or Doctorate) | Driver's highest education degree obtained
occupation | Architecture & Engineering, Arts Design Entertainment Sports & Media, Building & Grounds Cleaning & Maintenance, Business & Financial, Community & Social Services, Computer & Mathematical, Construction & Extraction, Education&Training&Library, Farming Fishing & Forestry, Food Preparation & Serving Related, Healthcare Practitioners & Technical, Healthcare Support, Installation Maintenance & Repair, Legal, Life Physical Social Science, Management, Office & Administrative Support, Personal Care & Service, Production Occupations, Protective Service, Retired, Sales & Related, Student, Transportation & Material Moving, Unemployed | Driver's occupation
income | Less than $12500, $12500 - $24999, $25000 - $37499, $37500 - $49999, $50000 - $62499, $62500 - $74999, $75000 - $87499, $87500 - $99999, $100000 or More | Driver's income range
car | Car that is too old to install Onstar :D, crossover, do not drive, Mazda5, Scooter and motorcycle | Car type
Bar | never, less1, 1~3, 4~8, gt8 | Number of times respondent goes to a bar every month
CoffeeHouse | less1, never, 1~3, 4~8, gt8 | Number of times respondent goes to a coffeehouse every month
CarryAway | never, less1, 1~3, 4~8, gt8 | Number of times respondent eats take away food every month
RestaurantLessThan20 | never, less1, 1~3, 4~8, gt8 | Number of times respondent eats at a restaurant where the expense per person is less than $20 every month
Restaurant20To50 | never, less1, 1~3, 4~8, gt8 | Number of times respondent eats at a restaurant where the expense per person is between $20 to $50 every month
toCoupon_GEQ5min | 0, 1 | Driving distance to the venue for the coupon is greater than 5 minutes
toCoupon_GEQ15min | 0, 1 | Driving distance to the venue for the coupon is greater than 15 minutes
toCoupon_GEQ25min | 0, 1 | Driving distance to the venue for the coupon is greater than 25 minutes
direction_same | 0, 1 | Is the venue for the coupon in the same driving direction as the driver's destination?
direction_opp | 0, 1 | Is the venue for the coupon in the opposite driving direction as the driver's destination?
Y | 0, 1 | Did the respondent accept the coupon? (1 if they answered 'right away' or 'later before the coupon expires'; 0 if they answered 'no, I do not want the coupon')

## Methods & Preliminary Findings

- The dataset was analyzed using Python and the Pandas/Numpy libraries.
- Visualizations were created using Matplotlib and Seaborn to explore relationships between features.
- The dataset contains 12,684 rows and 26 columns.
- 12,576 values in the `car` column were missing, so this feature was dropped from the analysis as it did not provide useful information.
- There were also missing values in the following colums: Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, Restaurant20To50
  - Missing values were imputed using the mode of the column
- Percentage of Coupons Accepted: 56.84%

## Analysis of the `Bar` Feature

- Percentage of Bar Coupons Accepted: 41.00%<br><br>
- Percentage of Bar Coupons Accepted by Those Who Go to the Bar <=3x per Month: 37.07%
- Percentage of Bar Coupons Accepted by Those Who Go to the Bar >3x per Month: 76.88%<br><br>
- Percentage of Bar Coupons Accepted by Those Who Go to the Bar >=1x per Month and are >25 Year Old: 69.52%
- Percentage of Bar Coupons Accepted by All Others 33.50%<br><br>
- Percentage of Bar Coupons Accepted by Those Who Go to the Bar >=1x per Month, Had Non-Kid Passangers, and Had Occupations Other Than Farming, Fishing, or Forestry: 71.32%
- Percentage of Bar Coupons Accepted by All Others 29.60%<br><br>
- Percentage of Bar Coupons Accepted by Those Who Go to the Bar >=1x per Month, Had Non-Kid Passangers, and Were Not Widowed: 71.32%
- Percentage of Bar Coupons Accepted by Those Who Go to the Bar >=1x per Month and are <30 Years Old: 72.17%
- Percentage of Bar Coupons Accepted by Those Who Go to Cheap Restaurants >=4x per Month and Whose Income is <$50K: 60.07%

### Interpretation

1. Younger individuals (under the age of 30) who frequent bars more than once a month have the highest acceptance rate for bar coupons. This could be due to the fact that younger individuals are more likely to go to bars and are more likely to be open to trying new bars.
2. Those who go to the bar more than once a month, did not have kid passangers, and are not involved in farming, fishing, or forestry occupations had the second highest acceptance rate, and this was tied with >once a month bar goers who did not have a kid passanger and who were not widowed. This suggest that there may be a social element to accepting bar coupons and going to bars.
3. Drivers who visit bars more than once a month are significantly more likely to accept bar coupons, perhaps because they see more value in the coupon.
4. Drivers who frequent cheaper restaurants and have a lower income also have a considerable rate of accepting coupons, although this group had the lowest acceptance rate. This suggests that individuals who are budget-conscious or have limited disposable income find value in such coupons.
5. The high acceptance rates across the specified groups (ranging from 60% to 72%) suggest that targeted marketing strategies could be very effective. These specific demographics can be focused on to achieve a high return on marketing investment.

## Analysis of the `CoffeeHouse` Feature

### Methods & Findings

- Explored the 'CoffeeHouse' feature
- Calculated and visualized how various features affect the acceptance rate of coffeehouse coupons
- Then I further explored certain features to try to determine the characteristics of those most likely to accept coffeehouse coupons
- Findings:

  - Percentage of Coffeehouse Coupons Accepted: 49.92%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who Have No Urgent Place to Go: 58.10%
  - Percentage of Coffeehouse Coupons Accepted by Those Who Have Other Destinations: 40.36%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling With Friend(s) or a Partner: 59.17%
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling Alone or With Kid(s): 44.17%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling in Rainy or Sunny Weather: 50.47%
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling in Snowy Weather: 43.23%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling in Hot Weather: 52.98%
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling in Cold Weather: 45.33%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling at 10AM: 64.07%
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Traveling at Other Times: 45.82%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Under 21 Years Old: 69.68%
  - Percentage of Coffeehouse Coupons Accepted by Those >=21 Years Old: 49.13%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Not Widowed: 50.06%
  - Percentage of Coffeehouse Coupons Accepted by Those Who are Widowed: 35.14%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who Go to the Coffeehouse <1x per Month: 48.04%
  - Percentage of Coffeehouse Coupons Accepted by Those Who Go to the Coffeehouse >=1x per Month: 66.02%<br><br>
  - Percentage of Coffeehouse Coupons Accepted by Those Who Go to the Coffeehouse >=1x per Month and are <=21 Years Old: 71.28%
  - Percentage of Coffeehouse Coupons Accepted by All Others 46.42%

### Interpretation

After exploring and analyzing the `CoffeeHouse` feature, I found five broad factors that affect the acceptance rate of coffeehouse coupons:

1. Convenience
   - If people are driving without a specific destination, they are more open to diversions like stopping at a coffeehouse. This makes them more likely to accept a coffeehouse coupon. On the other hand, those driving to work or their home are less inclined to take a detour, leading to a lower acceptance rate.
2. Social Factors
   - Traveling with a friend or partner seems to make the idea of a coffeehouse stop more appealing, thus increasing coupon acceptance. On the other hand, traveling alone or with children leads to a lower acceptance rate.
   - This factor, along with the convenience factor, matches what one would expect: that going to coffeehouses is seen as a leisure and social activity.
3. Environment
   - Moderate weather conditions like rain or sunshine don't influence acceptance much, keeping the rate around the baseline. Snowy weather, on the other hand, likely makes it more difficult and not worth the effort to make a stop, leading to a lower acceptance rate. Likewise, hot weather lead to a small increase in acceptance, while cold weather lead to a larger decrease.
   - The time of day showed a strong effect on acceptance - with 10am having a nearly 20% higher acceptance rate than other times.
   - These results suggest that morning time and hot weather conditions might create a more conducive environment for a coffeehouse visit, perhaps due to people wanting a morning boost or a cold drink.
4. Demographics
   - People under 21 are substantially more likely to accept coffeehouse coupons than those 21 and older. This is likely due to a combination of social and financial factors, flexible schedules, and fewer responsibilities.
   - Windows showed a much lower acceptance rate than all other marital statuses, perhaps due to a more solitary lifestyle or different daily habits.
5. Habits
   - Existing habits strongly influence future behavior, and those who visit coffeehouses at least once per month are much more likely to accept a coffeehouse coupon. This is may be due to the fact that these individuals visit coffeehouses on a consistent basis, while those who answered '<1x per month' may not be regular coffeehouse visitors, and those who answered 'never' may not be interested in coffeehouses at all. These latter two groups likely thus see less value in the coupon.

The additive effects of these factors can be seen when comparing the acceptance rates of those who are both 21 or younger and who visit coffeehouses at least once per month, and all others - the former group has the highest acceptance rate out of all the groups analyzed at 71.28%.
