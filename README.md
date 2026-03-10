A simple calculator for ideal resistors for non standard values.
available:  
2 & 3 Reisitors in series  
2 & 3 Reisitors in Parallel  
(2 Parallel) + 1 in series  
(2 Parallel) + (2 Parallel)  

![User Interface](https://github.com/Orngrimm/Resistor-calc/blob/main/Img/2026-03-10%2012-24-09.png?raw=true)


The limit of the biggest resistor-Value can be adjusted in const DECADES where 1e8 = biggest single resistor would be (theoretically) 999MOhm (if your E-Series supports that).  
As an example, this leads to a maximum value with E12 of 820MOhm per single resistor.  

If you want to add your own e-Series, just add them in the SERIES_DESC and E_SERIES. You may even remove or add certain resistor values if you dont have them in stock or have special values at hand...

Fractions of Ohms (like 5.5 Ohm) are supported as target-values

