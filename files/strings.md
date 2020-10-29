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
A  for Apple
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
###### Slicing & Negative Index
Format : ``` mystr[x:y] ```
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

*maxsplitနေရာမှာ ဘာမှမထည့်ရင် default အဖြစ် -1 လို့သတ်မှတ်ပြီး အကုန်လုံးကို ထုတ်ပေးပါတယ်*
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