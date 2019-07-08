# learnResKdb
Summary documentation of KDB+ functionalities and features.
Source: https://www.tutorialspoint.com/kdbplus/kdbplus_architecture.htm

About
-----
KDB+: k database plus
Q: the programming language working with kdb+

Kdb+ is a high-performance, high-volume database designed from the outset to handle tremendous volumes of data. It is fully 64-bit, and has built-in multi-core processing and multi-threading. 

Getting Started
---------------
Download kdb+ from & store directly under C-drive (Windows): http://kx.com/software-download.php

To start using kdb+, you need to start the q session. Three ways:
1. type “c:/q/w32/q.exe” on your run terminal.
2. MS-DOS command terminal and type q
3. q.exe file onto “C:\Windows\System32” and on the run terminal, just type “q”.


Example
-------

**Date**
Internally stored as integer with reference date 01-Jan-2000 with dates after/before stored as positive/negative number. 
Default format: "YYYY.MM.DD"
