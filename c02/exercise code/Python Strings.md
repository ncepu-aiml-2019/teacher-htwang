
### Strings and BuiltIn Methods


```python
a = "Coding Blocks"
print(a)

```

    Coding Blocks
    


```python
print(a[2])
```

    d
    


```python
print(a[-1])
```

    s
    


```python
print(len(a))
```

    13
    


```python
# Strings are Not Mutable!
a = "Code Blocks"
print(a)
```

    Code Blocks
    


```python
for i in range(len(a)):
    print(a[i])
```

    C
    o
    d
    e
     
    B
    l
    o
    c
    k
    s
    


```python
for c in a:
    print(c)
```

    C
    o
    d
    e
     
    B
    l
    o
    c
    k
    s
    

### Working with Strings


```python
a = "Mango"
b = "Juice"
print(a + b)
```

    MangoJuice
    


```python
print(a*5)
```

    MangoMangoMangoMangoMango
    


```python
# Range Slicing 
a[1:-2]
a[ : ]
a[-2:]
a[1:3]
```




    'an'




```python
# Membership - Substring is present in bigger string
a = "Coding Blocks"
b = "Code"
if b not in a:
    print("Yes")
else:
    print("No")

    #'go' in a

```

    Yes
    


```python
# String Formating 
print("My favourite fruit is %s and it comes from %c"%("Mango","I"))
```

    My favourite fruit is Mango and it comes from I
    


```python
# Triple Quotes
para = """This is some
paragram written
here"""
print(para)
```

    This is some
    paragram written
    here
    

### Strings : More Inbuilt Functions


```python
l = para.split()
print(l)
print(type(l))
print(type(l[0]))
```

    ['This', 'is', 'some', 'paragram', 'written', 'here']
    <class 'list'>
    <class 'str'>
    


```python
para.splitlines()
```




    ['This is some', 'paragram written', 'here']




```python
fruit = "Mango"
fruit = fruit.upper()
fruit = fruit.lower()
print(fruit)
```

    mango
    


```python
shake = "    Apple Shake   "
shake2 = shake
print(len(shake))
```

    18
    


```python
shake = shake.lstrip() #Removes the leading white space
shake = shake.rstrip() #Removes the ending white space
print(shake)
print(len(shake))
```

    Apple Shake
    11
    


```python
shake2 = shake2.strip() #Removes leading and trailing whites spaces 
print(shake2)
print(len(shake2))
```

    Apple Shake
    11
    


```python
a = "9318790"
a.isdigit()
```




    True




```python
a = "HNo"
a.isalpha()
```




    True




```python
a = "12abcA"
b = "    "
print(a.isalnum())
print(a.islower())
print(b.isspace()) 
```

    True
    False
    True
    

### Some More String Functions :)
- Find Function
- Replace
- Count Function
- Join Function
- Title Function
- Capitalize


```python
a = "I love having Apple Juice, and I like eat green Apple"
print(a.find("Apple",30,len(a)))

print(a.index("Apple",30,len(a)))
# Difference is find() return -1, index throws an exception
```

    48
    48
    


```python
a = a.replace("Apple","Mango")
print(a)

```

    I love having Mango Juice, and I like eat green Mango
    


```python
a.count("Mango")
```




    2




```python
l = a.split()
print(l)
```

    ['I', 'love', 'having', 'Mango', 'Juice,', 'and', 'I', 'like', 'eat', 'green', 'Mango']
    


```python
b = "_"
b = b.join(l)
print(b)
```

    I_love_having_Mango_Juice,_and_I_like_eat_green_Mango
    


```python
name_org = "coding blocks"
name_org.title()
```




    'Coding Blocks'


