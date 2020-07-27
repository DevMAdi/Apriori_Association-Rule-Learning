**check these out later:**

https://medium.com/machine-learning-researcher/association-rule-apriori-and-eclat-algorithm-4e963fa972a4
https://medium.com/@deepak.r.poojari/apriori-algorithm-in-python-recommendation-engine-5ba89bd1a6da

Some people who buy something also buy something
even though those product may not be at all connected

eg. People who buy diaper also buy beer.(both product not connected) or such as bread & milk

Association Rule Mining - Apriori Algorithm-> rule-based machine learning method for discovering relations between variables in large databases
This way shops can separate both product at large distance so people have to travel entire shops & may also buy something else.
or can stock them close for cust. convenience, depends on shops

//eg. Screenshot (2721/22)

How Apriori Algo. works?
-> It has 3 parts- **Support, Confidence, Lift**

## **Step1:	Apriori- Support**

**Support(M)** = user watch lists containing M/ # user watchlists

Taking eg. 1) check Screenshot (2724)- 100 people(20 people X 5 rows)
 among these, 10 people have seen exmachina movie. out of 100 people
				Thus **Support** = 10/100= 10%

## Step2:	Apriori- Confidence

**Confidence(M1->M2)=** # user watchlists contaning M1 & M2/ # user watchlists contaning M1

Taking eg. 1)People who've seen interstellar are also likely to have seen exmachina.
here M1- interstellar(everyone have seen)
	 M2- exmachina(seen M1, how many seen this one)
// see Screenshot (2725)- 40 people like interstellar & among those 7 watched exmachina
			Thus **Confidence**= 7/40 = 17.5%

## Step3:	Apriori- Lift

**Lift(M1->M2)=** Confidence(M1->M2) / Support(M2)

// see Screenshot (2726)
-> now suppose if we have entire new population
	random person selected & we suggest exmachina to him
	likelihood they will like exmachina: 10%
	(since in original population, originally 10 people liked out of 100)
Que. Can we improve this?

-> In this new population, suggest exmachina only to those people who
	have alrdy seen intersterlar.
	i.e ask if they seen intersterlar. Yes- suggest exmachina then
	likelihood they will like exmachina: 17.5%
	(since in original population, originally 7 people liked out of 40)

Thus Lift => improvement in prediction
	i.e randomly suggest someone movie vs suggest if they lardy watch one other particular movie.

Thus Lift= (17.5%)/ (10%) = 1.75
improvement of 1.75

Steps: 	Screenshot (2727)
