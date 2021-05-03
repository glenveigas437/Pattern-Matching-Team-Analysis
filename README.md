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

<h2>Steps Involved in building this system</h2>

<h3>Step 1: Calculating the goal contribution frequency of each player</h3> 

![Frequeny of Goal Contribution of each player](https://user-images.githubusercontent.com/31877827/116843523-d2676880-abfd-11eb-8e3e-d4839d0dbc4c.png)


<h3>Step 2: Calculating the Support for each player</h3>

Formula to calculate Support: <h3>Support = (Goal Contribution Frequency of the player(P)/Total Goals scored by the entire team(T)) * 100</h3>

![Support of each Player](https://user-images.githubusercontent.com/31877827/116846588-3726c100-ac06-11eb-8fc8-822e8a2a0f34.png)


<h3>Step 3: Setting Minimum Support and confidence</h3>
 For this I have set the minimum support as 5
 
 <h3>Step 4: Filtering Players with minimum Support Threshold</h3>

![Players with atleast 5% contribution](https://user-images.githubusercontent.com/31877827/116846786-c502ac00-ac06-11eb-8192-2f957cf24c14.png)

<h3>Step 5: Checking Combination Support For 2 Players</h3>
So, this step determines the contribution of a patnership
There might be cases where Player(X) has assisted Player(Y) 10 times and Player(Y) has assisted Player(X) 5 times so the unideirectional support will be different compared to the holistic support of these combinations

![Player Partnership Support](https://user-images.githubusercontent.com/31877827/116847117-83becc00-ac07-11eb-98ad-e97aade850f5.png)

After filtering
![Duos with atleast 5% contribution towards goals](https://user-images.githubusercontent.com/31877827/116847204-b36dd400-ac07-11eb-946f-7a5380df3959.png)

<h3>Step 6: Finding Confidence</h3>
Confidence is the measure of how much impact the first player has on the partnership

Formula for Confidence: <h4>Confidence: = (Support of Duo(A1, A2)/Support of Player(A1))*100

I have set the confidence to be 10

![image](https://user-images.githubusercontent.com/31877827/116847583-735b2100-ac08-11eb-8817-0a334b523d1a.png)

<h3>Inference</h3>

![Key Passes](https://user-images.githubusercontent.com/31877827/116847666-9d144800-ac08-11eb-9db6-06369378bf37.png)

![Build Play Passes + Assists + Goals](https://user-images.githubusercontent.com/31877827/116847693-b1584500-ac08-11eb-9440-68175f515ff0.png)


So, these are the key players the opposition should focus on, evidently Bruno Fernandes and Marcus Rashford have had a huge impact on the game this season so has Luke Shaw in terms of improving his stats with respect to attack and defence both but you can see that being a defender he has been one of the key players for Manchester United this season, and hugely contributed towards build up plays resulting into goals.


The first Update was made on 2nd May 2021 on the eve of Gameweek 34 where Manchester United would host Liverpool, I'll be updating the same as the season progresses and reaches matchweek 38.






