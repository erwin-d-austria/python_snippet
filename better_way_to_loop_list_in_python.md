Author: e.d.austria
Date: 11/27/18
Version: 1.0
Link:(https://github.com/erwin-d-austria/python_snippet)

# Better way to loop a list using Python

Before, this is my way to loop a list.
``` python
def FahrenheitToCelsisus(temp):
	return (temp-32) * 5/9

ctemps = [0, 12, 34, 100]

my_list = []
for x in ctemps:
	my_list.append(FahrenheitToCelsisus(x))
	
print(my_list)
```
Now, i found out that there is a best way of looping list
```python
def FahrenheitToCelsisus(temp):
	return (temp-32) * 5/9

ctemps = [0, 12, 34, 100]

print(list(map(FahrenheitToCelsisus, ctemps)))
```
Then i noticed that there is a better way.
``` python
ctemps = [0, 12, 34, 100]

print(list(map(lambda t: (t-32) * 5/9, ctemps)))
```

