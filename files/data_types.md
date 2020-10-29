### 0x03 Data Types

|  | Types |
| --- | --- |
| [Text Type](#text-type) | ```str``` |
| [Numeric Types](#numeric-types) | ```int```, ```float```, ```complex``` |
| [Sequence Types](#sequence-types) | ```list```, ```tuple```, ```range``` |
| [Mapping Type](#mapping-type) | ```dict``` |
| [Set Types](#set-types) | ```set```, ```frozenset```|
| [Boolean Type](#boolean-type) | ```bool``` |
| [Binary Types](#binary-types) | ```bytes```, ```bytearray```, ```memoryview``` |

*Reference from [W3School](https://www.w3schools.com/)*

<hr>
<br>

#### Text Type

##### Example 1 (str)
```python
x = "Logix Owl"

print(x)
print(type(x))
```
###### Output:
```
Logix Owl
<class 'str'>
```

**Note**
```type()``` can show the type of any objects

<hr>
<br>

#### Numeric Types

##### Example 2 (int)
```python
x = 100

print(x)
print(type(x))
```
###### Output:
```
100
<class 'int'>
```

##### Example 3 (float)
```python
x = 99.9

print(x)
print(type(x))
```
###### Output:
```
99.9
<class 'float'>
```

##### Example 4 (complex)
```python
x = 2+3j

print(x)
print(type(x))
```
###### Output:
```
(2+3j)
<class 'complex'>
```

<hr>
<br>

#### Sequence Types

##### Example 5 (list)
```python
x = [ "red" , "green" , "blue" ]

print(x)
print(type(x))
```
###### Output:
```
['red', 'green', 'blue']
<class 'list'>
```

##### Example 6 (tuple)
```python
x = ( "red" , "green" , "blue" )

print(x)
print(type(x))
```
###### Output:
```
('red', 'green', 'blue')
<class 'tuple'>
```

##### Example 7 (range)
```python
x = range(6)

print(x)
print(type(x))
```
###### Output:
```
range(0, 6)
<class 'range'>
```

<hr>
<br>

#### Mapping Type

##### Example 8 (dict)
```python
x = { "name" : "Logix Owl" , "age" : 24 }

print(x)
print(type(x))
```
###### Output:
```
{'name': 'Logix Owl', 'age': 24}
<class 'dict'>
```

<hr>
<br>

#### Set Types

##### Example 9 (set)
```python
x = { "red" , "green" , "blue" }

print(x)
print(type(x))
```
###### Output:
```
{'blue', 'red', 'green'}
<class 'set'>
```

##### Example 10 (frozenset)
```python
x = frozenset({ "red" , "green" , "blue" })

print(x)
print(type(x))
```
###### Output:
```
frozenset({'blue', 'red', 'green'})
<class 'frozenset'>
```

<hr>
<br>

#### Boolean Type

##### Example 11 (bool)
```python
x = True

print(x)
print(type(x))
```
###### Output:
```
True
<class 'bool'>
```

<hr>
<br>

#### Binary Types

##### Example 12 (bytes)
```python
x = b"Logix Owl"

print(x)
print(type(x))
```
###### Output:
```
b'Logix Owl'
<class 'bytes'>
```

##### Example 13 (bytearray)
```python
x = bytearray(6)

print(x)
print(type(x))
```
###### Output:
```
bytearray(b'\x00\x00\x00\x00\x00\x00')
<class 'bytearray'>
```

##### Example 14 (memoryview)
```python
x = memoryview(bytes(6))

print(x)
print(type(x))
```
###### Output:
```
<memory at 0x7fc301562580>
<class 'memoryview'>
```

<hr>
<br>

[Next (0x04 Strings)](./strings.md)