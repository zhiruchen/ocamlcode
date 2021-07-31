# Complie ocaml code

```
 ~/D/C/g/ocamlcode> subl hello.ml
 ~/D/C/g/ocamlcode> ocamlc -o hello.byte hello.ml
 ~/D/C/g/ocamlcode> ./hello.byte
Hello world!

```

# Build ocaml code

```
ocamlbuild hello.byte
SANITIZE: a total of 2 files that should probably not be in your source tree
  has been found. A script shell file
  "/ocamlcode/path/_build/sanitize.sh" is
  being created. Check this script and run it to remove unwanted files or use
  other options (such as defining hygiene exceptions or using the -no-hygiene
  option).
IMPORTANT: I cannot work with leftover compiled files.
ERROR: Leftover OCaml compilation files:
  File hello.cmo in . has suffix .cmo
  File hello.cmi in . has suffix .cmi
Exiting due to hygiene violations.
Compilation unsuccessful after building 0 targets (0 cached) in 00:00:00.
 ~/D/C/g/ocamlcode> _build/sanitize.sh
 ~/D/C/g/ocamlcode> rm hello.byte
 ~/D/C/g/ocamlcode> ocamlbuild hello.byte
Finished, 3 targets (0 cached) in 00:00:00.

 ~/D/C/g/ocamlcode> ./hello.byte
Hello world!
 ~/D/C/g/ocamlcode> file hello.byte
hello.byte: a /Users/x/.opam/4.06.0/bin/ocamlrun script executable (binary data)

```

## clean build

```bash
ocamlbuild -clean
Finished, 0 targets (0 cached) in 00:00:00.
00:00:00 0    (0   ) STARTING
```

## Load code from file

```bash
utop # #use "inc.ml";;
val inc : int -> int = <fun>
─( 10:30:48 )─< command 1 >────────────────────────────────────────────────────────{ counter: 0 }─
utop # inc 1;;
- : int = 2
```
