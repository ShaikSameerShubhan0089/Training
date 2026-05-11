# OOP Notes in Python

Using one single metaphor end to end: `Cars`

---

# 1. What is OOP?

OOP means `Object-Oriented Programming`.

It is a way of writing programs by thinking in terms of:
- objects
- properties
- behavior

Instead of thinking only about variables and functions separately, we group related data and actions together.

---

# 2. Car Metaphor for Everything

We will use only one idea for all topics:

Think of a `car`.

A car has:
- data
  - color
  - brand
  - speed
  - fuel type
- behavior
  - start
  - stop
  - accelerate
  - brake

In OOP:
- the `design` of a car is called a `class`
- a `real car` made from that design is called an `object`

---

# 3. Class

## What is a class?

A class is a blueprint or design.

It tells us:
- what data an object should have
- what actions an object should perform

## Car example

A car company first creates a design.
That design is not one real car.
It is only a plan.

In Python, that plan is a `class`.

## Code
```python
class Car:
    pass
```

## Meaning
- `class` is the keyword
- `Car` is the class name
- `pass` means "nothing written yet"

---

# 4. Object

## What is an object?

An object is a real instance created from a class.

If `Car` is the design, then:
- one red car
- one blue car
- one electric car

These are all objects.

## Code
```python
class Car:
    pass

car1 = Car()
car2 = Car()
```

## Meaning
- `car1` and `car2` are objects
- both are created from `Car`

---

# 5. Attributes

## What are attributes?

Attributes are variables that belong to an object.

For a car, attributes can be:
- brand
- color
- speed

## Code
```python
class Car:
    pass

car1 = Car()
car1.brand = "Toyota"
car1.color = "Red"
car1.speed = 120

print(car1.brand)
print(car1.color)
print(car1.speed)
```

## Output
```python
Toyota
Red
120
```

## Car understanding
Here, `car1` is one real car.
Its details are stored as attributes.

---

# 6. Methods

## What are methods?

Methods are functions written inside a class.

They describe what an object can do.

For a car:
- start
- stop
- accelerate

## Code
```python
class Car:
    def start(self):
        print("Car is starting")

    def stop(self):
        print("Car is stopping")

car1 = Car()
car1.start()
car1.stop()
```

## Output
```python
Car is starting
Car is stopping
```

## Car understanding
The car not only has data, it also performs actions.

---

# 7. `self`

## What is `self`?

`self` means:
"this current object"

If many cars exist, `self` helps Python know which car we are talking about.

## Car idea
Suppose:
- `car1` is red
- `car2` is blue

When `car1.start()` runs, Python should know it is `car1` starting, not `car2`.
That is why `self` is used.

## Code
```python
class Car:
    def show_details(self):
        print(self.brand, self.color)

car1 = Car()
car1.brand = "Toyota"
car1.color = "Red"

car1.show_details()
```

## Output
```python
Toyota Red
```

## Important point
`self` is not a keyword like `class` or `def`.
It is a naming convention, but almost everyone uses `self`.

---

# 8. Constructor: `__init__`

## What is a constructor?

A constructor is a special method that runs automatically when an object is created.

In Python, the constructor is:
```python
__init__
```

## Why do we use it?

To give values to a car as soon as it is created.

Without constructor:
- create car
- then assign brand
- then assign color
- then assign speed

With constructor:
- everything is assigned immediately

## Code
```python
class Car:
    def __init__(self, brand, color, speed):
        self.brand = brand
        self.color = color
        self.speed = speed

car1 = Car("Toyota", "Red", 120)
car2 = Car("Honda", "Blue", 100)

print(car1.brand, car1.color, car1.speed)
print(car2.brand, car2.color, car2.speed)
```

## Output
```python
Toyota Red 120
Honda Blue 100
```

## Car understanding
The moment the car is created, its important details are already set.

---

# 9. Instance Variables

## What are instance variables?

These are variables that belong to each object separately.

Each car can have its own:
- brand
- color
- speed

