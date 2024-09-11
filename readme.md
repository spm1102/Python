# Python syntax
## Variable and basic data type in Python
- **Variable** like other program's languages, variables' names in Python must follow several rules\:
  - The 1st letter is alpha (a,b,A,B,...)
  - Do not contain space
  - Not be key words in Python\:
    ![alt text](image.png)
  - Do not use special letter (!, @, #, $, ...)
  - Should clearly represent the purpose
- **Data type**\: int, float, str, bool, complex
  - To determine what kind of data type of a variable is, using `type()` function\:
    ```Python
    a = 100
    print(type(a))              # int
    ```
- **Operator\:**
  - **Comparator operator\:**
    ![alt text](image-1.png)
  - **Note\:** When comparing 2 float numbers, **SHOULD NOT** use the `==` operator. Instead, using a small enough number as the comparator
  - **Logic Comparator\:**
    ![alt text](image-3.png)
- **Assignment**\:
![alt text](image-2.png)
## String
### Basic syntax\:
- To create a string, put it into a `""` or `''`
- To include multiple lines in the string use `""" """`
For example\:
```Python
a = 'Python'               
print(a)                        # Python
a = "Python"
print(a)                        # Python
a = '''Python'''
print(a)                        # Python
a = """Python, Lập trình
           Python"""
print(a)                        # Python, Lập trình
                                # Python
```
### Combine strings
- Using `+` operator\: 
```Python
a = "Python"
b = "is easy"
print(a + b)                    # Python is easy
```
- Using `*` operator\:
```Python
a = "Python"
print(a * 3)                    # PythonPythonPython
```
- Using parentheses `()`\:
```Python
a = 'Python ''Javascript'
b = ('Python '
            'Java')
print(a)                        # Python Javascript
print(b)                        # Python Java
```
- Using `join()` method\: `separator_string.join(iterable)`
  ```Python
  # .join() with lists
  numList = ['1', '2', '3', '4']
  separator = ', '
  print(separator.join(numList)) #1, 2, 3, 4
  # join elements of text with space
  text = ['Python', 'is', 'a', 'great', 'programming', 'language']
  print(' '.join(text))          #Python is a great programming language

  #join string
  s1 = 'abc'
  s2 = '123'
  # each element of s2 is separated by s1
  print('s1.join(s2):', s1.join(s2))        #s1.join(s2): 1abc2abc3
  # each element of s1 is separated by s2
  print('s2.join(s1):', s2.join(s1))        #s2.join(s1): a123b123c
  ```
### Input() function
```Python
name = input("Enter your name: ")
print(name)                     # Enter your name: 

```
### Element's accessment in string
- String uses index just like list()
- For example\:
```Python
a = "Python TEK4.VN"
print(a)                        #Python TEK4.VN
print(a[2])                     #t
print(a[-1])                    #N
```
### Substring
- Similar with sublist\:`str[start:end:step]`
  ```Python
  my_string = "Python is easy"
  a1=my_string[0:3] 
  a2=my_string[2:-2] 
  print(a1)                     #Pyt
  print(a2)                     #thon is ea
  ```
- Using `split(separator, maxsplit)` to divide the string into a list including `maxsplit` elements separated by `separator` 
  ```Python
  text= 'I love Python'
  print(text.split()) #split with " " separator

  number_string = '1, 2, 3, 4, 5'
  print(number_string.split(', ')) #split with ', ' separator
  print(number_string.split(':')) #split with ':' separator
  print(number_string.split(', ', 2)) # maxsplit: 2
  ```
  Result:\:
  ```Python
  ['I', 'love', 'Python']
  ['1', '2', '3', '4', '5']
  ['1, 2, 3, 4, 5']
  ['1', '2', '3, 4, 5']
  ```
- Using `len()` to calculate the string length
- Using `in` or `not in` to check if an element is in the string
### Change a string
- Using `replace(a, b)` to replace a by b
- Using `del a` to delete a completely
- Using `strip(a)`, `rstrip(a)` and `lstrip(a)` to eliminate `a` from both ends, right and left of the string respectively
- Using `print(*object, sep = ' ', end = '\n', file = sys.stdout, flush = False)` as advanced print method
- **`f_string` method**\:
  ```Python
  name = "tek.vn"
  name2 = "Python"
  print(f"{name2} is easy to learn with {name}!")   # Python is easy to learn with tek.vn!
  ```
## Structure in Python
### if...else and if... elif...else
```Python
a = int(input("Enter a number:"))
if a == 0:
    print("Zero")
elif a > 0:
    print(f"{a} is a positive number")
else:
    print("Negative number")
```
### Iteration in Python
- **For loop**\: `for i in collection:`
  - Example\:
    ```Python
    sinh_vien = ["Sinh viên trường Y", "Sinh viên trường Luật", "Sinh viên trường Kỹ thuật"]
    for sv in sinh_vien:
      print(sv)               #Sinh viên trường Y
                              #Sinh viên trường Luật
                              #Sinh viên trường Kỹ thuật
    ```
  - Using `range(start, stop, step)`
    ```Python
    for x in range(1, 4, 2):
      print(x)                #1
                              #3
    ```
- **while loop**\: similarly
## List in Python
- **Initialization\:**
  - Using `list()` function
  - Using `[]`
    ```Python
    my_list1 = list((1, 2, 3))
    print(my_list1)             # [1, 2, 3]
    my_list2 = [1, 2, 3]
    print(my_list2)             # [1, 2, 3]

    my_list3 = [300, "Python", 500.5]
    print(my_list3)             # [300, 'Python', 500.5]

    my_list4 = list()
    print(my_list4)             # []
    vi_du = []
    print(vi_du)                # []
    ```
- The length of list\: Using `len()` function
```Python
my_list = [100, 200, "Python"]
print(len(my_list))             # 3
```
- **Index accessment**
  ![alt text](image-4.png)
- **List slicing**\: general case `listname[start_index : end_index : step]`
  - None of those parameters is mandatory
  - For example\:
    ```Python
    vidu_list=[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    print(vidu_list[2:6:2])     # [2, 4]
    print(vidu_list[0:8:3])     # [0, 3, 6]
    print(vidu_list[:5:2])      # [0, 2, 4]
    print(vidu_list[:5:-2])     # [9, 7]
    print(vidu_list[5::2])      # [5, 7, 9]
    print(vidu_list[5::-2])     # [5, 3, 1]
    print(vidu_list[::2])       # [0, 2, 4, 6]
    print(vidu_list[::-2])      # [9, 7, 5, 3, 1]
    print(vidu_list[::])        # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    print(vidu_list[:5])        # [0, 1, 2, 3, 4]
    print(vidu_list[5:])        # [5, 6, 7, 8, 9]
    ```
- **Change list's elements**
  ```Python
    vi_du2 = [50, 100, 200, 300, 400]
    print(vi_du2)               # [50, 100, 200, 300, 400]
    vi_du2[4] = 500
    print(vi_du2)               # [50, 100, 200, 300, 500]
    vi_du2[0:2] = [90, 150]
    print(vi_du2)               # [90, 150, 200, 300, 500]
  ```
- **Add list's elements**
  - Using `+` operator\: connect 2 or more lists
  - Using `append(a)` to add `a` to the tail of the list
  - Using `insert(position, value)` to add `value` to the specified position
  - Using `extend(a, b, c,...)` to add multiple value to the tail of the list
- **Eliminate list's elements**
  ![alt text](image-5.png)
- **Find element in list**
  - `in`\: if an element is in the list, it return true, else false
  - `not in`\: if an element is not in the list, it return true, else false
- **Sort**\: `list.sort(key=..., reverse=...)`
  - `key`\: a particular sorting function
  - `reverse = True`\: descendent sort
  - `reverse = False`\: ascendent sort
- **Reverse**\: `mylist.reverse()`
- **Max/min in list**\:`max(list)` and `min(list)`
- **Sum of list**\: `sum(list)`
- **Count element's apppearance**\: `list.count(a)`
- **Copy list**\:
  - Using assignment\: 
   ```Python
    my_list1 = [1, 2, 3]
    new_list = my_list1

    print(new_list)             # [1, 2, 3]
    my_list1.append(4)
    print(my_list1)             # [1, 2, 3, 4]
    print(new_list)             # [1, 2, 3, 4]
   ```
  - Using `copy()`\:
    ```Python
    my_list1 = [1, 2, 3]
    new_list = my_list1.copy()

    print(new_list)             # [1, 2, 3]
    my_list1.append(4)

    print(my_list1)             # [1, 2, 3, 4]
    print(new_list)             # [1, 2, 3]
    ```
- `any()`\:
  ![alt text](image-6.png)
- `all()`\:
  ![alt text](image-7.png)
## Tuple
- Similar to `list` but it is unchangable
- However if elements in tuple are changable data types such as list, they can be changed
- Another way to change a tuple is type conversion to `list`. After change, the list can also be converted into tuple back again
- **Initialization\:**
  - Using`()` or `tuple()` \:
    ```Python
    number_tuple = (11, 22, 21.25)
    print(number_tuple)                                         #(11, 22, 21.25)
    sample_tuple = tuple(('Python', 10, 23.15, [15, 18]))       #('Python', 10, 23.15, [15, 18])
    print(sample_tuple)
    ```
- Length of tuple\:
  ```Python
  tuple_sample = (1,2,3, "Học","Python", "TEK4.VN", [4,5,6])
  print(len(tuple_sample))                                      #7
  ```
- **Tuple expansion**\: Using `+` operator
- **Finding an element in tuple**\: Using `index(item, [start, end])` method
  ```Python
  tuple_1 = (1, 2, 3, 4, 5)
  tuple_2 = (3, 4, 5, 6, 7)
  tuple_3 = tuple_1 + tuple_2
  print(tuple_3)                                                #(1, 2, 3, 4, 5, 3, 4, 5, 6, 7)
  tuple_3.index(3,[0,5])                                        # 2
  ```
  - `index()` method just returns the index of the item it meets **the first**#   P y t h o n  
 