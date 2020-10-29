### Numeric

```int``` ```float``` ```complex``` ဆိုတဲ့ data types တွေပါဝင်ပါတယ်။

##### Example 1 (Declaration)
```python
a = 100
b = 99.9
c = 2+3j

print(a, type(a))
print(b, type(b))
print(c, type(c))
```
###### Output:
```
100 <class 'int'>
99.9 <class 'float'>
(2+3j) <class 'complex'>
```

<br>
<hr>

#### Number Type Conversion

##### Example 2 (int)

> ```int()``` function မှာ parameter ၁ ခု နဲ့ ၂ ခုဆိုပြီးတော့ ၂ မျိုးသုံးလို့ ရတယ်။

```python
num_string = "98765"
print("Before: ", end='')
print(num_string, ",", type(num_string))

number = int(num_string)
print("After: ", end='')
print(number, ",", type(number))
```
###### Output:
```
Before: 98765 , <class 'str'>
After: 98765 , <class 'int'>
```

##### Example 3 (int with base)

> first parameter က string ဖြစ်ရမယ်

> second parameter က base (int) ဖြစ်ရမယ်

```python
raw_num = "100"

print("Base 10:", int(raw_num, 10))
print("Base 2:", int(raw_num, 2))
print("Base 8:", int(raw_num, 8))
print("Base 16:", int(raw_num, 16))
```
###### Output:
```
Base 10: 100
Base 2: 4
Base 8: 64
Base 16: 256
```

##### Example 4 (float)
```python
num_string = "2468.9"
number = float(num_string)

print(number, ",", type(number))
```
###### Output:
```
2468.9 , <class 'float'>
```

##### Example 5 (complex)

> သူလဲ int လို နှစ်မျိုးသုံးလို့ရတယ်။

```python
c1 = complex("2+3j")
c2 = complex(2,3)

print(c1)
print(c2)
```
###### Output:
```
(2+3j)
(2+3j)
```

##### Example 6 (ord)

> character ကနေ integer ကို ပြောင်းတာ

```python
print(ord('a'))
print(ord('9'))
```
###### Output:
```
97
57
```

##### Example 7 (chr)

> integer ကနေ character ပြန်ပြောင်းတာ

```python
print(chr(97))
print(chr(57))
```
###### Output:
```
a
9
```

##### Example 8 (hex)

> Hexadecimal string ဖြစ်အောင်ပြောင်းတာ 

```python
print(hex(30))
```
###### Output:
```
0x1e
```

##### Example 9 (oct)

> Octal string ဖြစ်အောင်ပြောင်းတာ

```python
print(oct(30))
```
###### Output:
```
0o36
```

> [ASCII table](./ascii_table.md) ကို ဒီမှာ ကြည့်လို့ ရပါတယ်။

<br>
<hr>

#### Mathematical Functions

##### Example 10 (abs)

> ကျောင်းမှာသင်ခဲ့ရသလိုမျိုး ```|-1| = 1``` absolute value ကို ယူတာ

```python
n1 = -99
n2 = 50
n3 = 123.9

print(abs(n1))
print(abs(n2))
print(abs(n3))
```
###### Output:
```
99
50
123.9
```

##### Example 11 (round)

> အနီးစပ်ဆုံး ဒဿမနေရာကို integer အဖြစ်ယူတယ်

```python
print(round(100))
print(round(100.1))
print(round(100.6))
print(round(-100.6))
```
###### Output:
```
100
100
101
-101
```

##### Example 12 (round 2)

> parameter နှစ်ခုထည့်ပြီး ```round(number, number of digit)``` သုံးလို့ ရတယ်။

> ```number of digit``` ဆိုတာ ဒဿမနေရာယူတာ

```python
num = 2/3

print(num)
print(round(num,3))

print(round(3.456,2))
```
###### Output:
```
0.6666666666666666
0.667
3.46
```

##### Example 13 (ceil)

> x ထက်မငယ်တဲ့ အငယ်ဆုံး integer ကို ထုတ်ပေးတယ်။

> သူ့ကို သုံးချင်တယ်ဆိုရင် math ဆိုတဲ့ module တစ်ခုကို import လုပ်ပေးရတယ်

```python
import math

print(math.ceil(100))
print(math.ceil(100.1))
print(math.ceil(100.9))
print(math.ceil(-100.1))
```
###### Output:
```
100
101
101
-100
```

##### Example 14 (floor)

> x ထက် မကြီးတဲ့ အကြီးဆုံး integer ကို ထုတ်ပေးတယ်။

> သူလဲ math module ကို import လုပ်ပေးရတယ်။

```python
import math

print(math.floor(100))
print(math.floor(100.1))
print(math.floor(100.9))
print(math.floor(-100.1))
```
###### Output:
```
100
100
100
-101
```

##### Example 15 (pow)

> **Usage** ```pow(x,y)```or ```pow(x,y,z)```

> ```x``` = base

> ```y``` = power

> ```z``` = modulus

```python
print(pow(10,2))
print(pow(10,-2))

print(pow(99,9))
print(pow(99,9,999))
```
###### Output:
```
100
0.01
913517247483640899
702
```

##### Example 16 (sqrt)

> ဒါကတော့ Square Root ပြန်ရှာပေးတာပါ

```python
import math

print(math.sqrt(25))
print(math.sqrt(30))
```
###### Output:
```
5.0
5.477225575051661
```

##### Example 17 (max)

> အကြီးဆုံး value ကို return ပြန်ပေးတယ်

```python
m = max(2,3,4,5,10,-1,0)

print(m)
```
###### Output:
```
10
```

##### Example 18 (min)

> အငယ်ဆုံး value ကို return ပြန်ပေးတယ်

```python
m = min(2,3,4,5,10,-1,0)

print(m)
```
###### Output:
```
-1
```

> For more numeric function > [TutorialsPoint](https://www.tutorialspoint.com/python/python_numbers.htm)

