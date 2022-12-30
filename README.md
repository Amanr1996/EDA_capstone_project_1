
# **Hotel Bookings Exploratory Data Analysis**
**Objective**

Our main objective is to perform Exploratory data analysis on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.

Dataset We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

**Table of Content**

    1. Motivation
    2. Tools and Libraries Used
    3. Files
    4. Result
    5. Dataset Information
    6. Acknowledgements

**Dataset**

    We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

    - hotel: Name of hotel ( City or Resort)
    - is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
    - lead_time: time (in days) between booking transaction and actual arrival.
    - arrival_date_year: Year of arrival
    - arrival_date_month: month of arrival
    - arrival_date_week_number: week number of arrival date.
    - arrival_date_day_of_month: Day of month of arrival date
    - stays_in_weekend_nights: No. of weekend nights spent in a hotel
    - stays_in_week_nights: No. of weeknights spent in a hotel
    - adults: No. of adults in single booking record.
    - children: No. of children in single booking record.
    - babies: No. of babies in single booking record. 
    - meal: Type of meal chosen 
    - country: Country of origin of customers (as mentioned by them)
    - market_segment: What segment via booking was made and for what purpose.
    - distribution_channel: Via which medium booking was made.
    - is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
    - previous_cancellations: No. of previous canceled bookings.
    - previous_bookings_not_canceled: No. of previous non-canceled bookings.
    - reserved_room_type: Room type reserved by a customer.
    - assigned_room_type: Room type assigned to the customer.
    - booking_changes: No. of booking changes done by customers
    - deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
    - agent: Id of agent for booking
    - company: Id of the company making a booking
    - days_in_waiting_list: No. of days on waiting list.
    - customer_type: Type of customer(Transient, Group, etc.)
    - adr: Average Daily rate.
    - required_car_parking_spaces: No. of car parking asked in booking
    - total_of_special_requests: total no. of special request.
    - reservation_status: Whether a customer has checked out or canceled,or not showed 
    - reservation_status_date: Date of making reservation status.

**Total number of rows** : 119390

**Total number of columns**: 32

**Data Cleaning and Feature Engineering**

    1. Handling null values
    Null values in columns company and agent were replaced by 0.
    Null values in column country were replaced by 'others'.
    Null values in column children were replaced by the mean of the column.
    2. Removing Duplicate rows.All duplicate rows were dropped.
    3. Handling null values
    Null values in columns company and agent were replaced by 0.
    Null values in column children were replaced by the mean of the column.
    4. Converting columns to appropriate data types
    Changed data type of children, company, agent to int type.
    5. Removing outliers
    One outlier was found in the adr column. Simply dropped it.
    Creating new columns
    6. Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
    7. Created new column total_people by adding adults+children+babies.

**Exploratory Data Analysis**

    Performed EDA and tried answering the following questions:
    1. Which Hotel type getting maximum bookings?
    2. Which hotel seems to make more revenue?
    3. Which hotel has higher bookings?
    4. Which hotel has higher bookings in weekend nights?
    5. Which agent having maximum number of confirm bookings?
    7. From which country the most guests are coming ?
    8. who are the top ten agents making world wide bookings?
    9. Paris uses which agents the most?
    10. France uses which agents the most?
    11. Spain uses which agents the most?
    12. Deutch uses which agents the most?
    13. Israel uses which agents the most?
    14. What is the confirmation rate of the top 20 agents?
    15. What is the cancelation rate of the top 20 agents?
    16. Which year having highest number of stays?
    17. which is the highest revenue generating month in 2015 ?
    18. which is the highest revenue generating month in 2016 ?
    19. which is the highest revenue generating month in 2017 ?
    20. On which day in every month there were the highest stays?
    21. No which Day in a month ther were lowest stays?
    22. Which meal type is most preffered meal of customers?
    

    Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:

    Bar Plot.
    Scatter Plot.
    Pie Chart.
    Line Plot.
    Heatmap.


**Univariate Analysis**:

    Performed univariate analysis and made following conclusions:

    1. City hotels seems to make more revenue.

    2. City hotel has higher bookings in weekend nights.

    3. Agent no. 9 has made most no. of bookings.

    4. City hotels has higher bookings in weekend nights.

    5. Agent no. 9 has made most no. confirmed bookings.

    6. Most of the guests arfe coming from Portugal.

    7. In Portugal agent no. 240 has highest number of bookings and over 3000+ bookings are from agent no. 9.

    8. In france agent no. 9 has highest number of bookings.

    9. In in spain agent no. 9 has highest number of bookings and over 2000+ bookings are from agent no. 240.

    10. In Deutch agent no. 9 has highest number of bookings.

    11. In Israel agent no. 240 has highest number of bookings and over 700+ bookings are from agent no. 9.

    12. 2016 has highest number of stays. 

    13. Highest cancelation percent is fro agent no. 9 which is 40%. ther is 40 percent chance that the booking from agent no.9 get canceled.

    14. lowest cancelation percentage is from agents no 243, no.27, and no. 22. 

    15. there are highest no. of stays in 2016.

    16. September is the highest revenue generating month in 2015 and lowest revenue is from July and November.

    17. August is the highest revenue generating month in 2016.

    18. May is the highest revenue generating month in 2017.

    19. On day 3 and 6 and day 17 an 27 in every month there were the highest stays.

    20. on day 8, 15 and 23 has lowest stays.

    21.  meal type BB is most preffered meal of customers.
    
 
**Bivariate Analysis** :

We tried to answer following questions

 * Overall adr of City hotel is slightly higher than Resort hotel and no. of bookings of City hotel is also higher than Resort hotel. Hence, City hotel is makes more revenue.
 * Almost 30 % of City Hotel bookings got canceled.
 * TA/TO is mostly used for planning Hotel visits well ahead of time. 
 * Around 60% bookings are for City hotel and 40% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel. Also the overall adr of City hotel is slightly higher than Resort hotel.
 * Most of the guests came from european countries, with most of guests coming from Portugal.
 * Guests use different channels for making bookings out of which most preferred way is TA/TO.
 * July- August are the most busier and profitable months for both of hotels. 

And many more conclusions.

**Challenges**

1. There was a lot of duplicate data.
2. Data was present in wrong datatype format.
3. Choosing appropriate visualization techniques to use was difficult.
4. A lot of null values were there in the dataset.
