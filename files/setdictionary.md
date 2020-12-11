### Set & Dictionary

### Set

ထည့်လိုက်တဲ့ items တွေက

* unindex ဖြစ်ပါတယ်။ (list, tuple တို့လို index(အခန်း) နဲ့ ထုတ်လို့ မရပါ)
* unorder ဖြစ်ပါတယ်။ (items တွေက အစဥ်လိုက်ဝင်သွားတာမဟုတ်ပါဘူး။)
* Unique value ဖြစ်ရပါတယ်။ (တူနေတဲ့ items တွေကို တစ်ခုတည်းယူပါတယ်)

#### Declaration

##### Example 1
```python
myset = {"red","green","blue"}
print(myset)
```
###### Output:
```
{'red', 'green', 'blue'}
```

##### Example 2
```python
mylist = ['red','green','blue']
myset = set(mylist)
print(myset)
```
###### Output:
```
{'green', 'red', 'blue'}
```

> List, Tuple နဲ့ မတူတဲ့ နောက်တစ်ချက်က Set ကို empty set ဆောက်တဲ့အခါမှာ ```myset = {}``` ဆိုရင် ```error``` တက်ပါတယ်

> ```myset = set()``` လို့ဆောက်ရပါတယ်

##### Example 3
```python
myset = set()
myset.add(40)
myset.add(99)
print(myset)
```
###### Output:
```
{40, 99}
```

> Set မှာ item တွေထည့်ပြီးရင် change လို့ မရတော့ပါဘူး

##### Example 4 (access items)
```python
colorSet = {'red','green','blue','black','white'}

for color in colorSet:
	print('This is',color)
```
###### Output:
```
This is white
This is green
This is red
This is black
This is blue
```

> တခြားသော Iterable items တွေကို အကုန်ထည့်ချင်တဲ့ အခါမှာ ```set.update(iterable)``` ကိုသုံးပါတယ်။

##### Example 5 (update)
```python
abc = {'a','b','c'}
xyz = ['x','y','z']
abc.update(xyz)

print(abc)
```
###### Output:
```
{'c', 'a', 'y', 'b', 'x', 'z'}
```

##### Example 6 (removing)
```python
alphabet = set("abcdefg")
print("Original set:")
print(alphabet)
print()

alphabet.remove('e')
print("Removed 'e':")
print(alphabet)
print()

alphabet.discard('a')
print("Discarded 'a':")
print(alphabet)
print()

print("Popped unknown item '",alphabet.pop(),"':")
print(alphabet)
print()

alphabet.clear()
print("Cleared:")
print(alphabet)
print()

del alphabet
print("Deleted variable alphabet:")
print(alphabet)
#error will occur
print()
```
###### Output:
```
Original set:
{'g', 'c', 'a', 'f', 'd', 'b', 'e'}

Removed 'e':
{'g', 'c', 'a', 'f', 'd', 'b'}

Discarded 'a':
{'g', 'c', 'f', 'd', 'b'}

Popped unknown item ' g ':
{'c', 'f', 'd', 'b'}

Cleared:
set()

Deleted variable alphabet:
Traceback (most recent call last):
  File "test.py", line 27, in <module>
    print(alphabet)
NameError: name 'alphabet' is not defined
```

> ```set.remove()``` နဲ့ ```set.discard()``` အဓိက ကွာခြားတာကတော့ remove က ဖျက်လိုတဲ့ item က set ထဲမှာမရှိရင် error တက်ပြီး discard ကတော့ မတက်ပါဘူး

> ```set.pop()``` က list, tuple တို့နဲ့ မတူတာက set သည် unindex ဖြစ်တဲ့ အတွက် ဖျက်လိုတဲ့ index ကို ရွေးပြီး ဖျက်လို့ မရဘူး။ set ထဲမှာ ရှိနေတဲ့ ထိပ်ဆုံးအခန်းကို ဖျက်လိုက်တာဖြစ်တယ် (ဒါကြောင့် သူ ဘယ်နားကို ဖျက်လိုက်တယ်ဆိုတာ မသိရဘူး)

> ```set.clear()``` နဲ့ ```del set``` ကွာခြားတာကတော့ clear က set ထဲမှာရှိတဲ့ items တွေအားလုံးကိုပဲ ဖျက်တာ၊ del ကတော့ အဲဒီ variable တစ်ခုလုံးကို ဖျက်လိုက်တာ


```python
odd = (1,3,5,7,9,11,13,15)
print(odd[3:7])
print(odd[:5])
print(odd[6:])
print(odd[-4:-2])
print(odd[-4:7])
```
###### Output:
```
(7, 9, 11, 13)
(1, 3, 5, 7, 9)
(13, 15)
(9, 11)
(9, 11, 13)
```

##### Example 4 (checking an item)
List
```python
mylist = ['a','e',30,'o','u']

if 'a' in mylist:
	print('a is in list')
else:
	print('no a')

if 'b' in mylist:
	print('b is in list')
else:
	print('no b')
```
###### Output:
```
a is in list
no b
```
Tuple
```python
mytup = ('a','e',30,'o','u')

if 'a' in mytup:
	print('a is in tuple')
else:
	print('no a')

if 'b' in mytup:
	print('b is in tuple')
else:
	print('no b')
```
###### Output:
```
a is in tuple
no b
```

##### Example 5 (Changing item)

