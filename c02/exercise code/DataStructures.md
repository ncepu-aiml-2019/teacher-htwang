
## Tuples in Python


```python
t = (1,2,3,"Hello")
print(t)
```

    (1, 2, 3, 'Hello')
    


```python
#tuples are immutable
#t[0] = 5
print(t[0])
```

    1
    


```python
# Convert a tuple into a list

l = list(t)
print(l)

l[0] = 5
print(l)
```

    [1, 2, 3, 'Hello']
    [5, 2, 3, 'Hello']
    


```python
t2 = tuple(l)
print(t2)
```

    (5, 2, 3, 'Hello')
    


```python
#concatentation
print(t2 + t)

#Repetion
t2 = t2*3
print(t2)
```

    (5, 2, 3, 'Hello', 1, 2, 3, 'Hello')
    (5, 2, 3, 'Hello', 5, 2, 3, 'Hello', 5, 2, 3, 'Hello')
    


```python
t = (1,44,3,2)
print(min(t))
```

    1
    


```python
del t
```

## Dictionaries in Python


```python
d = {"Mango":100,"Apple":80}
print(d)
#Look Up
print(d["Mango"])

d["Guava"] = 60
print(d)

d["Grape"] = [10,20]
print(d["Grape"])

d["Pineapple"] = {"Small":90,"Large":150}

print(d["Pineapple"]["Small"])

```

    {'Mango': 100, 'Apple': 80}
    100
    {'Mango': 100, 'Apple': 80, 'Guava': 60}
    [10, 20]
    90
    


```python
print(d.keys())
```

    dict_keys(['Mango', 'Apple', 'Guava', 'Grape', 'Pineapple'])
    


```python
print(d.values())
```

    dict_values([100, 80, 60, [10, 20], {'Small': 90, 'Large': 150}])
    


```python
print(type(d.get("Mangoes")))
```

    <class 'NoneType'>
    


```python
if "Mangoes" in d:
    print("Price of Mango is %d"%(d["Mango"]))
else:
    print("Doesn't exist")




```

    Doesn't exist
    


```python
del d["Pineapple"]
l = list(d.items())
print(l)
```

    [('Mango', 100), ('Apple', 80), ('Guava', 60), ('Grape', [10, 20])]
    


```python
d2 = {"Strawberry":95}

d.update(d2)
print(d)

```

    {'Mango': 100, 'Apple': 80, 'Guava': 60, 'Grape': [10, 20], 'Strawberry': 95}
    


```python
print(len(d))
```

    5
    


```python
d.clear()
print(len(d))
```

    0
    


```python
l1 = ["Apple","Papaya","Guava","Banana"]
l2 = [100,120,30,50]

p = dict(zip(l1,l2))
print(p)
print(type(p))

```

    {'Apple': 100, 'Papaya': 120, 'Guava': 30, 'Banana': 50}
    <class 'dict'>
    


```python
for k in p.values():
    print(k)
```

    100
    120
    30
    50
    

### Python Sets


```python
s = set([15,1,2,3,4,3,1,1])
print(s)
```

    {1, 2, 3, 4, 15}
    


```python
if 14 in s:
    print("present")
else:
    print("not present")
```

    not present
    


```python
s2 = {5,6,11,1,1}
print(s2)
```

    {1, 11, 5, 6}
    


```python
s2.add(50)
print(s2)


```

    {1, 5, 6, 11, 50}
    




    {1, 2, 3, 4, 5, 6, 11, 15, 50}




```python
s.clear()
```


```python
a1 = {1,2,3,4}
a2 = {2,3,4,5,6}

#Those element which are only in one of the sets
print(a1^a2)



```

    {1, 5, 6}
    
