![[Pasted image 20250421010759.png]]


Integer division throws away the remainder.

*Type conversions*
* Converts one data type to another 
	* used in cases for when you have more than one data type for formulas 
		* `Example, given that about 50.4% of human births are males, then 0.504 * numBirths calculates the number of expected males in numBirths births. If numBirths is an integer variable (integer because the number of births is countable), then the expression combines a floating-point and integer.`
	* Another type of conversion is implicit conversion which automatically changes the data type. 
		* Arithmetic operators such as + or * if one of operand is a float the other one is automatically converted to a float 
		* Integer-to-float conversion is straightforward: 25 becomes 25.0.
		* float-to-integer_ conversion just drops the fraction: 4.9 becomes 4.
	* Example
		* `expectedMales = 0.504 * numBirths` as stated above implicit type casting is preformed due to one operand being a float   


## Chapter 3 section 5 : operators
```
10 << x << 15 = Math expression 

(10 < x ) and ( x < 15 ) Corl expression 

Both of these detect if a value is within a given range 

```