### Dictionary

* unordered ဖြစ်ပါတယ်
* ```key,value``` ဆိုပြီး အတွဲလိုက်သိမ်းပေးရပါတယ်
* ```key``` ကိုသုံးပြီး value ကို ဆွဲထုတ်ရပါတယ်
* ```key``` တွေ duplicate ဖြစ်နေလို့မရပါဘူး
* ```value``` တွေကတော့ တူလို့ရပါတယ်

#### Declaration

##### Example 1
```python
myDict = {2:'apple', 4.5:'orange', 'l':'logixowl'}

print(myDict[4.5])
print(myDict[2])
print(myDict['l'])
```
###### Output:
```
orange
apple
logixowl
```

> ဒီလိုလေးလဲ ရေးလို့ရပါတယ်

##### Example 2
```python
days = {
	'mon':'Monday',
	'tue':'Tuesday',
	'web':'Webnesday',
	'thu':'Thursday',
	'fri':'Friday',
	'sat':'Saturday',
	'sun':'Sunday'
}

print(days)
```
###### Output:
```
{'mon': 'Monday', 'tue': 'Tuesday', 'web': 'Webnesday', 'thu': 'Thursday', 'fri': 'Friday', 'sat': 'Saturday', 'sun': 'Sunday'}
```

##### Example 3
```python
person = {}
person['name'] = "Ba Kyaw"
person['age'] = 34
person['gender'] = "male"

print(person)
```
###### Output:
```
{'name': 'Ba Kyaw', 'age': 34, 'gender': 'male'}
```

##### Example 4 (access items)
```python
days = {
	'mon':'Monday',
	'tue':'Tuesday',
	'web':'Webnesday',
	'thu':'Thursday',
	'fri':'Friday',
	'sat':'Saturday',
	'sun':'Sunday'
}

print(days['sun'])
print(days.get('sat'))

# this will return None
print(days.get('other'))

# Don't do it (Error)
print(days['other'])
```
###### Output:
```
Sunday
Saturday
None
Traceback (most recent call last):
  File "test.py", line 19, in <module>
    print(days['other'])
KeyError: 'other'
```

##### Example 5 (dict_keys)
```python
days = {
	'mon':'Monday',
	'tue':'Tuesday',
	'web':'Webnesday'
}

dicKeys = days.keys()

print(dicKeys)
print(type(dicKeys))

days['sun']='Sunday'
print(dicKeys)
```
###### Output:
```
dict_keys(['mon', 'tue', 'web'])
<class 'dict_keys'>
dict_keys(['mon', 'tue', 'web', 'sun'])
```

##### Example 6 (dict_values)
```python
days = {
	'mon':'Monday',
	'tue':'Tuesday',
	'web':'Webnesday'
}

dicValues = days.values()

print(dicValues)
print(type(dicValues))

days['sun']='Sunday'

print(dicValues)
```
###### Output:
```
dict_values(['Monday', 'Tuesday', 'Webnesday'])
<class 'dict_values'>
dict_values(['Monday', 'Tuesday', 'Webnesday', 'Sunday'])
```

##### Example 7 (dict_items)
```python
days = {
	'mon':'Monday',
	'tue':'Tuesday'
}

dicItems = days.items()

print(dicItems)
print(type(dicItems))

days['sun']='Sunday'

print(dicItems)
```
###### Output:
```
dict_items([('mon', 'Monday'), ('tue', 'Tuesday')])
<class 'dict_items'>
dict_items([('mon', 'Monday'), ('tue', 'Tuesday'), ('sun', 'Sunday')])
```

##### Example 8 (removing)
```python
months = {
	'JAN':'January',
	'FEB':'February',
	'MAR':'March',
	'APR':'April',
	'MAY':'May'
}

print("> Using dict.pop(key)")
print(months.pop('JAN'))
print(months)
print()

print("> Using dict.popitem()")
print(months.popitem())
print(months)
print()

print("> Using del")
del months['FEB']
print(months)
print()

print("> Using dict.clear()")
months.clear()
print(months)
print()

# Don't do it (error)
print("> Using del")
del months
print(months)
print()
```
###### Output:
```
> Using dict.pop(key)
January
{'FEB': 'February', 'MAR': 'March', 'APR': 'April', 'MAY': 'May'}

> Using dict.popitem()
('MAY', 'May')
{'FEB': 'February', 'MAR': 'March', 'APR': 'April'}

> Using del
{'MAR': 'March', 'APR': 'April'}

> Using dict.clear()
{}

> Using del
Traceback (most recent call last):
  File "test.py", line 33, in <module>
    print(months)
NameError: name 'months' is not defined
```

##### Example 9 (looping)
```python
person = {
	"name": "Bo Kyaw",
	"age" : 39,
	"gender": "male",
	"skills": ['programming','developing']
}

# method 1
for p in person:
	print(p, "\t>", person[p])

print('________________')
# method 2
for key,value in person.items():
	print(key, "\t:", value)
```
###### Output:
```
name    > Bo Kyaw
age     > 39
gender  > male
skills  > ['programming', 'developing']
________________
name    : Bo Kyaw
age     : 39
gender  : male
skills  : ['programming', 'developing']
```

<hr>
<br>

##### Program 1 (using dict and list)
```python
students = [
	{
		"id": 1,
		"name": "Mg Mg",
		"email": "mgmg@gmail.com"
	},
	{
		"id": 2,
		"name": "Myo Myo",
		"email": "myo@gmail.com"
	},
	{
		"id": 3,
		"name": "Thu Thu",
		"email": "thu@gmail.com"
	}
]

for student in students:
	for key, value in student.items():
		print(key,"\t:",value)
	print("________________")
```

###### Output
```
id      : 1
name    : Mg Mg
email   : mgmg@gmail.com
________________
id      : 2
name    : Myo Myo
email   : myo@gmail.com
________________
id      : 3
name    : Thu Thu
email   : thu@gmail.com
________________
```

**Other Dictionary Methods**

| Method | Description |
| --- | --- |
| clear() | Removes all items from the dictionary. |
| copy() | Returns a shallow copy of the dictionary. |
| fromkeys(seq[, v]) | Returns a new dictionary with keys from seq and value equal to v (defaults to None). |
| get(key[,d]) | Returns the value of the key. If the key does not exist, returns d (defaults to None). |
| items() | Return a new object of the dictionary's items in (key, value) format. |
| keys() | Returns a new object of the dictionary's keys. |
| pop(key[,d]) | Removes the item with the key and returns its value or d if key is not found. If d is not provided and the key is not found, it raises KeyError. |
| popitem() | Removes and returns an arbitrary item (key, value). Raises KeyError if the dictionary is empty. |
| setdefault(key[,d]) | Returns the corresponding value if the key is in the dictionary. If not, inserts the key with a value of d and returns d (defaults to None). |
| update([other]) | Updates the dictionary with the key/value pairs from other, overwriting existing keys. |
| values() | Returns a new object of the dictionary's values |

*Reference from [Programiz](https://www.programiz.com)*
