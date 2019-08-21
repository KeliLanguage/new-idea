## Function definition
```hs
f
 : (x: Number, y: Number) -> Number 
 = (x, y) -> x + y
```

## Function application
The following are equal
```c
f (x: 1, y: 2)
f (y: 2, x: 1)
f (x: 1)(y: 2)
f (y: 2)(x: 1)
2 f(x: 1)
1 f(y: 1)
```

## Object construction
```c
obj = (x: 1, y: 2)


// OR


x = 1
y = 2
obj = (x, y)
```

## Property access
```c
obj x 
obj y
```

## Object deconstruction
```
obj = (x: 1, y: 2)
(x, y) = obj
```

## Examples
```hs
List(of: T) = union {
  | Nil
  | Cons (element: T, next: List(of: T))
}

map
  : (function: A -> B , over: A List) -> B List 
  = (function, over: list) -> 
  list if {
    | Nil -> Nil
    | Cons (element, next) -> Cons (element: function(element), next: next map(function))
  }
```
