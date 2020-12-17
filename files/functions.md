### Functions

> Code တချို့ကို ထပ်ခါထပ်ခါ မသုံးရအောင် လုပ်တဲ့နေရာမှာ သုံးတယ်

> Python မှာ build-in ပါတဲ့ ```print```, ```input```, ```type```, ... အစရှိတဲ့ functions များရှိပါတယ်

> Function တွေကို ခေါ်မသုံးခင် ကြေငြာထားရပါတယ်

##### Example 1 (Creating function)
```python
def sayHello():
	print("Hello World")

sayHello()
sayHello()
```
###### Output :
```
Hello World
Hello World
```
##### Example 2 (Function Arguments)
> Data တချို့ကို ယူသုံးချင်တဲ့ အခါ function ထဲကို Arguments အဖြစ်ထည့်ပေးရပါတယ်

```python
def sayMyName(name):
	print("Hello",name)

sayMyName("Kyaw Gyi")
sayMyName("Pu Lone")
```
###### Output :
```
Hello Kyaw Gyi
Hello Pu Lone
```

> Arguments လိုအပ်တဲ့ function တစ်ခုကို Arguments မပါပဲ ခေါ်သုံးခဲ့ရင် Error တက်ပါတယ်

##### Example 3 (No Arguments (Error))
```python
def sayMyName(name):
	print("Hello",name)
# Don't do it (Error)
sayMyName()
```
###### Output :
```
Traceback (most recent call last):
  File "test.py", line 5, in <module>
    sayMyName()
TypeError: sayMyName() missing 1 required positional argument: 'name'
```
> အဲ့လို error မတက်ချင်ရင် function ရဲ့ Arguments နေရာမှာ assign လုပ်ထားလို့ရပါတယ်

##### Example 4 (Making Default Arguments)
```python
def sayMyName(name="Unknown"):
	print("Hello",name)

sayMyName("Mg Mg")
sayMyName()
```
###### Output :
```
Hello Mg Mg
Hello Unknown
```

##### Example 5 (Arguments)
```python
def sumMe(a,b):
	print(a+b)

sumMe(3,5)
```
###### Output :
```
8
```

##### Example 6 (Multiple Arguments)
```python
def favColors(*colors):
	print("My Fav Colors are", colors)

favColors("red","green","blue")
```
###### Output : 
```
My Fav Colors are ('red', 'green', 'blue')
```

##### Example 7 (Keyword Arguments)
```python
def sayMyName(first, second):
	print(first,second)

sayMyName(second="Owl", first="Logix")
```
###### Output :
```
Logix Owl
```

##### Example 8 (Arbitrary Keyword Arguments)
```python
def printPerson(**person):
	print("Name:",person["name"])
	print("age:",person["age"])

printPerson(name="Su Su", age=21)
```
###### Output:
```
Name: Su Su
age: 21
```

##### Example 9 (return)
```python
def isEven(num):
	return num%2==0

print(isEven(3))
print(isEven(4))
```
###### Output:
```
False
True
```

##### Example 10 (return)
> Get the random integer between 1 and 10 (including)
```python
import random

def giveMeRandom(low, high):
	return random.randint(low,high)

print(giveMeRandom(1,10))
```
###### Output:
```
8
```

##### Example 11 (Recusive Function)
##### Factorial Program (Recursive Version)

```python
def factorial(num):
	if num==1:
		return 1
	else:
		return num*factorial(num-1)

print(factorial(5))
```
###### Output:
```
120
```

##### Example 13 : count()

> Format : ```string.count(value, start, end)```

> value = count လုပ်ချင်တဲ့ value

> start = စမယ့် အခန်းနံပါတ်

> end = ဆုံးမယ့် အခန်းနံပါတ်

```python
mytext = 'hi everyone, hi ladies, hi gentleman'

print(mytext.count('hi'))
print(mytext.count('hi',2))
print(mytext.count('hi',2,15))
```
###### Output:
```
3
2
1
```