> Tuple မှာ values တွေကို change လို့မရပါဘူး

```python
color = ['red','green','blue']

color[1]='orange'
print(color)

color[2]=['pink','yellow']
print(color)

color[2]=('pink','yellow')
print(color)

color[1:3]=['black']
print(color)

color.insert(1,'white')
print(color)
```
###### Output:
```
['red', 'orange', 'blue']
['red', 'orange', ['pink', 'yellow']]
['red', 'orange', ('pink', 'yellow')]
['red', 'black']
['red', 'white', 'black']
```

##### Example 6 (Add Items)
```python
men = ["hla","tun"]

men.append('mya')
print(men)

men.insert(3,'ba')
print(men)

boys = ['ko','nyi']

men.extend(boys)
print(men)
```
###### Output:
```
['hla', 'tun', 'mya']
['hla', 'tun', 'mya', 'ba']
['hla', 'tun', 'mya', 'ba', 'ko', 'nyi']
```

##### Example 7 (Remove Items)

> ```list.remove(item)``` အသုံးပြုခြင်း

```python
colors = ['red', 'orange', 'blue']
colors.remove('orange')

print(colors)
```
###### Output:
```
['red', 'blue']
```

> ```list.remove(item)``` မှာ remove လုပ်ချင်တဲ့ item က list ထဲ မရှိရင် error တက်ပါတယ်

##### Error Example (don't do it)
```python
colors = ['red', 'orange', 'blue']
colors.remove('black')

print(colors)
```
###### Output:
```
Traceback (most recent call last):
  File "test.py", line 2, in <module>
    colors.remove('black')
ValueError: list.remove(x): x not in list
```

> ```list.pop(index)``` ကို အသုံးပြုခြင်း

> parameter မထည့်ရင် Default အနေနဲ့ နောက်ဆုံးအခန်းကို remove လုပ်တယ်

##### Example 8 (remove using pop())
```python
years = [2017,2018,2019,2020]

years.pop(1)
print(years)

years.pop()
print(years)
```
###### Output:
```
[2017, 2019, 2020]
[2017, 2019]
```

> ```del``` ဆိုတဲ့ keyword နဲ့လဲ Remove လုပ်လို့ရပါတယ်

##### Example 9 (del)
```python
years = [2017,2018,2019,2020]

del years[1]
print(years)
```
###### Output:
```
[2017, 2019, 2020]
```

##### Example 10 (clear)

> Removing all items

```python
years = [2017,2018,2019,2020]

years.clear()
print(years)
```
###### Output:
```
[]
```

<br>
<hr>

#### List Methods

##### Example 11 (reverse)

```python
numbers = [4,7,1,2,3]
numbers.reverse()
print(numbers)
```
###### Output:
```
[3, 2, 1, 7, 4]
```

##### Example 12 (sort)

> Sorting Alphabetically & Numerically

```python
colors = ['red','green','blue']
colors.sort()
print(colors)
```
###### Output:
```
['blue', 'green', 'red']
```

##### Example 13 (sort descending)

```python
numbers = [4,7,1,2,3]
numbers.sort(reverse=True)
print(numbers)
```
###### Output:
```
[7, 4, 3, 2, 1]
```

#### List Copy

> list တွေကို copy လုပ်တဲ့အခါမှာ ၂ နည်းလုပ်လို့ရပါတယ်

> ဒါပေမယ့် ```list2 = list1``` ဆိုပြီး string တွေ integer တွေလို copy လို့ မရပါဘူး။
> အဲ့လို လုပ်ခြင်းက value တွေ သာ copy ရုံမကပဲ ```list2``` သည် ```list1``` ကို ကိုယ်စားပြုသလိုဖြစ်သွားပါတယ်။

> အဲ့တော့ ဘာပြဿနာတက်လဲဆိုရင် list2 ကို ပြင်လိုက်ရင် ```list1``` ပါ လိုက်ပြီး ပြောင်းလဲသွားသလို ```list1``` ကိုပြုပြင်လိုက်ရင် ```list2``` ပါ လိုက်ပြီး ပြောင်းလဲသွားပါတယ်။

> အဲ့ဒါကြောင့် list တွေကို copy ကူးလိုတဲ့အခါ အောက်ဖော်ပြပါ ၂ နည်းထဲက တစ်နည်းကိုသာ သုံးဖို့ အကြံပေးပါတယ်။

1. List Method (copy)
2. Build-in Method (list)

##### Example 14 (using list.copy())
```python
colors = ['red','green','blue']
colors_copy = colors.copy()
print(colors_copy)
```
###### Output:
```
['red', 'green', 'blue']
```

##### Example 15 (using list(iterable))
```python
numbers = [4,7,1,2,3]
num_copy = list(numbers)
print(numbers)
```
###### Output:
```
[4, 7, 1, 2, 3]
```

**Other List Methods**

| Methods | Description |
| --- | --- |
| append() | Adds an element at the end of the list |
| clear() | Removes all the elements from the list |
| copy() | Returns a copy of the list |
| count() | Returns the number of elements with the specified value |
| extend() | Add the elements of a list (or any iterable), to the end of the current list |
| index() | Returns the index of the first element with the specified value |
| insert() | Adds an element at the specified position |
| pop() | Removes the element at the specified position |
| remove() | Removes the first item with the specified value |
| reverse() | Reverses the order of the list |
| sort() | Sorts the list |