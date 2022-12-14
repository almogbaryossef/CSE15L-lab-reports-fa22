# Lab Report 4 - Vim

## Part 1 - Sequence of vim commands to replace all **start** with **base**
1. Open the file using vim by typing **vim DocSearchServer.java**.
![image](1.png)

2. Press \<Enter> in order to view the file in vim
![image](2.png)
  
3. Type 
```
:%s/\<start\>/base/g
```
in order to substitute all instances of **start** with **base**. 
**%** tells vim that we want to search&replace start for base in the entire file (the range)
**:...g** means that the command/pattern that we want to form will occur recursively for each line in the file that is within the range
**:s** is the substitute command, so in this case s tells vim that we will want to substitute one thing with another somewhere in the file (this is the action we want it to take)
**/start** the / means that whatever words follows it, in this case it is start, is the word it should search for. 
**\<*some word*\>** indicates that we are searching for a whole word, and we are marking its beginning and end.
Therefore, this command means that we are substituting in each line that contains the whole sequence of letters *start* with base, and we do that for all lines in the file. We first search for the next occurrence of start, substitute it with base, and if this is not the end of the file, execute the search/substitute again until there are no more lines in our range (file) that contain start.
![image](3.png)
  
4. Press \<Enter> in order to execute the substitution command above.
![image](4.png)
  
5. Type **:wq** in order to save the changes we have made in the file and exit.
![image](23.png)
  
6. Press \<Enter> to execute the command above, exiting vim.
![image](24.png)


## Part 2
Changing and running the program on the remote took 55 seconds.
Changing the program on the local computer and then using scp to copy it to the remote took 1 minute and 26 seconds.

- *Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?*


When working on a program that doesn't need many changes, I would rather simply do the changes on the remote. However, if the program had to be written from scratch or needed to be changed significantly, it does not make sense to do this twice, so I would use scp (there is a good chance of mistyping or making small mistakes that scp would eliminate). It is clear that for the program we had changed for this lab it is better to simply make changes on the remote since it takes significantly less time.


- *What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)*


As I stated above, I would consider the length of the file and the amount of editing it needs. scp might not be a good command to use if we want to copy large files, especially if we want to make only a few changes that don't require a lot of time. However, for shorter programs which we have done significant editing to so that editing on the remote would take almost as long as writing the program from the beginning, it would be a good idea to use scp.
