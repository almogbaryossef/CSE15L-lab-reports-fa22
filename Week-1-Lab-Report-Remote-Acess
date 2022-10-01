# **Lab Report 1: Remote Access**

This report gives a detailed step-by-step tutorial about establishing a remote connection between the student's private device and a UCSD platform that has a s unique account for each stuedent in CSE15L.

## Step 1
- Every student has an existing course-specific account for CSE15L at this [website](https://sdacs.ucsd.edu/~icc/index.php).
- After opening the link, enter your username and your student ID number as instructed. After looking up the account, a new webpage will appear. At the top of the page there is an option to change the password to the account. You must click on that link and change the password. Make sure to write down the password in your notes in case you cannot remember it in the future.
- If your password was changed successfully, a message will appear saying that it would take approximately 15 minutes for the password to be processed.

## Step 2
- While waiting, if you do not have Visual Studio Code installed, go to [this link](https://code.visualstudio.com/) and download it.
- Since I have taken CSE 11 in the last winter quarter, I already had VS Code installed.
- The homepage of VS Code should look similar to the following screenshot: 
![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/1#issue-1393192884)

## Step 3
- This step is directed at students who have a mac. I have used a macbook, and therefore followed the steps intended for it.
- In your account, you should find your username which would be of the form cs15lfa22gg@ieng.ucsd.edu. Note that the only unique characters for your username are "gg". While this is my unique combination, yours will be different.
- In order to connect to your remote account through your computer, have VS Code open and open a new terminal.
- In the terminal, type "ssh cs15lfa22gg@ieng6.ucsd.edu"
- "The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established. RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec. Are you sure you want to continue connecting (yes/no/[fingerprint])?" Type yes and enter.
- You will then be asked to enter the password you have chosen in step#1.
- After logging in to the basement's computer (server) through your computer (client), you should see an output similar to this:
![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/2#issue-1393202812)

## Step 4
- In order to see similarities and differences between your personal account and your UCSD account, try running commands such as
  cd ~
  cd
  ls -lat
  ls -a
  etc.
 - Below are screenshots of commands I ran on my personal computer's account and my UCSD account.
 ![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/3#issue-1393205926)
 ![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/4#issue-1393206212)
 
 ## Step 5
 - An important skill while remotely accessing another device is the ability to copy a file from one device to the other.
 - While completing the lab, I have used an example class given by the professor as a file that I wanted to copy from my account onto my UCSD account.
 - The code for this class is below:
 class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
- Compile and then run WhereAmI to make sure that it works.
- Then, I entered the command "scp WhereAmI.java cs15lfa22gg@ieng6.ucsd.edu:~/" which copied and pasted the file WhereAmI.java.
- After having entered the command with your personal username, enter your password.
- Run the WhereAmI program, and notice the differences between the outputs.
![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/5#issue-1393209397)
As you can see, I had a typo (replaced @ with .), which caused me to be unable to log into my account. After I fixed it, I was able to run the program.

## Step 6
- Since it can be troublesome and time consuming to enter your password every time you want to log into your UCSD account, there exists a tool called ssh keys in which you can create a key from your computer to the remote computer. A public key is compied onto the remote computer, and the private key is saved on yours.
- If you are still logged into your remote account, log out by typing "exit".
- I have created my key during the lab, but forgot it and had to delete my key and create a new one for the purpose of this lab. Therefore, the following screenshot contains the new key I created. Enter the same commands, starting with "ssh-keygen" but adjusting them to match your personal information.
![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/6#issue-1393212150)
- After having created your private key, you need to log into your UCSD account (use the "ssh cs15lfa22gg@ieng6.ucsd.edu" command, and enter your password).
- Enter the command "mkdir .ssh" After the file was created, log out ("exit"). You can see in the screenshot above that this file already existed on my account.
- On your account (client), type "scp /Users/almogbar/.ssh/id_rsa.pub cs15lfa22gg@ieng6.ucsd.edu:~/.ssh/authorized_keys"
- Below is a screenshot of that process. I have been able to log into my account without entering my password using the key.
![Image](https://github.com/almogbaryossef/CSE15L-lab-reports-fa22/issues/7#issue-1393212988)

## Step 7

You are done. Good job :)
