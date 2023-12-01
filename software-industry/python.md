# Learning Python

> Programming requires patience.

If you already know other programming languages, then [Python](https://www.python.org/) is trivial to learn. Otherwise start here. 

See also [domain modelling](../domain-modelling).

[toc]

## Resources

Beginner

- https://www.learnpython.org/



Advanced

- [Design patterns](https://refactoring.guru/design-patterns/python)
- [Concurrency](https://www.youtube.com/watch?v=9zinZmE3Ogk&t=1375s)



## Topics

### Computational Thinking

How to translate natural language to a computer language. How to define problems in an abstract way.

See [domain driven design](../domain-modelling/domain-driven-design.md).



```python
# math
print(2 * 2)
print(4 * 4)
```



### Variables

See [datatypes](https://docs.python.org/3/library/datatypes.html).

Variables

```python
length = 10 # meter
duration = 2 # second
velocity = length / float(duration) # m/s
print('The velocity is:', velocity)
```



### Conditions

```python
if velocity > 1:
  print('fast')
else:
  print('slow')
```



### Loops & Functions



```python
# define a function
def add(a: int, b: int):
  """Returns the sum of a and b
  """
  return a + b

# repeatedly execute the function
for i in '1234':
	print(add(2, 4))
  if i == '2':
    break
```



### Datastructures

```python
# standard datatypes
grouped_data: set = {0, 'e'}
mapped_data: dict = {'x': 10, 'y': 20}
ordered_data: list = [1, 2, 3]

# pattern matching
x, y = ('10 meter', '5 meter')
head, *tail = [1, 2, 3, 4]
```



### Dataclasses

[Dataclasses](https://docs.python.org/3/library/dataclasses.html)

```python
@dataclass
class Trajectory:
    length: float
    duration: float

    @property
    def velocity(self) -> float:
        return self.length / float(self.duration)

x = Trajectory(2, 8)
print(x)
print(x.velocity
```



### Classes

```python
# a statefull object
class Object
    def __init__(self):
        self.position = 0

    def move(self, distance: float):
        self.position += distance

x = Object()
x.move(10), x.move(2)
print(x.position)
```



