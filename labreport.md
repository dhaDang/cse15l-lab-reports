## LAB REPORT 1 <br> Danielle Dang 
<br>
Listed below is a step by step guide on how to log into a course specific account on **ieng6**!

### Step One: Installing VScode
If you don't have Visual Studio Code installed yet, open [VsCodeLink](https://code.visualstudio.com/) and follow the instructions provided.
The website should look like this!
<br>
<img width="919" alt="Screen Shot 2023-04-06 at 5 31 41 PM" src="https://user-images.githubusercontent.com/130107069/230517119-61e3cf37-d004-4413-a5e1-5e696a1e8386.png">

Note: Theres a dropdown if your device is not a mac

Once installed, open Visual Code Studio. The homepage should look similar to this: 
<img width="904" alt="Screen Shot 2023-04-06 at 5 33 47 PM" src="https://user-images.githubusercontent.com/130107069/230517292-8fd3323c-0f94-4544-b767-aa0bfd389e02.png">

**Congrats! You completed step 1**

### Step Two: Remotely Connecting 
Now that you have Visual Studio Code installed, you want to use the terminal to connect with a remote computer! In this case, we're trying to log in with a course specific account with ieng6.
<br>
Note: ignore the next few lines if you have a Mac, only complete the next two steps if you're on Windows!
* Install git 
* open a terminal in Vs Code and open a new terminal 

FOR MAC:
* github should be installed already to check write git to terminal 
The output of this should be: 
<img width="561" alt="Screen Shot 2023-04-06 at 5 50 12 PM" src="https://user-images.githubusercontent.com/130107069/230518605-7e217dd5-8650-4d5e-bc4b-6df36a1a2e2c.png">

** Note: steps below are the same regardless of Mac or Windows! **
* write: ssh cs15lsp23xx@ieng6.ucsd.edu ->replace xx corresponding to your personal account
* You should then be prompted to answer a yes/no question ** reply with yes! **
* Then type in your password 
** Now the terminal is connected to the CSE basement! Your terminal should look similar to this**
<img width="321" alt="Screen Shot 2023-04-07 at 10 00 04 AM" src="https://user-images.githubusercontent.com/130107069/230647932-b5accc4d-a4a2-4df7-9b9f-2e75e19f1a2f.png">


### Step 3: Trying Some Commands 
Lets try doing stuff with the terminal (now connected to the CSE basement)
List of commands to try!
* cd ~ (insert descriprion) 
* cd
* ls -lat
* ls -a
* /home/linux/ieng6/cs15lsp23/cs15lspabc (abc is someone else's username) 

Running a few commands shoud look similar to this:
<img width="504" alt="Screen Shot 2023-04-07 at 10 01 02 AM" src="https://user-images.githubusercontent.com/130107069/230648020-d4a64e62-5ab7-4097-8d4b-468e3a9f3784.png">

How do I exit the remote server after I'm done? 
* simple do **Ctrl-D**  or type **exit** 

**Congrats you have successfully connected to a remote server and run commands through it!**