##### Example 14 : join()

> Format : ```string.join(iterable)```

> iterable ဆိုတာက string return ပြန်ပေးတဲ့ ဘယ် object မဆို ထည့်လို့ရတယ်။ (required)

```python
mytext = "Hello LogixOwl"
print(':'.join(mytext))

mylist = ['red','green','blue']
print('#'.join(mylist))

mydict = {'name':'mgmg', 'sex':'male'}
print('&'.join(mydict))
```
###### Output:
```
H:e:l:l:o: :L:o:g:i:x:O:w:l
red#green#blue
name&sex
```

##### Example 15 : find()

> Format : ```string.find(value, start, end)```

| A |   | q | u | i | c | k |   | b | r | o | w | n |   | f | o | x |   | j | u | m | p | s |   | o | v | e | r |   | t | h | e |   | l | a | z | y |   | d | o | g | . |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26 | 27 | 28 | 29 | 30 | 31 | 32 | 33 | 34 | 35 | 36 | 37 | 38 | 39 | 40 | 41 |

```python
text = 'A quick brown fox jumps over the lazy dog.'

print(text.find('over'))

print(text.find('u'))
print(text.find('u',4))
print(text.find('o',12,30))
```
###### Output:
```
24
3
19
15
```

<hr>

**String methods**

| Method | Description |
| --- | --- |
| capitalize() | Converts the first character to upper case |
| casefold() | Converts string into lower case |
| center() | Returns a centered string |
| count() | Returns the number of times a specified value occurs in a string |
| encode() | Returns an encoded version of the string |
| endswith() | Returns true if the string ends with the specified value |
| expandtabs() | Sets the tab size of the string |
| find() | Searches the string for a specified value and returns the position of where it was found |
| format() | Formats specified values in a string |
| format_map() | Formats specified values in a string |
| index() | Searches the string for a specified value and returns the position of where it was found |
| isalnum() | Returns True if all characters in the string are alphanumeric |
| isalpha() | Returns True if all characters in the string are in the alphabet |
| isdecimal() | Returns True if all characters in the string are decimals |
| isdigit() | Returns True if all characters in the string are digits |
| isidentifier() | Returns True if the string is an identifier |
| islower() | Returns True if all characters in the string are lower case |
| isnumeric() | Returns True if all characters in the string are numeric |
| isprintable() | Returns True if all characters in the string are printable |
| isspace() | Returns True if all characters in the string are whitespaces |
| istitle()  | Returns True if the string follows the rules of a title |
| isupper() | Returns True if all characters in the string are upper case |
| join() | Joins the elements of an iterable to the end of the string |
| ljust() | Returns a left justified version of the string |
| lower() | Converts a string into lower case |
| lstrip() | Returns a left trim version of the string |
| maketrans() | Returns a translation table to be used in translations |
| partition() | Returns a tuple where the string is parted into three parts |
| replace() | Returns a string where a specified value is replaced with a specified value |
| rfind() | Searches the string for a specified value and returns the last position of where it was found |
| rindex() | Searches the string for a specified value and returns the last position of where it was found |
| rjust() | Returns a right justified version of the string |
| rpartition() | Returns a tuple where the string is parted into three parts |
| rsplit() | Splits the string at the specified separator, and returns a list |
| rstrip() | Returns a right trim version of the string |
| split() | Splits the string at the specified separator, and returns a list |
| splitlines() | Splits the string at line breaks and returns a list |
| startswith() | Returns true if the string starts with the specified value |
| strip() | Returns a trimmed version of the string |
| swapcase() | Swaps cases, lower case becomes upper case and vice versa |
| title() | Converts the first character of each word to upper case |
| translate() | Returns a translated string |
| upper() | Converts a string into upper case |
| zfill() | Fills the string with a specified number of 0 values at the beginning |

*Reference from [W3School](https://www.w3schools.com/python/python_strings.asp)*

[Next (Operators)](./operators.md)