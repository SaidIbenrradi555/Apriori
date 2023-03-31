RL
K-means
CAH 
Arbre de décision



<h1>The Apriori Algorithm</h1>


The Apriori algorithm is a classic algorithm used to mine frequent itemsets in a dataset. The algorithm works by generating candidate itemsets of increasing size, and pruning those that do not meet a minimum support threshold. The algorithm uses a level-wise approach, where it first generates all frequent itemsets of size 1, then uses those to generate frequent itemsets of size 2, and so on.


#### Working of the Apriori Algorithm

The Apriori algorithm works in the following way:

1 Generate frequent itemsets of size 1 by scanning the database and counting the support of each item.

2 Repeat until no new frequent itemsets can be generated:<br>
  &emsp; a. Generate candidate itemsets by joining frequent itemsets of the previous level.<br>
  &emsp;  b. Prune candidate itemsets that do not meet the minimum support threshold.<br>
  &emsp;  c. Count the support of each candidate itemset.<br>

3 Generate association rules from the frequent itemsets.



### Basic concepts of Apriori algorithm



`Support`: It refers to the frequency of occurrence of an itemset in a dataset. It is calculated as the number of transactions containing the itemset divided by the total number of transactions.

$\text{support}(X) = \frac{\text{number of transactions containing }X}{\text{total number of transactions}}$.

`Confidence`: It measures how often the rule is found to be true. It is calculated as the number of transactions containing both the antecedent and consequent divided by the number of transactions containing only the antecedent.<br><br>
$\text{confidence}(X \rightarrow Y) = \frac{\text{support}(X \cup Y)}{\text{support}(X)}$.<br><br>

`Lift`: It measures the strength of the association between the antecedent and the consequent. A lift value greater than 1 indicates that the antecedent and consequent are positively correlated, while a value less than 1 indicates a negative correlation.<br>


$\text{lift}(X \rightarrow Y) = \frac{\text{support}(X \cup Y)}{\text{support}(X) \times \text{support}(Y)}$.<br><br>
`Frequent itemsets`: Itemsets that occur frequently in the dataset above a minimum support threshold.

`Association rules`: Rules that express a relationship between two itemsets, where the presence of one itemset implies the presence of the other. They consist of an antecedent (if) and a consequent (then) part.

