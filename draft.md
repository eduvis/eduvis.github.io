---
layout: page
title: Maple CAS Software Calculator Operation Using MS Windows with the NVDA Screen-reader
description: "Here is a Cheat Sheet for VCE students interested in operating a CAS calculator independently, using the NVDA screen reader. Best of luck and get in touch if you need a hand."
permalink: /maple-2022-cheat-sheet/
---

By Charlie Roberts
Here is a Cheat Sheet for VCE students interested in operating a CAS calculator independently, using the NVDA screen reader. Best of luck and get in touch if you need a hand.
## Maple 2022 Operation
### Acknowledgements
Thanks to Robert & Raymond from [ASES](https://www.ases.co/) and Nathaniel from EduVis, for contributing to this document.
### Description
Maple Computer Algebra System (CAS) software can algebraically manipulate numbers, symbolic formulas, polynomials, sets, lists, equations, arrays, vectors, and matrices. It can solve systems of equations and differentiate and integrate expressions. Maple can run on Windows, Mac & Linux operating systems.
### Screen reader Accessibility in Maple 2022
Maple now has an accessibility mode which optimizes the Standard interface for users of the NVDA screen reader.

To turn on screen reader mode in Maple 2022:
From the Tools menu, select ```
Accessibility > Use Screen Reader Settings
```
. Alternatively, use the shortcut key `F10`.

Maple 2022 Screen Reader settings (standard interface) are tested and optimized for NVDA. An image of the standard interface in Screen Reader mode is below. However, JAWS users will still need to operate in the command-line interface by selecting the `Windows key`, then ```
Maple 2022 (command-line)
```
. NVDA users can also operate in the command-line interface if they wish. See picture below of the command line interface.

Maple standard interface worksheets and documents can be saved using ```
Alt, File, Save as…
```
.

Maple has a range of topic packages. For example, if you want to see commands for Statistics, type 
```
?Statistics
```
. Accessibility options are found at
```
?worksheet,managing,accessibility
```
.

### MAPLE 2022 (STANDARD) DOCUMENT TYPES
Pressing ```
CTRL+N
```
will open a new worksheet document, which allows you to toggle between Math & Text entry by using the `F5` key.

Use `Alt`, `F`[ile], `N`[ew], `D`[ocument]: to open in Document Mode, which allows you to toggle between Math, Text, & non-executible Math by using the F5 key. However, the screen reader does not announce the mode.

### NVDA SCREEN READER COMMANDS
- To receive output in 1-D (horizontal set out) in Maple 2022:
   select `Alt`, `T`[ools], `O`[ptions], `RightArrow` to `Display` then `Tab` to `input display` and arrow to `Maple Notation`. Also `Tab` down to `Output display` and `arrow` to `Maple notation`.
- For feedback as you type, press
   ```
      NVDA+2 or 3
   ```
   to toggle the speaking of characters/words. If you are using laptop mode as your keyboard layout, CapsLock should serve as a sufficient NVDA modifier key. If using desktop mode, you may be able to use the Insert key, or numpad Insert.
- Note the following:
   - By default, unless you have modified it, NVDA doesn’t save its settings automatically, so you’ll either have to go into preferences and turn on the ‘save on exit’ option, or otherwise press 
      ```
         CTRL+NVDA+C
      ```
      to save configuration.
- Use
   ```
      NVDA+L
   ```
   to read the current input line. Some symbols, such as the `caret` (`^`), or index (power of) are not always announced when pressing NVDA & L or arrowing up & down. Therefore, press NVDA+L twice for it to be spelt out. Press three times for phonetic rendering. Alternatively, hold down 
   ```
      NVDA+Left or Right arrows
   ```
    to hear each character announced, assuming the `Review Cursor` is tethered to the `Focus`.
- Use the Review Cursor to review the previous logs of input and output. Press
   ```
      NVDA+Up/Down arrows
   ```
   in the command line interface, or
   ```
      NVDA+Up/Down arrows
   ```
   in the standard interface, to go up or down a line in the current `Navigator object`. Additionally, use
   ```
      NVDA+Left/Right arrows
   ```
   to navigate by character and include the `Control` key with the `left/right arrows` to move by word.
- If you have accidentally changed from object to screen review, then press
   ```
      NVDA+PGDN (or Page-Down)
   ```
   to cycle to object review.

### COMMON MATHEMATICAL OPERATIONS
At the end of every input line you enter, you need to input the `semi-colon (;)` for Maple to know the line is finished.

```
   x + y - z;
```
will show you how addition and subtraction work.

```
   x * y;
```
shows you how multiplication works.

```
   x / y;
```
shows you how division works.

```
x^y;
```
for power (use NVDA key with L twice to read the term
   ```
x caret y
```
).

```
sqrt(x);
```
is for square root (√)

```
   exp(x);
```
is for exponential
```
sin(x);
```
```
cos(x);
```
```
tan(x);
```
for trigonometric functions

```
arcsin(x);
```
```
arccos(x);
```
```
arctan(x);
```
for inverse trig functions

Press
```
CTRL+Space
```
for command prediction in the standard interface.

### SOLVING
```
eval(xˆ2+5*x, x=1);
```
evaluates the polynomial `x^2 + 5x at x= 1` and returns `6`.

```
evalf(expression );
```
Numerically evaluates an expression and returns its decimal approximation
   e.g.
   ```
      evalf(Pi);
   ```
   returns numerical approximation `3.141592654`.

```
subs(x=value,expression );
```
Substitutes the given value into expression.
   e.g.
   ```
      subs(x=2,xˆ2+2*x+1);
   ```
   gives `9`.

#### EXPANDING
```
expand(expression );
```
Distributes the given expression. e.g. `expand((x+3)*(x+5));` returns `x 2 + 8x + 15`.

Factorising polynomials e.g. `factor(4*xˆ2+12*x+8);` returns `4(x + 1)(x + 2)`.

```
evalf(6/9);
```
`0.6666666667`
```
Eval(6/9);
```
`2/3`

### SURDS
#### square root:
```
sqrt(8);
```
`2*2^(1/2)`

#### cube root:
```
root(8, 3);
```
`2`

### Solve Equations
```
solve(n/6 = 5);
```
`30`

```
solve(2*b - 4*b = -b + 3);
```
`-3`

### Inequalities
#### One step linear inequalities
```
solve(`>=`(z + 4, 1));
```
`RealRange(-3, infinity)`

### Exponential Functions
```
solve(8^x = 9);
```
`2/3*ln(3)/ln(2)`

```
fsolve(8^x = 9);
```
`1.056641667`

### Monomials
```
4*u^5 + u^5;
```
`5u^5`

```
(9*u^5)*(3*u^6);
```
(need to put asterix between the brackets)
`27*u^11`

```
(4*g^2)/(4*g^9);
```
`1/g^7`

### Polynomials
#### add and subtract polynomials
```
(5*x^2 + 2*x - 4) + (-2*x^2 + 4*x - 5);
```
`3 x ^2+ 6 x - 9`

#### Multiplying polynomials (expanding)
```
expand((q - 3)*(q + 3));
```
`q^2-9`

#### Factorising
```
factor(g^2 + 14*g + 13);
```
`(g + 13) (g + 1)`

```
factor(m^2 - 10*m + 25);
```
`(m-5)^2`

### Quadratic Equations
```
solve(2*(y + 4) = 0);
```
`-4`

### Simultaneous equations
```
solve({x+y= 6, x-y = 2}, [x, y]);
```
(soles the system of two equations)
`[[x = 4, y = 2]].`

### STATISTICS
call up the stats package by typing the next line:
```
with(Student[Statistics]):
```

#### E.g. #1
```
>
Mean([2,4,4.0])
3.333333333
```
Compute the mean of data not containing any floating point values. This leads to an exact result.
```
>
Mean([2,4,4])
10/3
```

#### E.g. #2
```
A:=[5,4,3,2,1]:
Mean(A);
3
Quartile(A,3);
4
Quartile(A,1);
2
```
