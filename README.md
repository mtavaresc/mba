# Market Basket Analysis with Apriori Algorith
---
# Association Rule Learning (ARL)
In today's world where the number of customers and transactions are increasing, it has become more valuable to create meaningful results from data and for developing marketing strategies. Revealing hidden patterns in the data in order to be able to compete better and maximize profit in the face of intense competition in the market, and to establish value-oriented long-term relationships with customers, makes a great contribution to determining marketing strategies.

However, the development of rule-based strategies is no longer possible in big data world, offering the right product to the right customer at the right time; it forms the basis of cross-selling and loyalty programs within the scope of customer retention and increasing lifetime value. Therefore, it has been crucial point for companies making product offers by using these patterns of association and developing effective marketing strategies Market Basket analysis is one of the association rule applications. It allows us to predict the products that customers tend to buy in the future by developing a pattern from their past behavior and habits.

There are different algorithms to be used for Association Rules Learning. One of them is the Apriori algorithm. In this project, product association analysis will be handled with “Apriori Algorithm” and the most suitable product offers will be made for the customer who is in the sales process, using the sales data of an e-commerce company.

## What is Association Rule Learning?
Association Rule Learning is rule-based learning for identifying the association between different variables in a database. `One of the best and most popular examples of Association Rule Learning is the Market Basket Analysis`. The problem analyses the association between various items that has the highest probability of being bought together by a customer.

For example, the association rule, {onions, chicken masala} => {chicken} says that a person who has got both onions and chicken masala in his or her basket has a high probability of buying chicken also.

## Apriori Algorithm
The algorithm was first proposed in 1994 by Rakesh Agrawal and Ramakrishnan Srikant. Apriori algorithm finds the most frequent itemsets or elements in a transaction database and identifies association rules between the items just like the above-mentioned example.

## How Apriori works?
To construct association rules between elements or items, the algorithm considers 3 important factors which are, support, confidence and lift. Each of these factors is explained as follows:

### Support:  
The support of item I is defined as the ratio between the number of transactions containing the item I by the total number of transactions expressed as:

![support](https://miro.medium.com/v2/resize:fit:403/0*pyOADkeaWyrVP2ft.png)

**Support** indicates how popular an itemset is, as measured by the proportion of transactions in which an itemset appears. In Table 1 below, the support of {apple} is 4 out of 8, or 50%. Itemsets can also contain multiple items. For instance, the support of {apple, beer, rice} is 2 out of 8, or 25%.

![support-example](https://annalyzin.files.wordpress.com/2016/04/association-rule-support-table.png?w=503&h=447)

*If you discover that sales of items beyond a certain proportion tend to have a significant impact on your profits, you might consider using that proportion as your support threshold. You may then identify itemsets with support values above this threshold as significant itemsets.*

### Confidence:
This is measured by the proportion of transactions with item I1, in which item I2 also appears. The confidence between two items I1 and I2, in a transaction is defined as the total number of transactions containing both items I1 and I2 divided by the total number of transactions containing I1. ( Assume I1 as X , I2 as Y )

![confidence](https://miro.medium.com/max/576/1*50GI4dR58MnhwBP9dw6nFQ.png)

**Confidence** says how likely item Y is purchased when item X is purchased, expressed as {X -> Y}. This is measured by the proportion of transactions with item X, in which item Y also appears. In Table 1, the confidence of {apple -> beer} is 3 out of 4, or 75%.

![confidence-example](https://annalyzin.files.wordpress.com/2016/03/association-rule-confidence-eqn.png?w=527&h=77)

*One drawback of the confidence measure is that it might misrepresent the importance of an association. This is because it only accounts for how popular apples are, but not beers. If beers are also very popular in general, there will be a higher chance that a transaction containing apples will also contain beers, thus inflating the confidence measure. To account for the base popularity of both constituent items, we use a third measure called lift.*

### Lift:
Lift is the ratio between the confidence and support.

**Lift** says how likely item Y is purchased when item X is purchased, while controlling for how popular item Y is. In Table 1, the lift of {apple -> beer} is 1,which implies no association between items. A lift value greater than 1 means that item Y is likely to be bought if item X is bought, while a value less than 1 means that item Y is unlikely to be bought if item X is bought.
( here X represents apple and Y represents beer )

![lift-example](https://annalyzin.files.wordpress.com/2016/03/association-rule-lift-eqn.png?w=566&h=80)



[^note]:
for **Extra Reading**: [refer this](https://towardsdatascience.com/association-rules-2-aa9a77241654)