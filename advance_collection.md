Author: e.d.austria
Date: 11/27/18
Version: 1.0
Link:(https://github.com/erwin-d-austria/python_snippet)

# Advance Collection in Python

A collection is similar to a basket that you can add and remove items from. 

## OrderedDict
``` python
from collections import defaultdict
	
fruits = ['apple', 'banana', 'pear', 'orange', 'banana']

fruitCounter = defaultdict(int)
for fruit in fruits:
	fruitCounter[fruit] += 1

print(fruitCounter)
```
## Counter
``` python
from collections import Counter

class1 = ['Bob', 'Becky', 'Chad', 'Darcy', 'Frank', 'Hannah',
    		'Kevin', 'James', 'James', 'Melanie', 'Penny', 'Steve']

class2 = ['Bill', 'Barry', 'Cindy', 'Debbie', 'Frank',
		'Gabby', 'Kelly', 'James', 'Joe', 'Sam', 'Tara', 'Ziggy']

# TODO: Create a Counter for class1 and class2
c1 = Counter(class1)
c2 = Counter(class2)

# TODO: How many students are in class 1?
print(sum(c1.values()), "student in class 1")
# TODO: Combine the two classes
c1.update(class2)
# TODO: What's the most common name in the two classes?
print(c1.most_common(3))
# TODO: Separate the classes again
c1.subtract(class2)
# TODO: What common between the two classes?
print(c1 & c2)
```

## OrderDict
``` python
from collections import OrderedDict

sportTeams = [("Royals", (18, 12)), ("Rockets", (24, 6)),
			("Cardinal", (20, 10)), ("Dragons", (22, 8)),
			("Kings", (15, 15)), ("Chargers", (20, 10)),
			("Jets", (16, 14)), ("Warriors", (25, 5))]
# sort the teams by number of wins
sortedTeams = sorted(sportTeams, key=lambda t: t[1][0], reverse=True)

# TODO: create an odered dictionary of the teams
teams = OrderedDict(sortedTeams)
print(teams)

# TODO: Use popitem to remove the top item
tm, wl = teams.popitem(False)
print("Top team: ", tm, wl)

# TODO: test for equality
a = OrderedDict({"a" : 1, "b" : 2, "c" : 3})
b = OrderedDict({"a" : 1, "c" : 3, "b" : 2})
print("Equality test: ", a == b)
```