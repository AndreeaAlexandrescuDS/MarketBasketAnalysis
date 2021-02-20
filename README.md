# MarketBasketAnalysis
MBA with PySpark


## Theory of Apriori Algorithm
- https://en.wikipedia.org/wiki/Association_rule_learning
- https://en.wikipedia.org/wiki/Apriori_algorithm
- https://pypi.org/project/apyori/
- https://spark.apache.org/docs/2.2.0/ml-frequent-pattern-mining.html
<br>

There are three major components of the Apriori algorithm:
- Support
- Confidence
- Lift
<br>

## 1) Support
<br>
Support refers to the popularity of an item and can be calculated by finding the number of transactions containing a particular item divided by the total number of transactions
<br>

## 2) Confidence
<br>
Confidence refers to the likelihood that an item B is also bought if item A is bought.
<br>

## 3) Lift
<br>
Lift refers to the increase in the ratio of the sale of B when A is sold.
<br>

## Association rule by Lift

- lift = 1 → There is no association between A and B.
- lift < 1→ A and B are unlikely to be bought together.
- lift > 1 → greater the lift, greater the likelihood of buying both products together.

## Steps Involved in Apriori Algorithm
<br>
The Apriori algorithm tries to extract rules for each possible combination of items.
<br>
For larger dataset, this computation can make the process extremely slow.
<br>
To speed up the process, we need to perform the following steps:

 - Set a minimum value for support and confidence. This means that we are only interested in finding rules for the items that have certain default existence (e.g. support) and have a minimum value for co-occurrence with other items (e.g. confidence).
 - Extract all the subsets having a higher value of support than a minimum threshold.
 - Select all the rules from the subsets with confidence value higher than the minimum threshold.
 - Order the rules by descending order of Lift.
