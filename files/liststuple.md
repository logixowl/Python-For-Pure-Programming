### Lists & Tuple

##### Example 1 (declare)
List
```python
strlist = ['a', 'b', 'c', 'd']
print(strlist)

numlist = [1,2,3,4,5]
print(numlist)

mixlist = ['red', 20, 'a', 4.5, 3+9]
print(mixlist)

nestedlist = ['g', 32, ['a','b',4], 'hello']
print(nestedlist)
```
###### Output:
```
['a', 'b', 'c', 'd']
[1, 2, 3, 4, 5]
['red', 20, 'a', 4.5, 12]
['g', 32, ['a', 'b', 4], 'hello']
```
Tuple
```python
strtup = ('a', 'b', 'c', 'd')
print(strtup)

numtup = (1,2,3,4,5)
print(numtup)

mixtup = ('red', 20, 'a', 4.5, 3+9)
print(mixtup)

nestedtup = ('g', 32, ('a','b',4), 'hello')
print(nestedtup)
```
###### Output:
```
('a', 'b', 'c', 'd')
(1, 2, 3, 4, 5)
('red', 20, 'a', 4.5, 12)
('g', 32, ('a', 'b', 4), 'hello')
```

##### Example 2 (access items)

List
```python
nestedlist = ['g', 32, ['a','b',4], 'hello']
print(nestedlist[0])
print(nestedlist[-1])
print(nestedlist[2])
print(nestedlist[2][1])
```
###### Output:
```
g
hello
['a', 'b', 4]
b
```
Tuple
```python
nestedtup = ('g', 32, ('a','b',4), 'hello')
print(nestedtup[0])
print(nestedtup[-1])
print(nestedtup[2])
print(nestedtup[2][1])
```
###### Output:
```
g
hello
('a', 'b', 4)
b
```

##### Example 3 (slicing)
List
```python
odd = [1,3,5,7,9,11,13,15]
print(odd[3:7])
print(odd[:5])
print(odd[6:])
print(odd[-4:-2])
print(odd[-4:7])
```
###### Output:
```
[7, 9, 11, 13]
[1, 3, 5, 7, 9]
[13, 15]
[9, 11]
[9, 11, 13]
```
Tuple
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