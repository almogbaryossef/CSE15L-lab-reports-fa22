# Lab Report 3 (Researching Commands)

I have chosen to explore the command "grep". During the lab in week 4, we saw that grep can be used to find all lines in a file that contain a certain string (we used ".txt" to get the paths in the file find-results.txt of .txt files).
The format which we used was: grep <some string> <file>. The command grep can also be used in the format: grep <command-line option(s)> <pattern> <file1> <file2> ...

## Command-line Option 1: -c
**-c** can be used with grep to return the number of lines that contain the pattern provided in the chosen file(s).
We use the format: grep -c <pattern> <file1> <file2> ....

Example 1:
![Image](-cExample1)
  
Example 2:  
![Image](-cExample2)
  
Example 3:
![Image](-cExample3)
  
  
## Command-line Option 2: -v
**-v** returnss all the lines that do not fulfill the pattern prvided in the chosen file(s).
We use the format: grep -v <pattern> <file1> <file2> ...

Example 1:
![Image](-vExample1)
  
Example 2:  
![Image](-vExample2)
![Image](-vExample2.2)
  
Example 3:
![Image](-vExample3)
  

