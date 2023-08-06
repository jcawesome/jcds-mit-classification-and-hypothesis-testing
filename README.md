# Hotel Booking Cancellation Prediction
## Introduction
In this notebook, I will try and use different techniques I have learned from the **Classification and Hypothesis Testing** course under the MIT - "Data Science and Machine Learning: Making Data-Driven Decisions" Program.

## Business Case
**Context:** 
> The objective of the project is to analyse the data provided to find which factors have a high influence on booking cancellations, build a predictive model that can predict which booking is going to be cancelled in advance, and help in formulating profitable policies for cancellations and refunds.

**A significant number of hotel bookings are called off due to cancellations or no-shows.** Typical reasons for cancellations include change of plans, scheduling conflicts, etc. This is often made easier by the option to do so free of charge or preferably at a low cost. This may be beneficial to hotel guests, but it is a less desirable and possibly revenue-diminishing factor for hotels to deal with. Such losses are particularly high on last-minute cancellations.

The new technologies involving online booking channels have dramatically changed customers’ booking possibilities and behavior. This adds a further dimension to the challenge of how hotels handle cancellations, which are no longer limited to traditional booking and guest characteristics.

This pattern of cancellations of bookings impacts a hotel on various fronts:

1. Loss of resources (revenue) when the hotel cannot resell the room.
2. Additional costs of distribution channels by increasing commissions or paying for publicity to help sell these rooms.
3. Lowering prices last minute, so the hotel can resell a room, resulting in reducing the profit margin.
4. Human resources to make arrangements for the guests.

**Problem:** Find factors that influence booking cancellations, build a predictive model that can predict cancellations in advance, formulate profitable policies for cancellations and refunds.

The notebook is divided into different sections:
* Data Dictionary
* Import Libraries
* Data Loading and Initital Summary Statistics
* Exploratory Data Analysis
* Data Preparation for Modeling
* Model Evaluation Criterion
* Model Building
* Summary

## Summary
I have tried multiple models (Support Vector Machins, Decision Trees, Random Forest) and able to identify key factors that affect the booking_status (cancel or not cancel) of customers booking hotel rooms:
* lead_time
* avg_price_per_room
* no_of_special_requests
> These 3 factors are similar between the Decision Trees and Random Forest Models.

The **tuned decision tree with F1-score accuracy of 85% and 84% for training and test dataset**, respectively, reveals to be the best model to fit our key objective which is the following: "The hotel would want the F1 Score to be maximized, the greater the F1 score, the higher the chances of minimizing False Negatives and False Positives." This model can be used to predict whether a certain booking will get cancelled or not.

## Business Recommendations
Here are 4 key business recommendations based on the findings of this project:

1. I can see that lead_time is the most important factor to deciding whether a customer will cancel the booking or not. The business could follow-up or confirm early with these customers when they make the bookings whether they would want to keep the bookings. A regular follow-up nearer the actual booking date is recommended.
2. It is found that repeat customers has a lower chance of cancelling. Keep these customers happy and satisfied with the whole booking experience and stay to ensure reduction of booking cancellations.
3. With relation to the 2nd recommendation, I'd recommend to include better promotions in the future for customer who booked and didn't cancel since these will be the repeat customers for the business. Build a better database of new potential customers.
4. Promote the idea of customers' ability to customize their booking with special requests. This will make their booking experience personalized and stand out compared to competitors.

## Future Improvements
This project assessment involves breaking down the analysis thru a series of questions. To further improve on this notebook, I should do the following:
* Extract other features that could potentially be used for the predictive model
* Try out other model types for building the predictive model to further improve model accuracy