## Code
```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

car1 = Car("Toyota", "Red")
car2 = Car("Honda", "Black")

print(car1.brand)
print(car2.brand)
```

## Output
```python
Toyota
Honda
```

## Car understanding
Every car has its own personal details.

---

# 10. Class Variables

## What are class variables?

These are variables shared by all objects of the class.

## Car idea
Suppose all cars in one training example have:
- 4 wheels

That does not need to be stored separately for every car.

## Code
```python
class Car:
    wheels = 4

    def __init__(self, brand):
        self.brand = brand

car1 = Car("Toyota")
car2 = Car("Honda")

print(car1.wheels)
print(car2.wheels)
print(Car.wheels)
```

## Output
```python
4
4
4
```

## Difference

| Type | Belongs to |
|---|---|
| Instance variable | one car |
| Class variable | all cars |

---

# 11. Encapsulation

## What is encapsulation?

Encapsulation means:
- keeping data and methods together
- controlling access to internal data

## Car idea
When driving a car:
- you press accelerator
- you press brake

You do not directly control every small engine part.

The complex internal work is hidden.

That is the idea of encapsulation.

## Code
```python
class Car:
    def __init__(self, brand, speed):
        self.brand = brand
        self.__speed = speed

    def show_speed(self):
        print("Speed:", self.__speed)

car1 = Car("Toyota", 120)
car1.show_speed()
```

## Output
```python
Speed: 120
```

## Important point
`__speed` uses double underscore.
It shows that this data is meant to be internal.

## Car understanding
We do not want everyone to directly change important internal parts carelessly.

---

# 12. Abstraction

## What is abstraction?

Abstraction means:
- showing only important details
- hiding unnecessary internal details

## Car idea
To drive a car, you need to know:
- steering
- brake
- accelerator

You do not need to know:
- exact engine combustion process
- wiring of every sensor

That is abstraction.

## Simple understanding
- user sees only what is necessary
- system hides internal complexity

## Code idea
```python
class Car:
    def start(self):
        print("Car started")
```

A user just calls `start()`.
The internal engine process is hidden.

---

# 13. Inheritance

## What is inheritance?

Inheritance means one class can use features of another class.

## Car idea
Suppose we have a general `Car`.
Now we create:
- `ElectricCar`
- `SportsCar`

These are still cars.
So they can reuse the features of `Car`.

## Code
```python
class Car:
    def start(self):
        print("Car is starting")

class ElectricCar(Car):
    pass

e1 = ElectricCar()
e1.start()
```

## Output
```python
Car is starting
```

## Car understanding
`ElectricCar` inherits from `Car`.
So it can use the `start()` method.

---

# 14. Method Overriding

## What is method overriding?

Method overriding means a child class gives its own version of a method already present in the parent class.

## Car idea
A normal car and an electric car may both "start", but the behavior can be different.

## Code
```python
class Car:
    def start(self):
        print("Car uses general start process")

class ElectricCar(Car):
    def start(self):
        print("Electric car starts silently")

car1 = Car()
e1 = ElectricCar()

car1.start()
e1.start()
```

## Output
```python
Car uses general start process
Electric car starts silently
```

## Car understanding
Same method name.
Different behavior.

---

# 15. `super()`

## What is `super()`?

`super()` is used to access parent class methods or constructor.

## Car idea
Suppose `ElectricCar` wants to reuse basic car setup, then add battery details.

## Code
```python
class Car:
    def __init__(self, brand):
        self.brand = brand

class ElectricCar(Car):
    def __init__(self, brand, battery):
        super().__init__(brand)
        self.battery = battery

e1 = ElectricCar("Tesla", "75 kWh")
print(e1.brand)
print(e1.battery)
```

## Output
```python
Tesla
75 kWh
```

## Car understanding
Parent setup is reused instead of rewritten.

---

# 16. Polymorphism

## What is polymorphism?

Polymorphism means:
"same method name, different behavior"

## Car idea
Different types of cars may respond differently to the same action `start()`.

