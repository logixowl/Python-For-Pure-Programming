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

#### Global, Local variable

> Global Variable ဆိုတာ Program တစ်ခုအတွင်းမှာရှိတဲ့ function အပြင်မှာရော function အတွင်းမှာပါ အသုံးပြုနိုင်တဲ့ variable ဖြစ်ပါတယ်

> Local Variable ဆိုတာ Function တစ်ခုအတွင်းမှာသာ သုံးလို့ ရတာကို ခေါ်ပါတယ်

##### Example 12 : create a global variable
```python
a = 45

def myfunc():
	print('I am number', a)

myfunc()
```
###### Output:
```
I am number 45
```

> ဒါပေမယ့် Example 12 က variable ```a``` ကို ပြင်လို့မရပါဘူး ပြင်ရင် အောက်ပါ အတိုင်း Error တက်ပါလိမ့်မယ်

##### Example 13 (change global variable (Error))
```python
a = 45

def myfunc():
	a = a * 2
	print('I am number',a)

myfunc()
```
###### Output:
```
Traceback (most recent call last):
  File "test.py", line 8, in <module>
    myfunc()
  File "test.py", line 5, in myfunc
    a = a * 2
UnboundLocalError: local variable 'a' referenced before assignment
```

> Global variable ကို ပြင်ပြီးသုံးလို့ရအောင် ```global``` ဆိုတဲ့ keyword နဲ့ ကြေငြာပေးရပါတယ်

##### Example 14 (global keyword)
```python
a = 45

def myfunc():
	global a
	a = a * 2
	print('I am number',a)

myfunc()
```
###### Output:
```
I am number 90
```

##### Example 15 (create local variable)
```python
def myfunc():
	name = "LogixOwl"
	print("local:",name)

myfunc()
# print("global:",name) #will make error
```
###### Output:
```
local: LogixOwl
```

##### Example 16 (local & global variables 1)
```python
name = 'Unknown'

def myfunc():
	name = 'LogixOwl'
	print('Local:', name)

myfunc()
print('Global:', name)
```
###### Output:
```
Local: LogixOwl
Global: Unknown
```

##### Example 17 (local & global variables 2)
```python
name = 'Unknown'

def myfunc():
	global name #added
	name = 'LogixOwl'
	print('Local:', name)

myfunc()
print('Global:', name)
```
###### Output:
```
Local: LogixOwl
Global: LogixOwl
```

### Creating Own Module

> ```Module``` တစ်ခုဆောက်ဖို့အတွက် python file အရင် ဆောက်ရပါမယ် ```logixowl.py```

> create လုပ်ထားတဲ့ python file နဲ့ အသုံးပြုမယ့် main file သည် path လမ်းကြောင်းတစ်ခုထဲ(folder တစ်ခုထဲ) အတွင်းမှာ ရှိရပါမယ်

> **```logixowl.py```**
```python
def isEven(num):
	return num%2==0

def factorial(num):
	fact = 1
	for i in range(1,num+1):
		fact*=i
	return fact
```

> **```test.py```**
```python
import logixowl

print(logixowl.isEven(10))
print(logixowl.isEven(11))

print(logixowl.factorial(5))
print(logixowl.factorial(4))
```
###### Output (run test.py)
```
True
False
120
24
```

> ```import``` ကို ဒီလိုလဲ လုပ်လို့ရပါသေးတယ် output က တူတဲ့အတွက် output ကို မပြတော့ပါဘူး

##### test2.py
```python
import logixowl as owl

print(owl.isEven(10))
print(owl.isEven(11))

print(owl.factorial(5))
print(owl.factorial(4))
```

##### test3.py
```python
from logixowl import *

print(isEven(10))
print(isEven(11))

print(factorial(5))
print(factorial(4))
```