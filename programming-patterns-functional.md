## Functional Programming Patterns

These patterns are often associated with functional programming languages, algebraic type systems and discrete mathematics.

**Syntax**

```haskell
-- function_name : signature
name : Domain -> Codomain

-- e.g.
divideByTwo : Int -> Float
```



#### Special functions

| Name                | Symbol | Code                       |
| ------------------- | ------ | -------------------------- |
| Identity            | I      | `f(x) = x`                 |
| Constant            | K      | `f(x) = a`                 |
| Curry (application) | S      | `S(f, g, x) = f(x, (g(x))` |
| Loop                | Ω      | `f(x) = {x, f(x)}`         |



#### Element-based Patterns

**Values & Variables**
A value is an immutable piece of data. A variable is a reference to a value. A variable can refer to another variable.

Composite values contain multiple entries. E.g. a tuple `(1, 2)`.

**Pure Function**
[Functions](https://en.wikipedia.org/wiki/Pure_function) that are stateless and deterministic. This makes them trivial to parallelize.

`f : A -> B`

*Multivariate* functions are pure functions that depend on multiple inputs. E.g. `sum(1,2) = 3`.

**Partial Function**
A function that is [under-defined](https://wiki.haskell.org/Partial_functions), i.e. it doesn't handle all possible input values. E.g. `GetFirstElement` would break when given an empty sequence.

**Higher Order Function**
A function that takes another function as an input. It uses *partial application*.

`f : (A -> B) -> A -> B `



#### Chain-based Patterns

**Function Composition**
In natural language: apply one function to the result of applying another function to an argument.

`g ∘ f = g( f( x ) )`

**Map**
Apply a function to a sequence of input values. E.g. `map(sqrt, [2,4]) = [1,2]`

**Fold or Reduce**
[Reduce](https://en.wikipedia.org/wiki/Fold_%28higher-order_function%29) a collection of values down to a single element using a [reduction operator](https://en.wikipedia.org/wiki/Reduction_operator). If the operator is associative and commutative then the execution done efficiently in parallel.

E.g. `reduce(sum, [ 1, 2 ]) = 3`

**MapReduce**
[MapReduce](https://en.wikipedia.org/wiki/MapReduce)

```haskell
-- using key-value pairs K1, V1..
map : (K1, V1) > [ (K2, V2) ]
reduce : [V2] -> [C]
```





#### Union Types

##### Multiple Tracks

A function with a union type as domain or codomain. E.g. a function that can fail could have the signature `f : A -> B | Error` .

- This generalizes to `Future` types, where the result is *either* a promise or a value.

In OOP languages functions tend to be able to have an implicit `Exception` return type. E.g. `DivideByZeroError`.



##### Monad

```haskell
-- 1. a type M
type M x = A x | B

-- 2. a return function to convert a value to the monad
wrap : x -> M x

-- 3. a bind or map function
bind : M x -> (x -> M y) -> M y
```

The *bind* function [wraps](https://en.wikipedia.org/wiki/Monad_(functional_programming)) around another function in order make its signature compatible with another function. It serves as an adapter and allows certain functions to be used in a pipeline or chain.

Bind can be used to handle union types. E.g. the `Maybe` or `Option` type. The function `Maybe.apply` can be defined as follows:

```haskell
type Maybe x = Just x | Nothing

Maybe.apply : (A -> Maybe A) -> Maybe A -> Maybe A
Maybe.apply f x =
  case x of
  	Just v -> f v -- standard application of `f` to a value `v`
  	Nothing -> Nothing -- do nothing
```

With a *mapping* function to apply it to multiple values.

```haskell
Maybe.map f values : (A -> Maybe B) -> [ Maybe A ] -> [Maybe B]
Maybe.map f values =
	map (bind f) values
```

Note that this generalizes to an arbitrary number of states. E.g.:

```haskell
type State x y = Success x | Failure y

bind : (A -> State A B) -> State A B -> State A B
bind f x =
  case x of
  	Success v -> f v -- standard application of `f` to a value `v`
  	Failure msg -> Failure msg -- pass through
```



For example

```haskell
Pipeline
├── call endpoint1 
├── awaitAndThen (call, endpoint2)
└── awaitAndThen (call, endpoint3)
```

Each stage will first check if the result is available, and then do an additional call.



##### Monoid

```haskell
-- a type A
type A x = B x | C

-- an associative binary operation
join : A -> A -> A

-- an identity element
type I = 0  -- for summation
type I = 1  -- for products
type I = [] -- for sequences

-- application of I and any value x 
x == join I x

-- wrap A around x
return : x -> A x
```

For example

```haskell
sum : Int -> Int
i = 0
fold sum 1,2,3 == sum( sum( sum(i, 1), 2), 3) == 6
```



#### Multi track functions

Given a pipeline of functions

```py
Start
├── apply f
├── apply g
└── apply h
```

Where

```haskell
f : A -> A | Error
g : A -> B | Error
h : B -> C | Error
```

Bad solution

```py
def apply_pipeline(x):
  result = f(x)
  if result is not Error:
    result = g(x)
    if result is not Error
      result = h(x)
 return result
```

With Exceptions

```python
def apply_pipeline(x) raises Exception:
  return h(g(f(x)))

def f():
  # ...
  raise Error()
```

