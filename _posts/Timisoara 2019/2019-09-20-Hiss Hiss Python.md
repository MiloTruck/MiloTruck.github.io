---
title: "Hiss Hiss Python [50]"
tags: [Timisoara CTF, Binary Exploitation]
excerpt: "Binary Exploitation"
layout: single
classes: wide
--- 

**Category:** Binary Exploitation 

> This snake likes to h1ss at its input.  
nc 89.38.208.144 11113

[Challenge Files](https://github.com/MiloTruck/CTF-Archive/tree/master/Timisoara%20CTF%202019%20Qualification%20Round/Binary%20Exploitation/Hiss%20Hiss%20Python%20%5B50%5D){: .btn .btn--primary}

## Write-up
Vulnerability: [https://blog.efiens.com/efiensctf2019-round2-write-ups/](https://blog.efiens.com/efiensctf2019-round2-write-ups/)

Unlike Python 3, Python 2's input() actually evaluates the input instead of taking it as a string. If we feed a command into input(), Python 2 will run the command, which is the vulnerability.
Giving `__import__('os').system('/bin/sh')` as input opens a shell.

**Flag:** TIMCTF{h1ss_h1ss_shell}