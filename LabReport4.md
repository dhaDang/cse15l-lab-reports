## LAB REPORT 4 <br> Danielle Dang 
<br>

Lab Report task: Do steps 4-9 listed in the lab write up and provide screenshots and the keys used to produce complete the step 

**Step One: Log into ieng6**

<img width="523" alt="Screen Shot 2023-05-19 at 8 56 40 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/789b8041-a407-433e-a319-88ffe6762b9b">

I had previously logged into my ieng6 account, therefore instead of typing out "ssh cs15lsp23jw@ieng6" I was able to type this instead:

```
<up> <up> <up> <enter>
```
Output:

<img width="576" alt="Screen Shot 2023-05-19 at 9 00 12 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/b99e1140-d717-4612-91d8-1c5c232da4c1">

The up command allowed me to go through my history and retrieve the input from the last time I logged into my ieng6 account. This saved a lot of time, and rather 
than spending all the extra time trying to type out ssh and my account, I was able do so with only a few up arrow commands. 

**Step Two: Clone your fork of the repository from your Github account**

<img width="567" alt="Screen Shot 2023-05-19 at 9 11 52 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/ea30b812-b6ff-45c4-bb30-d772fe05acad">

In order to clone the fork of the repository from my github account I typed out: 

```
<g> <i> <t> <space> <c> <l> <o> <n> <e> <Command-C> the github I wanted to clone <Command-V> to paste it into my terminal <enter> 
```
The Command-C and Command-V allowed me to paste the link of the repository I wanted to copy faster and easier. Rather than using my mouse I was able to quickly used these commands 
and complete my tasks in a fast manner. 

Output: 

<img width="602" alt="Screen Shot 2023-05-21 at 9 49 55 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/2710f51c-fc39-4831-92f2-f4b3db6c959c">

**Step Three: Run the tests, demonstrating that they fail**

Before I was able to run the tests I first had to enter the appropriate directory for the purposes of this lab report: 

<img width="695" alt="Screen Shot 2023-05-21 at 9 53 50 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/f3f302a0-39e8-4199-8878-de124d6e151a">

I did these with the keys:
```
<ls> <enter> <cd lab7> <enter> <ls> <enter>
```

I knew I had previously ran the tests, therefore it was somewhere in my history. With this understanding, I clicked these keys: 

```
<up> <up> <up> <up> <up> <up> <enter>
```

Then in order to run JUnit and run the tests, I used the up arrow keys to go through my history and retrieve it with these keys: 
```
<up> <up> <up> <up> <up> <up> <up> <up> <up> <enter>
```
Another up arrow key allowed me to retrieve the next part of terminal work required to run JUnit 
```
<up> <up> <up> <up> <up> <up> <up> <up> <up> <up> <enter>
```
Output:

<img width="694" alt="Screen Shot 2023-05-21 at 10 00 43 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/aab19d5c-f122-464b-a7f7-418544c1608d">

The terminal indicates that there is a failing test in the java file. 

**Step Four: Edit the code file to fix the failing test**

To enter the code and start editing:
```
<vim> <space> <ListExamples.java> 
```

Once inside the folder to fix the code I pressed:
```
<k> <k> <k> <k> <k> <k> *at this point I was at the line that needed to be fix*  <j> <j> <j> <j> <j> <j> <j> <j> <j> <j> <j> *at this point I'm positioned between the "x" and "1" in "index1 += 1;"* <x> *to delete the 2* <i> *to get into insert mode* <2> <esc> <:wq> *to quit and save*
```

Code after changes:

<img width="694" alt="Screen Shot 2023-05-21 at 10 16 08 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/d842d118-a2f8-423c-a907-575ca35b1ba1">

**Step Five: Run the tests, demonstrating that they fail**

**Step Six: Commit and push the resulting change to your Github account. 

Now that I had fixed my code, I want to commit and push the code that now properly works into my github account. 

I did this using the following keys: 

```
<git commit -a [main 8295a38] changed!> <enter> <git push> <enter password> <enter> 
```
The output of these actions is: 

<img width="671" alt="Screen Shot 2023-05-21 at 12 12 50 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/829f27b3-d97a-475d-92fe-3ad40ce3eb81">

The changes are now officially made and pushed to github! 


