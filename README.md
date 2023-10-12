# Classifying Low Customer-traffic Holidays to Assist in Business Closure Decisions
![image]()

## Background
Oregon Company (OC) owns and operates two major retail locations in the Portland metro area.  Those locations are open to customers 363 days per year, observing only the Christmas and New Year's Day holidays.  This level of operation is difficult in the current labor market, and OC management seeks to find other candidate holidays for closure in order to reduce operating costs while minimizing impacts on customers.

## Objective
This analysis seeks to analyze OC sales data ("traffic") on public holidays, and develop a machine learning model that can accurately profile upcoming holidays and predict their likelihood of seeing relatively lower customer traffic.  The goal is to save OC operations costs while having least impact possible on OC customers.  

## Methods
The analysis is conducted in the following steps.

### Data Extraction and Prep
The analysis relies on three distinct sources of data, each of which are obtained and prepped per [this notebook](https://app.hex.tech/5b266aaf-b343-4ae7-bdea-218e8fe3001f/app/bc7ccc2f-6461-401a-8fca-933c36943bd7/latest).

### Data Analysis
OC's questions heading into the analysis were as follows:

1. Which holidays (other than New Year's and Christmas) exhibit the lowest daily customer traffic, and is this robust across locations and customer types?

2. How does daily traffic for each holiday above compare with a similarly-situated, non-holiday business day?

3. What features of the day contribute to a holiday having relatively lower/higher sales than it's non-holiday counterpart?
   
[This notebook](https://app.hex.tech/5b266aaf-b343-4ae7-bdea-218e8fe3001f/app/d735a3e8-64d4-46bc-a28c-8fac3a2de39e/latest) systematically answers these questions.

### Machine Learning
Experiments were conducted to train and evaluate a binary classifier for use in profiling upcoming holidays. [This notebook](https://app.hex.tech/5b266aaf-b343-4ae7-bdea-218e8fe3001f/app/60b5079d-cdcc-4710-bf25-951338254a99/latest) details the model pre-processing, training and evaluation process.  The deployed profiling and classfication app is available [here](https://app.hex.tech/5b266aaf-b343-4ae7-bdea-218e8fe3001f/app/b3b7308c-6ef7-4470-8cc6-a238b8561864/latest).

## Results
The best classifier was a random forest, which was found to have high level of accuracy (.79), recall (.85) and precision (.86) on the unseen test set. The results suggest that Thanksgiving Day, Memorial Day, and July 4th all represent good candidate holidays for closure in the upcoming year, and management can rely on the app to quickly profile holidays as needed. [This presentation](https://www.beautiful.ai/player/-NgZMa9kUW4dmfGvzJxd) provides a summary of the analysis.

## Value Proposition
OC management needs to reduce operations costs while minimizing customer impact.  In addition to their current closures on Christmas and New Year's, OC can be confident that the deployed model will yield accurate predictions of lower sales holidays over the next year.  These predictions will help the company reduce costs and minimize impact on their customers.  In addition, the model's lead time of 1 full year gives OC communications staff plenty of time to alert customers of the next year's holiday closure, if warranted.  