<!-- translation
[English](README.md) | [Tiếng Việt](README-vn.md) | [简体中文](README-cn.md) -->

<!-- genereal ideas:
* theme specific
* powerful cheats in general
* the whole design is done in a cool manner
* maybe hosting a website and stylyying it for cheat sheets

concrete ideas:
* rdkit cheat sheet!
* important python standard libs cheat sheets
* termux, raspi

dotfiles -->

# Cheat sheet (Linux)

This is a collection of commands I'm using on my linux machine as a python developer. 

# Contents

1. [Shell Expansions, Logical Operators](#shell-expansions-logical-operators)
      * [Shell Expansions](#shell-expansions)
      * [Logical Operators](#logical-operators)
2. [Basic Commands](#basic-commands)
      * [Beginner](#beginner)
      * [Intermediate](#intermediate)
      * [Advanced](#advanced)
3. [Command Line Tools](#command-line-tools)
      * [Git](#git)
      * [Anaconda](#anaconda)
      * [Docker](#docker)
      * [LSDeluxe](#lsdeluxe)
4. [Aliases](#aliases)
5. [Shortcuts](#shortcuts)
      * [Terminal](#terminal) 
      * [Chromium Browser](#chromium-browser) 
      * [VSCode](#vscode) 
6. [Shell Scripting](#shell-scripting)
      * [Bash in a Nutshell](#bash-in-a-nutshell)
      * [Variables](#variables)
      * [Loops](#loops)
      * [Functions](#functions)
      * [Condtionals](#conditionals)
7. [Raspberry Pi](#raspberry-pi)


I use the alias `marcopolo` to reach this cheat sheet faster:

```bash
echo "\nalias marcopolo='xdg-open https://github.com/NiklasTiede/cheatsheet'" >> ~/.bashrc
source ~/.bashrc
```

---

# Shell Expansions, Logical Operators

## Shell Expansions

Expansions are performed by the shell before the command is executed. **Tilde** and **filename** **expansion** are used more often when interacting with the shell. **Brace**, **variable** and **arithmetic** **expansion** tend to be used more often while doing shell scripting.

The tilde `~` expands to the environment variable `$HOME`, which is usually the home directory. If `$HOME` is not defined, tilde `~` expands with the home directory by default.

```bash
$ echo ~
/home/username
```

Filename expansion is a way to select easily a number of files or directories from within the current working directory as arguments for a command. A glob pattern containing wildcard characters specifies the set of filenames. 

| Wildcard Character | Represents | 
|--|--|
| `*` | 1 or more character |
| `?` | 1 character |
| `[0-9]` `[a-z]` | 1 specified character |

Examples:

```bash
$ ls
file1.go  file2.go  file3.py  file4.py  file40.py

$ ls *.py
file3.py  file4.py  file40.py

$ ls file?.py
file3.py  file4.py

$ ls file[0-3].*
file1.go  file2.go  file3.py
```
**[⬆ back to top](#contents)**

---

## Logical Operators

Shell control operators let you expand your possibilities using the shell vastly. 

| Symbol | Example | Description | 
|--|--|--|
| `&` |  | execute in background |
| `;` | `com1; com2` | execute always  |
| `&&` | `com1 && com2` | logical and |
| `>` or `<` |  | redirection |
| `>>` or `<<` | `echo 'source x' >> ~/.bashrc` | append |
| `|` | `history | grep 'patt'`  | pipelining |
| `||` |  | logical or |

These operators and shell expansions will be found throughout this cheat sheet repeatedly.


**[⬆ back to top](#contents)**

---

# Basic Commands

GNOME built-in commands/programs

## Beginner

basic navigation on the system:

```bash
cd
ls
pwd
```


## Intermediate



```bash

```

## Advanced

pretty useful combinations:

```bash
  
```






help


```bash
pwd
ls
cd
clear
history | tail
df -h  
```

```bash
help   # 
<command> --help   # 
man <command>   # 
info <command>   # 
whatis <command>
which <command>   #  
locate <command>  #

file *             # lists the types of all files
```


using filename expansion, globbing, shell expansion, wildcard characters

searching for string pattern in all files:
grep, good for pipelining and searching through files

```bash
#  print only names of files containg the pattern from cwd:
grep -rl 'patt'

# shows also each line where pattern is occuring:
grep -rnw '/path/' -e 'patt'

# search through all files recursively
grep -rnw 'patt' 

# searches only certain files for the search pattern
grep -rnw -e 'patt' --include=*.py   

-r recursive
-l only filenames
-n numbber of line within file
-w only whole word
--include only certain files included
```


 environment variables:
 
```bash
printenv      # 
echo $PATH      # 
      # 
      # 
      # 
```

text

```bash
      # 
      # 
      # 
      # 
      # 
```


**[⬆ back to top](#contents)**

---

# Command Line Tools

text

## Git


**[⬆ back to top](#contents)**

---

# Aliases

make asliase to increase prodictivity 


**[⬆ back to top](#contents)**

---

# Shortcuts

Terminal Shortcuts on Linux
|  Shortcut |  Meaning |
|---|---|
| <kbd>Ctrl</kbd> <kbd>Alt</kbd> <kbd>T</kbd> | open terminal |  
| <kbd>Ctrl</kbd> <kbd>Shift</kbd> <kbd>Q</kbd> | close terminal | 
| <kbd>Tab</kbd> | autocomplete, navigation | 
| <kbd>Ctrl</kbd> <kbd>Shift</kbd> <kbd>Up</kbd> or <kbd>Down</kbd> | scrolling up, down |
| <kbd>Ctrl</kbd> <kbd>R</kbd> | search history |
|  |  |
|  |  |
|  |  |

**[⬆ back to top](#contents)**

---

# Shell Scripting

important shebang lines: what is a shebang line and why do they exist?

`#!/bin/bash`
`#!/bin/sh`
`#!/usr/bin/env python`

**[⬆ back to top](#contents)**

---

# Raspberry Pi



**[⬆ back to top](#contents)**






---

# Basic Syntax

## Hello World

File `hello.go`:
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello Go")
}

```

`$ go run hello.go`


|Operator|Description|
|--------|-----------|
|`==`|equal|
|`!=`|not equal|
|`<`|less than|
|`<=`|less than or equal|
|`>`|greater than|
|`>=`|greater than or equal|


```go
var i int = 42
var f float64 = float64(i)
var u uint = uint(f)

// alternative syntax
i := 42
f := float64(i)
u := uint(f)
```


```go
ls -la
var i int = 42
var f float64 = float64(i)
var u uint = uint(f)

// alternative syntax
i := 42
f := float64(i)
u := uint(f)
```
