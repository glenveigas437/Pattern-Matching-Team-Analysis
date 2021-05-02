# Pattern-Matching-Team-Analysis
Analysis of player contribution towards goals scored for Manchester United in 2020-21 Premier League Season Using Apriori Pattern Matching Algorithm

Before You dive deep into knowing the analysis I have done with regards to player contribution towards goals scored by players of Manchester United F.C. here's a little bit you need to know about [Apriori Algorithm and Pattern Matching Analysis](https://towardsdatascience.com/apriori-association-rule-mining-explanation-and-python-implementation-290b42afdfc6)

Apriori Algorithm is basically used to find the association in between 2 items, a famous manifestation of this algorithm is [Market Basket Analysis](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.402.8724&rep=rep1&type=pdf).

<h3>How did I use Patten Matching in Football Analytics?</h3>

Dataset: The [Goals.csv](https://github.com/glenveigas437/Pattern-Matching-Team-Analysis/blob/main/Goals.csv) file contains Goal contributors ranging upto 5 touches max for a goal.

![Goals.csv Snippet](https://user-images.githubusercontent.com/31877827/116814101-b9ff3b80-ab74-11eb-9722-3f03b57941a0.png)

Itemizing Goals.csv: 
  * if there is just one player in the row, then the goal scored was not a team effort
  * The penultimate name in the row is of the assist provider
  * The last name in the row is of the goal scorer


 




