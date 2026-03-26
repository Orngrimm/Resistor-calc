# Purpose  
A simple calculator for ideal resistors for non standard values.  

Want to run it directly from here?  
https://rawcdn.githack.com/Orngrimm/Resistor-calc/main/Resistor-Calc%20V15.4.html

# Features
Now with optimised calculations which let it calculate up to e192 (LOL!) in a reasonable time.*  
Sports a copy-Button to quickly copy a solution as plaintext.  
Now also with PDF-export!
Best (and simplest of the best) solution is now marked.  
Ontime-Evaluation for valid inputs of the target-resistance (Green/Red background of the field)  
## *Calc-Improvements
1. Sorted + early exit (biggest win for series)
For series, sort values and binary-search for the best complement instead of looping. Reduces O(n²) to O(n log n).
3. Precompute all parallel pairs (biggest win for parallel-heavy topologies)
Instead of recomputing parallel(R1,R2) inside nested loops, precompute all unique parallel combinations into a flat array once. Then the (2par)+(2par) problem becomes two lookups into that array
O(n²) instead of O(n⁴).
5. Deduplicate pairs
Since parallel(R1,R2) = parallel(R2,R1), only compute each pair once (upper triangle of the matrix).

For E192 (~1750 values), (2par)+(2par) goes from ~9 billion iterations down to roughly 3 million — about 3000× faster. E192 should now calculate in well under 20 second.

## Circuits
These circuits are available:  
- 2 & 3 Resistors in series  
- 2 & 3 Resistors in parallel  
- (2 Parallel) + 1 in series  
- (2 Parallel) + (2 parallel)  

## 0 and infinity?
Jumpers (0 Ohm) and infinity (not placed resistors) are considered  

# User Interface
![User Interface](https://github.com/Orngrimm/Resistor-calc/blob/main/imgs/UI.png?raw=true)

# Limits
The limit of the biggest resistor-Value can be adjusted in const DECADES where 1e8 = biggest single resistor would be (theoretically) 999MOhm (if your E-Series supports that).  
As an example, this leads to a maximum value with E12 of 820MOhm per single resistor.  

## Customisation
If you want to add your own e-Series, just add them in the SERIES_DESC and E_SERIES. You may even remove or add certain resistor values if you dont have them in stock or have special values at hand...

## Precision
Fractions of Ohms (like 5.5 Ohm) are supported as target-values.  
If you enter the technical way (12k4 instead of 12400) please be aware that i only account for 1 decimal after the comma and will report it if there are more)
