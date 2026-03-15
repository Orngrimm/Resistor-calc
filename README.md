# Purpose  
A simple calculator for ideal resistors for non standard values.  

Want to run it directly from here?  
https://rawcdn.githack.com/Orngrimm/Resistor-calc/main/Resistor-Calc%20V15.0.html

Now with optimised calculations which let it calculate up to e192 (LOL!) in a reasonable time.  

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
