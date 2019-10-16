
## OOPS in A Python
A minimalistic Python Class




```python
class Person:
    pass

p = Person()
print(type(p))
```

    <class '__main__.Person'>
    

### Let's us define one Person Class


```python
class Person:
    #Class Variable, common for all objects of the same class
    nationality = "Indian"
    
    def __init__(self,pname,clg):
        self.name = pname
        self.college = clg
    
    def sayHi(self,name):
        print("Hello "+name)
        
    def __secretMethod(self):
        print("In Secret Method of ",self.name)
    
    def introduce(self):
        print("My Name is ",self.name)
        print("I am from ",self.college)
        print("I am ",self.nationality)
        self.__secretMethod()
        
        
p = Person("Prateek","Coding Blocks")
p.sayHi("World!")
p.introduce()
#p.__secretMethod()

p2 = Person("Arnav","Micromax")
p2.introduce()


```

    Hello World!
    My Name is  Prateek
    I am from  Coding Blocks
    I am  Indian
    In Secret Method of  Prateek
    My Name is  Arnav
    I am from  Micromax
    I am  Indian
    In Secret Method of  Arnav
    

### Instance Variables vs Class Variables


```python
class Dog:
    
    color = "Brown"
    #Common for all data member of the class 
  
    def __init__(self,breed):
        """This method accepts the breed of the dog and initialsies it"""
        self.activities = []
        self.breed = breed
    
    def addActivity(self,act):
        self.activities.append(act)
        
    def __secretActivity(self):
        print("Doing Secret Activity ",self.breed)
        
    def doActivity(self):
        """This is reg dog activities"""
        print(self.breed)
        print(self.activities)
        self.__secretActivity()
        
        
d1 = Dog("German Shepherd")
d2 = Dog("Golden Retriever")

d1.addActivity("HighJump")
d1.addActivity("Roll Over")
#d1.__secretActivity()

d2.addActivity("LowJump")
d2.addActivity("Roll Upside Down")
#d2.__secretActivity()
d1.doActivity()
d2.doActivity()

d2.doActivity?


```

    German Shepherd
    ['HighJump', 'Roll Over']
    Doing Secret Activity  German Shepherd
    Golden Retriever
    ['LowJump', 'Roll Upside Down']
    Doing Secret Activity  Golden Retriever
    

### Public vs Private method

### Inheritance in Python


```python
class SchoolMember:
    def __init__(self,name,age):
        self.name = name
        self.age = age
        print("Init School Member: %s "%self.name)
        
    def introduce(self):
        print("Name :%s %d"%(self.name,self.age))
        

class Teacher(SchoolMember):
       
        def __init__(self,name,age,salary):
            SchoolMember.__init__(self,name,age)
            self.salary = salary
            print("Init Teacher : %s"%self.name)

        def introduce(self):
            SchoolMember.introduce(self)
            print("Salary : %d"%(self.salary))
            
class Student(SchoolMember):
    '''Represents a school student'''
    def __init__(self,name,age,marks):
        SchoolMember.__init__(self,name,age)
        self.marks = marks
        print("Init Student %s"%(self.name))
        
    def introduce(self):
        SchoolMember.introduce(self)
        print("Marks %d"%(self.marks))
    

t = Teacher("Mr.Alpha",30,45000)
t.introduce()

s = Student("Xyz",20,90)
s.introduce()

```

    Init School Member: Mr.Alpha 
    Init Teacher : Mr.Alpha
    Name :Mr.Alpha 30
    Salary : 45000
    Init School Member: Xyz 
    Init Student Xyz
    Name :Xyz 20
    Marks 90
    
