### Calculus Lambda 

```
e ::= x
    | \x -> e
    | e1 e2
```

### Identity Function

```
\x -> x
```

### Beta Reduce

```
(\x -> e1) e2 == e1[x := e2]
```

### Omega Combinator

```
(\x -> x x) (\x -> x x)
```

### Boolean

```
true == \x y -> x
false == \x y -> y
if == \b x y -> b x y
```

### Logical Operators (not x and x or)

```
not == \b -> b true false
and == \b1 b2 -> b1 b2 false
or == \b1 b2 -> b1 true b2
```

### Records (Tuple)

```
pair == \x y -> (\b -> if b x y)
first == \p -> p true
second == \p -> p false
```

### Numbers (Church Number)

```
zero = \f x -> x
one == \f x -> f x
two == \f x -> f (f x)
three == ...
```

### Increment

```
\n -> \f x -> f (n f x)
```

### Add (+)

```
\n m -> n INC m
```

