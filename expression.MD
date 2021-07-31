## If expression

## let expression

```ocaml
let x = 42;;

utop # let x = 42 in x + 1;;
- : int = 43
```

```ocaml

let x = e1 in e2
```

e1: binding expression
e2: body expression

## dynamic semantic

To eval `let x = e1 in e2`:

* eval e1 to value `v1`.
* substitute `v1` for `x` in `e2`, yielding a new expression e2'.
* eval e2' to value `v2`.
* the result of eval the let expression is `v2`.
