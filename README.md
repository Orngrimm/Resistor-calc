# Purpose  
A simple calculator for ideal resistors for non standard values.  

Want to run it directly from here?  
https://rawcdn.githack.com/Orngrimm/Resistor-calc/main/Resistor-Calc%20V13.1.html

## Circuits
These circuits are available:  
2 & 3 Reisitors in series  
2 & 3 Reisitors in Parallel  
(2 Parallel) + 1 in series  
(2 Parallel) + (2 Parallel)  

## 0 and infinity?
Jumpers (0 Ohm) and infinity (not placed resistors) are considered  

# User Interface
![User Interface](https://github.com/Orngrimm/Resistor-calc/blob/main/Img/UI.png?raw=true)

# Limits
The limit of the biggest resistor-Value can be adjusted in const DECADES where 1e8 = biggest single resistor would be (theoretically) 999MOhm (if your E-Series supports that).  
As an example, this leads to a maximum value with E12 of 820MOhm per single resistor.  

## Customisation
If you want to add your own e-Series, just add them in the SERIES_DESC and E_SERIES. You may even remove or add certain resistor values if you dont have them in stock or have special values at hand...

## Precision
Fractions of Ohms (like 5.5 Ohm) are supported as target-values  

# Warning
The e-Series E48, 96 and 192 are VERY timeconsuming as the calculation work scales exponentially.
E24 took me on a modern Laptop like 20sec. E48 was in the ballpark of quite some minutes. 
The time for E96 was exactly LOL and for E192 ist was "Nice try! See you next year".  
But honestly, you really need a precision like 1 femto-Ohm? Yeah... Thought so. Stick with E12 ;)

