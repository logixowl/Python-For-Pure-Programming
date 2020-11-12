### Strings

##### Example 1 (Single Line String)
String တစ်ခုကို output ထုတ်ရန်အတွက်```'(single quotes)```သို့မဟုတ် ```"(double quotes)```ကို သုံးနိုင်ပါတယ်
```python
print("Logix Owls")
print('Logix Owls')
```
###### Output :
```
Logix Owls
Logix Owls
```
##### Example 2 (Assign to a Variable)
```python
hello = "Hello Logix Owls"
print(hello)
print(type(hello))
```
###### Output :
```
 Hello Logix Owls
 <class 'str'>
```

#### Special(Escape) Characters in String

> ```' '``` အဖွင့်အပိတ်ကြားထဲမှာ ```'``` ကို ထည့်ချင်တဲ့အချိန် (သို့မဟုတ်) ```" "``` အဖွင့်အပိတ်ကြားထဲမှာ ```"``` ကို ထည့်ချင်တဲ့ အချိန်တွေမှာ ```\``` (back slash) ကို သုံးရပါတယ်။

```python
print('mg mg\'s book')
print("she says \"i love you\"")
```
###### Output:
```
mg mg's book
she says "i love you"
```

**Some useful special characters**

> ```\t``` = tab

> ```\n``` = new line

> ```\r``` = carriage return

> ```\\``` = back slash

<br>

##### Example 3 (Multiline String)
တစ်ကြောင်းထက်ပိုသော( Enter ဆင်းထားသော) strings များကို output ထုတ်ချင်လျှင်```'''(single quotes)```သုံးခု သို့မဟုတ်```"""(double quotes)```သုံးခုကို အသုံးပြုရပါမည်
```python
hello='''Hello Owls,
Have a nice day!'''
print(hello)
```
###### Output :
```
Hello Owls,
Have a nice day!
```
```python
print("""A for Apple
B for Beer""")
```
###### Output :
```
A for Apple
B for Beer
```

##### Example 4 (String Length)
```python
hello = "Hello Logix Owls"
print(len(hello))
```
###### Output :
```
16
```

##### Example 5 (String Concatenation)
```python
hello1 = "Hello"
hello2 = "Logix Owls"
hello = hello1 + hello2
print(hello)
```
###### Output :
```
HelloLogix Owls
```

```python
hello1 = "Hello"
hello2 = "Logix Owls"
hello = hello1 +" "+ hello2
print(hello)
```
###### Output :
```
Hello Logix Owls
```

##### Example 6 (Index)
| L | o | g | i | x | O | w | l |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| -8 | -7 | -6 | -5 | -4 | -3 | -2 | -1 |

```python
mystr = "LogixOwl"
print(mystr[4])
```
###### Output :
```
x
```
#### Slicing & Negative Index
> Format : ``` mystr[x:y] ```
```
x = စမယ့် စာလုံးရဲ့ index
y = နောက်ဆုံးထုတ်ချင်တဲ့စာလုံးရဲ့ index ကို တစ်ခန်းပိုယူ
```
*x နေရာမှာ ဘာမှမထည့်ရင် default အနေနဲ့ index 0 လို့သတ်မှတ်*

*y နေရာမှာ ဘာမှမထည့်ရင် default အနေနဲ့ last index+1 အဖြစ်သတ်မှတ်*

```python
print(mystr[1:8])
print(mystr[-6,-1])
print(mystr[:6])
print(mystr[3:])
```
###### Output :
```
ogixOwl
gixOw
LogixO
ixOwl
```
#### String Methods
##### Example 7 : strip()
*string တစ်ခုရဲ့ အစနဲ့အဆုံးမှာရှိတဲ့ space တွေ next line တွေကို ဖယ်ထုတ်ချင်တဲ့အခါမှာ အသုံးပြုပါတယ်*
```python
str1 = "Logix Owls "
str2 = '''


Hello Owls!'''
print(str1.strip())
print(str2.strip())
```
###### Output : 
```
Logix Owls
Hello Owls!
```

##### Example 8 : split()
***return List***

Format : ``` string.split("separator", maxsplit) ```

*separator နေရာမှာ ဘာမှမထည့်ရင် default အဖြစ် whitespace ကိုသတ်မှတ်ပါတယ်*

*maxsplit တွင် ကိုယ်ထုတ်ချင်တဲ့ split အရေအတွက်ထက် တစ်ခုလျော့ပြီး သတ်မှတ်ပေးရပါမယ်*

*maxsplit နေရာမှာ ဘာမှမထည့်ရင် default အဖြစ် -1 လို့သတ်မှတ်ပြီး အကုန်လုံးကို ထုတ်ပေးပါတယ်*
```python
mystr = "Logix Owls,owls"
print(mystr.split())
print(mystr.split(","))
print(mystr.split("o"))
print(mystr.split("o",1))
```
###### Output :
```
['Logix', 'Owls,owls']
['Logix Owls', 'owls']
['L', 'gix Owls,', 'wls']
['L', 'gix Owls,owls']

```

##### Example 9 : lower()
> string တစ်ခုလုံးကို lower case (စာလုံးအသေး) ပြောင်းပေးတာ

```python
name = 'LOGIXOWL'

print(name.lower())

print("Nay Kg LR?".lower())
```
###### Output:
```
logixowl
nay kg lr?
```

##### Example 10 : upper()
> string တစ်ခုလုံးကို upper case (စာလုံးအကြီး) ပြောင်းပေးတာ

```python
name = 'logixowl'

print(name.upper())

print("Nay Kg Lr?".upper())
```
###### Output:
```
LOGIXOWL
NAY KG LR?
```

##### Example 11 : replace()
> Format : ```string.replace(oldstr, newstr)```

```python
oldstr = "dogs are so cute, so i love dogs"
newstr = oldstr.replace('dogs','cats')

print(oldstr)
print(newstr)
```
###### Output:
```
dogs are so cute, so i love dogs
cats are so cute, so i love cats
```

##### Example 12 : replace() with 3 parameters
> Format : ```string.replace(oldstr, newstr, count)```

```python
mytext = 'hi everyone, hi ladies, hi gentleman'

print(mytext)
print(mytext.replace('hi','hello'))
print(mytext.replace('hi','hello',2))
```
###### Output:
```
hi everyone, hi ladies, hi gentleman
hello everyone, hello ladies, hello gentleman
hello everyone, hello ladies, hi gentleman
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