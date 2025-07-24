# Required Assignment 5.1: Will the Customer Accept the Coupon?
Jupyter Notebook Assignment Link: https://github.com/marlonkolivas/practical_application_one/blob/main/practical_application_one.ipynb
## Coupon Acceptance Analysis
This project explores consumer behavior around coupon acceptance, specifically focusing on **Bar** and **Coffee House** coupons. The analysis uses visualization and statistical methods to understand how different demographic and contextual factors influence the likelihood of coupon acceptance.

## Data

This data is from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver. There are three possible answers people can choose from:

- “Right away”
- “Later, before the coupon expires”
- “No, I do not want the coupon”

## Key Visualization

- **Heatmaps**: Correlation between categorical features and coupon acceptance
- **Bar Charts**: Acceptance rates by passenger type, gender, education, and income
- **Line Plot**: Acceptance trends across different times of the day
- **Box Plot**: Age distribution by passenger type
- **Grouped Bar Plots**: Comparison of acceptance rates across multiple demographics

## Tools & Libraries

- **Python**
- `pandas`, `numpy`
- `seaborn`, `matplotlib`, `plotly`
- `sklearn.preprocessing.LabelEncoder` (for encoding categorical data)

# Investigating the **Bar** Coupon

1. To investigate and focus only on the Bar coupon, I filtered the dataset by setting the coupon column equal to 'Bar' and then reset the index.
   
2. **What proportion of bar coupons were accepted?** <br>

      To calculate the proportion of accepted Bar coupons. I first counts how many Bar coupons were accepted (Y == 1), then divides that by the total number of Bar   coupons       to get the acceptance rate. Finally, it prints the proportion formatted to two decimal places.
   
3. **Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.**<br>

      To compare the coupon acceptance rates between two groups based on how frequently they visit bars. I filter the data into two categories: those who go to bars 3 or           fewer times per month and those who go more than 3 times, then calculates and visualizes the acceptance rates for each group using a bar plot. The result clearly             shows that those who visited bars more than three times a month were more likely to accept the coupon. Frequent bar-goers might see more value in the coupon since they       are likely to use it, making them more inclined to accept it.

4. **Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others. Is there a difference?** <br>

   To compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 with all others, I started by converting the age              categories into numeric values using mapping. Then, I filtered the dataset into a target group (frequent bar-goers over 25) and a comparison group (all others). The code calculates and compares the coupon acceptance rates for both groups using a pie chart and prints the acceptance rates along with the difference between them. Based on the results, there is a noticeable difference in acceptance rates between drivers who go to a bar more than once a month and are over the age of 25 and all other drivers. One possible reason for the higher acceptance rate among drivers who go to bars more than once a month and are over the age of 25 is that they may be more socially active and open to trying new places or offers, making them more likely to accept coupons for bars.

5. **Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry.**

   To compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry, I begin by filtering bar_coupons to define a target group: ndividuals who go to bars more than once a month, are not traveling with kids (passanger is not 'kid(s)'), and do not work in farming, fishing, or forestry. It then defines the "all others" group by removing the target group from the original dataset. Next, it calculates the coupon acceptance rates (Y) for both groups. These rates are plotted in a vertical bar chart using Matplotlib, with acceptance rates. The target group, drivers who go to bars more than once a month, are not with kids as passengers, and do not work in farming, fishing, or forestry, had a higher coupon acceptance rate compared to all other drivers. Excluding those in farming, fishing, and forestry, who may work irregular hours or in rural areas, means the target group may have better access to bars and more predictable routines.

6.  **Compare the acceptance rates between those drivers who:**

- go to bars more than once a month, had passengers that were not a kid, and were not widowed *OR*
- go to bars more than once a month and are under the age of 30 *OR*
- go to cheap restaurants more than 4 times a month and income is less than 50K.

    By calculating and comparing acceptance rates across these groups, **frequent bar-goers without kids or widowed status**, **younger adults under 30, and moderate-income frequent restaurant visitors** I identified profiles with higher responsiveness to bar coupon offers. The results were visualized using a bar chart for easy comparison. The results show that all three target groups had higher acceptance rates compared to the general population. The group of frequent bar-goers who are not widowed and don’t travel with kids showed the highest acceptance, suggesting that social and independent lifestyle factors may influence receptiveness to bar coupons.

7. **Based on these observations, what do you hypothesize about drivers who accepted the bar coupons?**

     The bar chart titled “Bar Coupon Acceptance Rate: Three Target Groups” compares how likely three groups are to accept bar coupons. The group with the highest acceptance rate (70%) comprises monthly bar patrons without children or not widows. Socially active individuals without dependents or emotional burdens are more receptive to bar offers. The second group (under 30 who frequent bars) has a slightly lower acceptance rate (68–69%). Younger individuals are open to deals but may be less consistent in accepting them. The third group (dining out frequently and earning less than $50K) has the lowest acceptance rate (45%). Their spending priorities may not align with bar environments due to budget constraints. Lifestyle and personal circumstances seem to influence coupon receptiveness more than age or income alone.

   # Independent Investigation

Using the bar coupon example as motivation, you are to explore one of the other coupon groups and try to determine the characteristics of passengers who accept the coupons.<br>
Kindly see attached Jupyter Notebook for the Independent Investigation 

**Next step and Recommendations** 

Feature engineering, classification models, and data cleaning can enhance coupon targeting. Targeted promotions based on demographics and occupations, along with personalized offers, can improve acceptance rates.