## Code
```python
class Car:
    def start(self):
        print("General car start")

class ElectricCar(Car):
    def start(self):
        print("Electric start")

class SportsCar(Car):
    def start(self):
        print("Sports car roaring start")

cars = [Car(), ElectricCar(), SportsCar()]

for c in cars:
    c.start()
```

## Output
```python
General car start
Electric start
Sports car roaring start
```

## Car understanding
Same method:
- `start()`

Different outputs depending on the object.

---

# 17. Access Modifiers in Python Style

Python does not enforce access modifiers exactly like some other languages, but we usually use naming style:

## Public
Normal variable
```python
speed
```

## Protected-like convention
Single underscore
```python
_speed
```

## Private-like convention
Double underscore
```python
__speed
```

## Car idea
- public: speed visible normally
- protected-like: internal use warning
- private-like: strongly intended to stay inside the class

---

# 18. Getter and Setter

## Why use them?

Sometimes we do not want direct uncontrolled access to car data.

For example:
- speed should not become negative

## Code
```python
class Car:
    def __init__(self, speed):
        self.__speed = speed

    def get_speed(self):
        return self.__speed

    def set_speed(self, speed):
        if speed >= 0:
            self.__speed = speed
        else:
            print("Invalid speed")

car1 = Car(100)
print(car1.get_speed())

car1.set_speed(150)
print(car1.get_speed())

car1.set_speed(-20)
```

## Output
```python
100
150
Invalid speed
```

## Car understanding
The car's speed is controlled safely.

---

# 19. Types of Inheritance

We can still explain all with cars.

## 1. Single Inheritance
One child from one parent

```python
class Car:
    pass

class ElectricCar(Car):
    pass
```

## 2. Multilevel Inheritance
One child from another child

```python
class Car:
    pass

class ElectricCar(Car):
    pass

class SelfDrivingElectricCar(ElectricCar):
    pass
```

## 3. Hierarchical Inheritance
Many child classes from one parent

```python
class Car:
    pass

class ElectricCar(Car):
    pass

class SportsCar(Car):
    pass
```

## 4. Multiple Inheritance
One class inherits from more than one class

## Car example
A smart car may use features from:
- `Car`
- `LuxuryFeatures`

```python
class Car:
    pass

class LuxuryFeatures:
    pass

class SmartCar(Car, LuxuryFeatures):
    pass
```

---

# 20. Method Resolution Order (MRO)

## What is MRO?

If multiple inheritance exists, Python needs to know:
- from which parent to take the method first

That order is called MRO.

## Code
```python
class Car:
    def show(self):
        print("Car")

class LuxuryFeatures:
    def show(self):
        print("Luxury")

class SmartCar(Car, LuxuryFeatures):
    pass

s1 = SmartCar()
s1.show()
```

## Output
```python
Car
```

## Why?

Because Python checks parents in order written:
```python
class SmartCar(Car, LuxuryFeatures):
```

First `Car`, then `LuxuryFeatures`.

---

# 21. Composition

## What is composition?

Composition means one object contains another object as a part.

## Car idea
A car has:
- engine
- tyres
- battery

The car is made of these parts.

## Code
```python
class Engine:
    def start(self):
        print("Engine starts")

class Car:
    def __init__(self):
        self.engine = Engine()

    def start_car(self):
        self.engine.start()
        print("Car starts moving")

car1 = Car()
car1.start_car()
```

## Output
```python
Engine starts
Car starts moving
```

## Car understanding
Car is not inheriting from engine.
Car contains an engine.

This is composition.

---

# 22. Association

## What is association?

Association means two objects are connected, but one is not fully part of the other.

## Car idea
A `Driver` uses a `Car`.

Driver and car are related, but driver is not a part inside the car class structure like engine.

## Code
```python
class Car:
    def __init__(self, brand):
        self.brand = brand

class Driver:
    def __init__(self, name, car):
        self.name = name
        self.car = car

car1 = Car("Toyota")
driver1 = Driver("Rahul", car1)

print(driver1.name, "drives", driver1.car.brand)
```

