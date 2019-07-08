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


Data types
----------

**Date**

I) Description
Internally stored as integer with reference date 01-Jan-2000 with dates after/before stored as positive/negative number. 
Default format: "YYYY.MM.DD"
Start Day: Saturday (mod 7 -> 0)

II) Use case
```
x: 2015.01.22 
`int$x # number of days since 2000.01.01
`year$x # extracting year from date
`mm$x # extracting month from date 
`dd$x # extracting day from date
# arithmetic operations..
x+1
```

**Times**
Stored as integer of miliseconds as of midnight.
Default format: "HH:MM:SS.MSS"

```
tt1: 03:30:00.000 # store 3.30 am
`int$tt1 # number of milliseconds in 3.5 hours
`hh$tt1 # extract hour component from time
```

**Lists**
```
l1:(-10.0;3.1415e;`abcd;"r")
count l1
l1[0]
l2: (9;8;7)
l2[2]:66 # assignments
symbols:(`Life;`Is;`Beautiful)
chars:("h";"e";"l";"l";"o";" ";"w";"o";"r";"l";"d")
l0:(l1;l2) # combining 2 lists
l3:(9;8;(99;88)) # nesting lists to capture data complexity
```

**Dictionaries**
Extension of lists that create the foundation for creating tables: "key -> value" relationship between elements
```
d:`Name`Age`Sex`Weight!(`John;36;"M";60.3)
d[`Name`Sex] # lookup
d[`Age]:35 # amend & upsert
d[`Height]:"182 Ft" # extend
```


Operations
----------

**Creating Tables**

empty table
```
trade:([]time:();sym:();price:();size:()) # no type declaration
trade:([]time:`time$();sym:`$();price:`float$();size:`int$()) # with type declaration
```

non-empty table
```
trade:([]sym:(`a`b);price:(1 2)) # without key
trade:([sym:`$()]time:`time$();price:`float$();size:`int$()) # with key
```










