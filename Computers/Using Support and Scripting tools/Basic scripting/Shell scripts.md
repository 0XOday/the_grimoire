

* loops
```
#!/bin/bash
# Demonstrate For syntax in Bash
for i in {1..254}
do
ping -c1 “192.168.1.$i”
done
```



* Operators
	* Controls the flow of a script 

  
| Symbol Notation | Switch Notation | Usage                                                           |
| --------------- | --------------- | --------------------------------------------------------------- |
| ==              | -eq             | Is equal to (returns TRUE if both conditions are the same)      |
| !=              | -ne             | Is not equal to (returns FALSE if both conditions are the same) |
| <               | -lt             | Is less than                                                    |
| >               | -gt             | Is greater than                                                 |
| <=              | -le             | Is less than or equal to                                        |
| >=              | -ge             | Is greater than or equal to                                     |
| &&              | AND             | If both conditions are TRUE, then the whole statement is TRUE   |
| \|              | OR              | If either condition is TRUE, then the whole statement is TRUE   |


