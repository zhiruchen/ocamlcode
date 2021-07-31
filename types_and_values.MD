
# Types And Values

```ocaml
utop # 42;;
- : int = 42

```

* 42 is the value
* int is the type of the value
* -: the value is not given a name

```ocaml
utop # let x = 86;;
val x : int = 86

```

* A value was bound to a name, hence the `val` keyword
* `x` is the name to which the value was bound
* `int` is the type of the value
* `86` is the value.

```ocaml
utop # let increment x = x + 66;;
val increment : int -> int = <fun>

```
* `increment` is the identifier to which the value was bound.
* `int -> int` is the type of the value. This is the type of function that take an int as input and produce an `int` as output, the arrow `->` as visual metaphor for the transformation of one value into another value.
* `<fun>` a palceholder to indicate that there is some unprintable function value.

* call function with syntax like this("apply" the function rather than "call" it)

```ocaml
utop # increment 0;;
- : int = 66
─( 08:37:49 )─< command 7 >────────────────────────────────────────────────────────{ counter: 0 }─
utop # increment(21);;
- : int = 87
─( 08:43:13 )─< command 8 >────────────────────────────────────────────────────────{ counter: 0 }─
utop # increment (increment 5);;
- : int = 137

```

