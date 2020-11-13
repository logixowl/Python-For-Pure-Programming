### Lists & Tuple

#### List

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

boys = ('ko','nyi')

men.extend(boys)
print(men)
```
###### Output:
```
['hla', 'tun', 'mya']
['hla', 'tun', 'mya', 'ba']
['hla', 'tun', 'mya', 'ba', 'ko', 'nyi']
```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```

##### Example  ()
```python

```
###### Output:
```

```
