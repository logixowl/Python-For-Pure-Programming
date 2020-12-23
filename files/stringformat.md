### String Output Formatting

##### Example 1
```python
mytext = "Hello {}, I'm {}"
print(mytext.format("everyone","LogixOwl"))
```
###### Output
```
Hello everyone, I'm LogixOwl
```


##### Example 2
```python
print("Hello {0}, I'm {1}".format("everyone","LogixOwl"))
```
###### Output
```
Hello everyone, I'm LogixOwl
```


##### Example 3
```python
print("Hello {1}, I'm {0}".format("everyone","LogixOwl"))
```
###### Output
```
Hello LogixOwl, I'm everyone
```


##### Example 4
```python
text = "Name\t: {0}\nPrice\t: {1}\nRate\t: {rating}%"
print(text.format('Apple',350,rating=99.8))
```
###### Output
```
Name    : Apple
Price   : 350
Rate    : 99.8%
```


##### Example 5
```python
text = 'This is floating {:.3f} with 3 decimal place'
print(text.format(3.14286))
```
###### Output
```
This is floating 3.143 with 3 decimal place
```


##### Example 6
```python
text = '''Hey {0}!
Do you know {1}?
{1} is so cool!'''

print(text.format('Everyone','LogixOwl'))
```
###### Output
```
Hey Everyone!
Do you know LogixOwl?
LogixOwl is so cool!
```


##### Example 7
```python
# left align
print("I {:<10} you".format('love'))
# right align
print("I {:>10} you".format('love'))
# center
print("I {:^10} you".format('love'))
```
###### Output
```
I love       you
I       love you
I    love    you
```


##### Example 8
```python
print("Price {:=10} Kyats".format(-1500))
```
###### Output
```
Price -     1500 Kyats
```


##### Example 9
```python
print("Two integers: {0:+} and {1:+}".format(-5,7))
```
###### Output
```
Two integers: -5 and +7
```


##### Example 10
```python
print("Population of our country is {:,}".format(53710000))
print("Population of our country is {:_}".format(53710000))
```
###### Output
```
Population of our country is 53,710,000
Population of our country is 53_710_000
```


##### Example 11
```python
text = """Binary value of {0} is {0:b}
Oct value of {0} is {0:o}
Hex value of {0} is {0:x}"""

print(text.format(43))
```
###### Output
```
Binary value of 43 is 101011
Oct value of 43 is 53
Hex value of 43 is 2b
```



##### Example 12
```python
print("you correct {:.1%} of the question".format(0.9))
```
###### Output
```
you correct 90.0% of the question
```

