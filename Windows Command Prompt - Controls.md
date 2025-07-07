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



**##search for the presence of that package**



winget searcg <package\_name>



**##install the package that is required**



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



**6.to Open an app in the targeted directory** 



**(Ensure the target directory)**



<file\_name.extension>



**7.to change directory**



**##to directly change the path**



> cd "<path>"



**##For changing drives and directories in one command**



> cd /d D:\\Path\\To\\Folder

 

**## to get back to the previous folder** 

> cd..



**## to change to another disk** 

> cd D:


(and then move to your required dir)



**8. to list all the files in the directory**



> dir



**9. to clear the screen**



> cls



**10. to view current directory**



> cd



**11. to delete all files or folders**



> del filename.txt ##to remove file



> rmdir /s /q foldername ##to remove folder 



