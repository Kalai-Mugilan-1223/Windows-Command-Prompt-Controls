b



**1.Set the variable name to the path** 



**## Temperary set**

set <var\_name>="<path>" #no space between varname and the path



**##Permenant set** 

setx <var\_name> "<path>"



**2.Access the app that is declared** 



**##to open any app that is set with the var name:**



start "" "%<var\_name>%"



**eg:**

start "" "%chrome%" 



**##to open chrome from cmd with the specified link**

start "" "%chrome%" --new-tab <link>



**3.To install any package or applications from the command prompt** 



winget install <package\_name>



**eg:**

winget install python3.10



**4.to create a directory that is not existing**



**(Make sure you are in the targeted directory)**



**##mkdir**



mkdir <folder\_name>

md <folder\_name>



**5.to create a file that is not existing**



**(Make sure you are in the targeted directory)**



**##type nul** 



type nul > <file\_name.extension>  #note: the filename should be given with extension

