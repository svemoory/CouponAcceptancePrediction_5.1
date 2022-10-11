# Will the Customer Accept the Coupon?

### Overview:

This a a practical application assignment for PCMLAI program from Berkeley Haas to answer the question, “Will a customer accept the coupon?” The goal of this project is to usevisualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not. Here is the link to the [Jupyter Notebook](https://github.com/svemoory/CouponAcceptancePrediction_5.1/blob/main/CouponAcceptancePrediction.ipynb).

### Data:
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc., and then asks people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50)

### Exploring Data Analysis (EDA)

The attributes of this data set include:

User attributes
* Gender: male, female
* Age: below 21, 21 to 25, 26 to 30, etc.
* Marital Status: single, married partner, unmarried partner, or widowed
* Number of children: 0, 1, or more than 1
* Education: high school, bachelors degree, associates degree, or graduate degree
* Occupation: architecture & engineering, business & financial, etc.
* Annual income: less than $12500, $12500 - $24999, $25000 - $37499, etc.
* Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
* Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
* Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
* Number of times that he/she eats at a restaurant with average expense less than $20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
* Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
* Contextual attributes
* Driving destination: home, work, or no urgent destination
* Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
* Weather: sunny, rainy, or snowy
* Temperature: 30F, 55F, or 80F
* Time: 10AM, 2PM, or 6PM
* Passenger: alone, partner, kid(s), or friend(s)
Coupon attributes
* time before it expires: 2 hours or one day

### Data Analysis and Visualization

#### Summary of findings based on Bar coupons:
After slicing and dicing the data from various categorical information, we can make the following observations:

* Undoubtedly, the drivers wo regularly go the bars atleast once a month have strong inclination towards accepting the bar coupons.
* The drivers with minors in the car are less likely to accept te bar coupons
* Marital Status doesnt really suggest a particular inclination towards the acceptance, although in conjunction wit the age, the acceptance rate goes up
* Low income drivers normally prefer dining an cheaper restaurants as compared to going to a bar.

#### Summary of findings based on Coffee House coupon:
* By exploring the coupon data and drilling into subcategories, we can derive the following observations:

* Just like the bar coupon category, the affinity to accept the coffee coupon is extremely strong for customers who have previously visited the coffee house atleast 1 or more times.

* Sunny weather with high 80s seems to draw a lot of customers towards coffee house. It can be the factor of more outgoing vacations/road trips during summer.

* Gender seems to have no impact on the acceptance rate of the coffe house coupons.

* Customers in the early adulthood seems to be inclined towards accepting coffee coupons. This could be because the millenials are more technology savvyand more exposure to social media which can drive them towards the coffee houses which offer more than just a beverage.

* Also, the customers who accept the coffee coupons do not seem to mind taking detours in opposite driving direction.

### Next steps and recommendations:
* I think we can reach a much better prediction model if we explore other coupon categories and visualize side by side

* The data in few categories for example age is not evenly distributed, we can be able to produce a better model, if we can collect more than than is normally distributed.

* A lot of categorical vectors data type did not allow a scatter plot because of string data.May be we can identify few dependent variables and try to correlate them to get more idea about the characteristics of the customer.

* Possibly merge the data with other user attributes like ethinicity, cuisine of restaurant, date/month of the year. This kind of data may give more cues about the kind of restaurants a customer may prefer. For example, a vegan.veg customer may have a unique preference to the typle of coupns that he/she accepts

* Explore the possibility of % discount the coupon is offering and the date of expiry. Does the user acceptance rate change if the coupon is valid anywhere in the state/radius?
