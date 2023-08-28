---
id: smasnp7xn4wspgqjvfd5ihb
title: Nix
desc: ''
updated: 1664608831872
created: 1664608815044
---

Nix is an immutable package manager

# Basics of the Language

## Value types

```nix
6/3 # /home/nix/6/3

6/ 3 # 2
```

## Identifiers

```nix
a-b # identifier
a - b # a minus b
```

## String

Strings are `"str"` or `''str''`, single quotes don't make strings.

String interpolation with `${var}`.

## Sets

The `//` operator is an operator between two sets. The result is the union of the two sets. In case of conflicts between attribute names, the value on the right set is preferred.

```nix
nix-repl> { a = "b"; } // { c = "d"; }
{ a = "b"; c = "d"; }
nix-repl> { a = "b"; } // { a = "c"; }
{ a = "c"; }
```

# Derivations

Derivations are the intermediate representation of a build.

The builtin function `derivation`, is used to describe a single derivation (a build task). It takes as input a set, the attributes of which specify the inputs of the build.

- There must be an attribute named system whose value must be a string specifying a Nix system type, such as "i686-linux" or "x86_64-darwin". (To figure out your system type, run nix -vv --version.) The build can only be performed on a machine and operating system matching the system type. (Nix can automatically forward builds for other platforms by forwarding them to other machines.)
- There must be an attribute named name whose value must be a string. This is used as a symbolic name for the package by nix-env, and it is appended to the output paths of the derivation.
- There must be an attribute named builder that identifies the program that is executed to perform the build. It can be either a derivation or a source (a local file reference, e.g., ./builder.sh).