## Output
```python
Rahul drives Toyota
```

---

# 23. Aggregation

## What is aggregation?

Aggregation is a weaker form of relationship.
One object uses another, but both can exist separately.

## Car idea
A service center works with many cars.
Cars can exist without the service center.
The service center can also exist without one specific car.

## Code
```python
class Car:
    def __init__(self, brand):
        self.brand = brand

class ServiceCenter:
    def __init__(self, name):
        self.name = name

    def service_car(self, car):
        print(self.name, "is servicing", car.brand)

car1 = Car("Honda")
center1 = ServiceCenter("FastFix")
center1.service_car(car1)
```

## Output
```python
FastFix is servicing Honda
```

---

# 24. Why OOP is Useful

Using the car idea, OOP helps us:

## 1. Organize code better
All car-related data and methods stay together.

## 2. Reuse code
`ElectricCar` can reuse `Car`.

## 3. Reduce repetition
Common logic stays in parent class.

## 4. Make programs more realistic
Real-world things like cars, drivers, engines are easier to model.

## 5. Improve readability
The code becomes easier to understand and maintain.

---

# 25. OOP Interview Quick Revision

## Class
Blueprint of a car

## Object
Real car made from blueprint

## Attribute
Car data like brand, color, speed

## Method
Car action like start, stop

## Constructor
Initial setup when car is created

## Inheritance
Electric car using features of car

## Polymorphism
Different cars responding differently to `start()`

## Encapsulation
Protecting internal car data

## Abstraction
Showing only useful controls, hiding engine complexity

## Composition
Car has an engine

---

# 26. Common Mistakes Students Make

## 1. Forgetting `self`
If method belongs to object, `self` is needed.

## 2. Confusing class and object
- class = design
- object = real car

## 3. Not using constructor when needed
Then initialization becomes messy.

## 4. Thinking inheritance means copy-paste
Inheritance is reuse through relationship, not manual duplication.

## 5. Confusing composition and inheritance
- inheritance = is-a
- composition = has-a

With cars:
- ElectricCar is a Car
- Car has an Engine

---

# 27. One Full Mini Example

```python
class Car:
    wheels = 4

    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

    def start(self):
        print(self.brand, "car is starting")

    def show_details(self):
        print("Brand:", self.brand)
        print("Color:", self.color)
        print("Wheels:", Car.wheels)

class ElectricCar(Car):
    def __init__(self, brand, color, battery):
        super().__init__(brand, color)
        self.battery = battery

    def start(self):
        print(self.brand, "electric car starts silently")

    def show_battery(self):
        print("Battery:", self.battery)

car1 = Car("Toyota", "Red")
car2 = ElectricCar("Tesla", "White", "75 kWh")

car1.start()
car1.show_details()

car2.start()
car2.show_details()
car2.show_battery()
```

## Output
```python
Toyota car is starting
Brand: Toyota
Color: Red
Wheels: 4
Tesla electric car starts silently
Brand: Tesla
Color: White
Wheels: 4
Battery: 75 kWh
```

---

# 28. Final Summary Using Only Cars

- A `class` is the design of a car
- An `object` is a real car
- `attributes` are car details
- `methods` are car actions
- `self` means current car
- `__init__` sets up the car when created
- `inheritance` means one type of car using another car design
- `polymorphism` means different cars behave differently with same method
- `encapsulation` protects car internals
- `abstraction` hides complex engine details
- `composition` means car has engine
- `association` means driver uses car

---

# 29. Quick Practice Questions

1. What is the difference between a class and an object using the car example?
2. Why do we use `self`?
3. What is the role of `__init__`?
4. Why is `ElectricCar` an example of inheritance?
5. Why is `Engine` inside `Car` an example of composition?
6. What is the difference between instance variable and class variable?
7. What is method overriding?
8. Why do we use `super()`?
9. What is polymorphism using `start()` method?
10. Why is abstraction useful in a car system?

