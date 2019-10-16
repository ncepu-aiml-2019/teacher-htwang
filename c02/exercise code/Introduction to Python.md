
### Python Basics
    - Hello World
    - Variables 


```python
print("Hello World")
```

    Hello World
    


```python
a = 10
b = 10.5

print(a)
print(b)
```

    10
    10.5
    


```python
print(type(a))
print(type(b))
```

    <class 'int'>
    <class 'float'>
    


```python
c = "hello_python"
print(type(c))
```

    <class 'str'>
    


```python
d = 5 + 3j
print(d)
print(type(d))
```

    (5+3j)
    <class 'complex'>
    


```python
a = 100.5

```


```python
print(a)
print(type(a))
```

    100.5
    <class 'float'>
    

## Working with Input


```python
name = input("Enter the name of your organisation")
print("Hello",end=' ')
print(name)
```

    Enter the name of your organisationCoding Blocks
    Hello Coding Blocks
    

## Reading Numbers | Typecasting


```python
a = float(input("Enter a Number"))
print(a)
print(a*a)

print(type(a))
print("The square of the number is " + str(a*a))
```

    Enter a Number6.60
    6.6
    43.559999999999995
    <class 'float'>
    The square of the number is 43.559999999999995
    

## More about the Print Function

- format 
- end and sep


```python
print("Hello","World","I","Love","Python",sep="+")
```

    Hello+World+I+Love+Python
    


```python
a = 10
b = 20
print(a,end=',')
print(b)
```

    10,20
    


```python
a = "Indians"
b = "Mangoes"

c = "Russians"
d = "Pizza"
```


```python
print("{0} love {1}".format(c,d))
```

    Russians love Pizza
    


```python
a = 10
b = 20

print("You entered %d and %d and %d"%(a,b,b))
```

    You entered 10 and 20 and 20
    

### Variables,Datatypes and Operators

A type of identifier.

Rules for naming identifiers:

    The first character of the identifier must be a letter of the alphabet (uppercase ASCII or lowercase ASCII or Unicode character) or an underscore (_).

    The rest of the identifier name can consist of letters (uppercase ASCII or lowercase ASCII or Unicode character), underscores (_) or digits (0-9).

    Identifier names are case-sensitive. For example, myname and myName are not the same. Note the lowercase n in the former and the uppercase N in the latter.

Examples of valid identifier names are i, name_2_3.

Examples of invalid identifier names are 2things, this is spaced out, my-name and >a1b2_c3.

### Airthmetic Operators (+,-,*,**,/,//,%) 




```python
a = 10
b = 21

print(a+b)
print(a-b)
print(a*b)
print("%0.4f"%(a/b))
print(a//b)
#Exponent/Power Function
print(a**b)
print(b%a)



```

    31
    -11
    210
    0.4762
    0
    1000000000000000000000
    1
    

### Multiple Variable Assignment


```python
a,b,c = 10,20,30.34
```


```python
# This functions print the variables
print(a,b,c)
```

    10 20 30.34
    

### Whitespaces and Indendation


- Whitespace is important in Python.

- Actually, whitespace at the beginning of the line is important. This is called indentation.

- Leading whitespace (spaces and tabs) at the beginning of the logical line is used to determine the indentation level of the logical line, which in turn is used to determine the grouping of statements.

- This means that statements which go together must have the same indentation. Each such set of statements is called a block

### Don't mix tabs and Spaces
### Comments are Important for readability of your code


```python

# This is a single comment !

"""This is a 
multiline 
comment """

myString = """This is 
a multiline string """

print(myString)


```

    This is 
    a multiline string 
    

### Operators - Arithmetic, Comparsion, Compound Assignment, Logical Operators




```python
raining = True
temperature = 30


outing = raining and temperature <= 30
print(outing)


```

    True
    

## If Else Blocks


```python
weather  = input()

if weather=="Rainy":
    print("Don't go outside")
    print("It is raining heavilly")
    
elif weather=="Cool":
    print("Lets play Cricket")

else:
    print("Lets go for shopping")



```

    Rainy
    Don't go outside
    It is raining heavilly
    

### Loops in Python 


```python
n = 10
i = 1

while i<=n:
    print("Step %d"%i)
    i = i + 1

print("Loop Finished")
    
    
```

    Step 1
    Step 2
    Step 3
    Step 4
    Step 5
    Step 6
    Step 7
    Step 8
    Step 9
    Step 10
    Loop Finished
    


```python
for i in range(1,10,2):
    print(i,end=",")
```

    1,3,5,7,9,


```python
no = 10
ans = 1

for i in range(1,11):
    ans *= i
    
print(ans)
```

    3628800
    

## Loops here


```python
for i in range(10,1,-2):
    print(i,end=',')
```

    10,8,6,4,2,


```python
# 5 X 5 Matrix
n = 5
for x in range(n):
    for y in range(n):
        print(max(x+1,y+1,n-x,n-y),end=" ")
    print()

```

    5 5 5 5 5 
    5 4 4 4 5 
    5 4 3 4 5 
    5 4 4 4 5 
    5 5 5 5 5 
    

### Break Continue and Pass Statements


```python
for i in range(1,10):
    if i==5:
        continue
    print(i)

print("Loop ends")
```

    1
    2
    3
    4
    6
    7
    8
    9
    Loop ends
    


```python
# Write a Program which prints all primes number upto N !
```


```python
def helloFact():
    print("Hello Factorial")
    
helloFact()
    
    
```

    Hello Factorial
    


```python
def factorial(n):
    ans = 1
    for i in range(1,n+1):
        ans *= i
    return ans

print(factorial(5))


```

    120
    


```python
def isPrime(n):
    
    for i in range(2,n):
        if(n%i==0):
            return False
        
    return True


def printPrime(V):
    
    for i in range(1,V+1):
        if(isPrime(i)):
            print(i,end=',')
            
            
printPrime(100)
    
```

    1,2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,

## Default Argument Values and Local Global Variables




```python
lang = "C++"
def say(x="Python"):
    print("I Love " +x)
    
say("JavaScript")
say()
print(lang)
```

    I Love JavaScript
    I Love Python
    C++
    

### Recursive Function


```python
def fact(n):
    #Base Case
    if(n==0):
        return 1
    #Rec Case
    return n*fact(n-1)

print(fact(6))
```

    720
    

### Keywords Arguments



```python
def myFunc(score,lang,rollNo):
    print("I scored %d in %s"%(score,lang))
    print(rollNo)
    
    
myFunc(rollNo=1010,lang="Python",score=10)
```

    I scored 10 in Python
    1010
    
