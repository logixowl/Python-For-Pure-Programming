### Loops

![]()

Loop နှစ်မျိုးရှိတယ်
1. ```while``` loop
2. ```for``` loop

#### while Loops

**Format**

```python
while (condition)
    ...
    ...
```

> condition မှန်နေသ၍ ```while``` အတွင်းထဲကို အလုပ်လုပ်မယ်။

##### Example 1 (number output)
```python
num = 1

while num < 10:
	print(num)
	num += 1
```
###### Output:
```
1
2
3
4
5
6
7
8
9
```

##### Example 2 (number output reverse)
```python
num = 9

while num > 0:
	print(num)
	num -= 1
```
###### Output:
```
9
8
7
6
5
4
3
2
1
```

##### Example 3 (Get Evens Program)
```python
num = 0

while num < 10:
	print(num)
	num += 2
```
###### Output:
```
0
2
4
6
8
```

##### Example 4 (infinite loop) (Don't do it)
```python
while True:
	print("Hello")
```
###### Output:
```
Hello
Hello
Hello
Hello
Hello
Hello
Hello
Hello
^CHello
Traceback (most recent call last):
  File "test.py", line 3, in <module>
    print("Hello")
KeyboardInterrupt
```

##### Example 5 (infinite input loop)
```python
while True:
	name = input("Enter your name: ")
	print("Hello",name)
```
###### Output:
```
Enter your name: logix
Hello logix
Enter your name: owl
Hello owl
Enter your name: logix owl
Hello logix owl
Enter your name: ^CTraceback (most recent call last):
  File "test.py", line 2, in <module>
    name = input("Enter your name: ")
KeyboardInterrupt
```

##### Example 5 (looped number comparison)
```python
num = int(input('Enter a number: '))

while num != 999:
	if num > 0:
		print('Positive')
	elif num < 0:
		print('Negative')
	else:
		print('Zero')

	num = int(input('Enter a number: '))

print("Done")
```
###### Output:
```
Enter a number: 2
Positive
Enter a number: 0
Zero
Enter a number: -1
Negative
Enter a number: 999
Done
```

##### Example 6 (break)
```python
num = 1

while num < 10:
	print(num)
	if num == 5:
		break
	num += 1
```
###### Output:
```
1
2
3
4
5
```

##### Example 7 (continue)
```python
num = 0

while num < 10:
	num += 1
	if num == 5:
		continue
	print(num)
```
###### Output:
```
1
2
3
4
6
7
8
9
10
```

##### Example 8 (infinite calculator program)
```python
ip = input('Enter a operation or stop: ')

while ip != 'stop':
	arr = ip.split(' ')
	a = int(arr[0])
	operator = arr[1]
	b = int(arr[2])
	ans = 0

	if operator == '+':
		ans = a + b
	elif operator == '-':
		ans = a - b
	elif operator == '*':
		ans = a * b
	elif operator == '/':
		ans = a / b
	else:
		ans = "Invalid operator"

	print(str(a) + operator + str(b) + '=' + str(ans))

	ip = input('Enter a operation or stop: ')
```
###### Output:
```
Enter a operation or stop: 2 + 6
2+6=8
Enter a operation or stop: 6 / 3
6/3=2.0
Enter a operation or stop: 3 * 5
3*5=15
Enter a operation or stop: stop
```

##### Example 9 (infinite sum program)
```python
ip = input('Enter a number or stop to output: ')
ans = 0
while ip != 'stop':
	ans = ans + int(ip)
	ip = input('Enter a number or stop to output: ')

print('Total sum =',ans)
```
###### Output:
```
Enter a number or stop to output: 2
Enter a number or stop to output: 3
Enter a number or stop to output: 4
Enter a number or stop to output: 1
Enter a number or stop to output: stop
Total sum = 10
```

##### Example 1 (number output)
```python

```
###### Output:
```

```
