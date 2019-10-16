
## Data Structures in Python
### Builtin Datatypes
- Strings
- Lists
- Tuples
- Dictionaries
- Sets

## Lists

- List is like array, heterogenous list


```python
myList = [ 1,2,3.5,"Hello"]
print(myList)
print(type(myList))
```

    [1, 2, 3.5, 'Hello']
    <class 'list'>
    


```python
l2 = list([1,2,3])
print(l2)
print(type(l2))
```

    [1, 2, 3]
    <class 'list'>
    


```python
l3 = list(l2)
print(l3)

l3 = l3 + l2
print(l3)

l3.extend(l2)
print(l3)
```

    [1, 2, 3]
    [1, 2, 3, 1, 2, 3]
    [1, 2, 3, 1, 2, 3, 1, 2, 3]
    


```python
# List of Square of the numbers from 1 to 5
l4 = [i*i for i in range(1,6)]
print(l4)
```

    [1, 4, 9, 16, 25]
    

## List Slicing




```python
print(l4[0:3])
print(l4[-3:])
```

    [1, 4, 9]
    [9, 16, 25]
    

## Insertion and Deletion 
- append
- insert

- remove
- pop
- del 


```python
l = [1,2]
l.append(3)

l.append([1.0,2.1])
l += [4,5,6]
print(l)

```

    [1, 2, 3, [1.0, 2.1], 4, 5, 6]
    


```python
l.insert(2,20)
print(l)
```

    [1, 2, 20, 20, 20, 3, [1.0, 2.1], 4, 5, 6]
    


```python
print(l[3][1])
```

    2.1
    


```python
del l[0]
print(l)
```

    [3, [1.0, 2.1], 4, 5, 6]
    


```python
l.pop()
print(l)
```

    [3, [1.0, 2.1], 4]
    


```python
l = ([1,2,3])
l = l*4
print(l)
```

    [1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3]
    


```python
l = ["Apple","mango","guava",80]
80 in l
```




    True




```python
for i in range(len(l)):
    print(l[i])
```

    Apple
    mango
    guava
    80
    


```python
for x in l:
    print(x)
```

    Apple
    mango
    guava
    80
    

## More functions on lists  : Searching & Sorting


```python
l = [4,3,2,16,18]
print(max(l))
print(min(l))
#Linear Search 
print(l.index(16))

```

    18
    2
    3
    


```python
l = sorted(l)
```


```python
print(l)
```

    [2, 3, 4, 16, 18]
    


```python
l = [4,5,1,3,2]
l.sort(reverse=True)
print(l)
```

    [5, 4, 3, 2, 1]
    


```python
## Read a list of Numbers
numbers = [int(number)*int(number) for number in input().split()]
print(numbers)
print(type(numbers))

```

    1 2 3 4 
    [1, 4, 9, 16]
    <class 'list'>
    
