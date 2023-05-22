## LAB REPORT 4 <br> Danielle Dang 
<br>

Lab Report task: Do steps 4-9 listed in the lab write up and provide screenshots and the keys used to produce complete the step 

**Step One: Log into ieng6**


<img width="549" alt="Screen Shot 2023-05-22 at 3 58 22 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/6b40cd3d-d92e-411e-81e8-c87696b7f6bd">

I had previously logged into my ieng6 account, therefore instead of typing out "ssh cs15lsp23jw@ieng6" I was able to type this instead:

```
<up> <up> <up> <enter>
```
Output:

<img width="416" alt="Screen Shot 2023-05-22 at 3 58 48 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/94f82024-120f-4acb-a198-01af9d71c9ea">

The up command allowed me to go through my history and retrieve the input from the last time I logged into my ieng6 account. This saved a lot of time, and rather 
than spending all the extra time trying to type out ssh and my account, I was able do so with only a few up arrow commands. 

**Step Two: Clone your fork of the repository from your Github account**

<img width="567" alt="Screen Shot 2023-05-19 at 9 11 52 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/ea30b812-b6ff-45c4-bb30-d772fe05acad">

In order to clone the fork of the repository from my github account I typed out: 

```
<g> <i> <t> <space> <c> <l> <o> <n> <e> <Command-C> **the ssh link of the github I wanted to clone** <Command-V> to paste it into my terminal <enter> 
```
The Command-C and Command-V allowed me to paste the link of the repository I wanted to copy faster and easier. Rather than using my mouse I was able to quickly used these commands 
and complete my tasks in a fast manner. 

Output: 

<img width="693" alt="Screen Shot 2023-05-22 at 3 59 22 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/60985f41-b9f6-4c6c-b303-54b2059733b4">

**Step Three: Run the tests, demonstrating that they fail**

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

Now that we made the changes to fix the code in ListExamples, we can run JUnit again to indicate it properly works. 

To do this, the keys used were: 

```
<Ctrl C> **I copied the Junit javac from week 3 on the cse15 spring website into the terminal first** <Ctrl V> **paste into terminal** <enter> <Ctrl C> <Ctrl C> **Copied Junit java from week 3 onto cse15 sprin website into the terminal** <ListExamplesTests> **the file I want to run JUnit On**  <enter> 
```
Output of this: 

<img width="697" alt="Screen Shot 2023-05-22 at 11 53 16 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/9da1f10d-8b85-419a-b1cd-342e4738c909">

This indicates that the code was fixed and all the tests that failed previously is now passing 

**Step Six: Commit and push the resulting change to your Github account.**

Now that I had fixed my code, I want to commit and push the code that now properly works into my github account. 

I did this using the following keys: 

```
<git add . > <enter> <git commit -a changed> <enter> <git push> <enter> 
```
The output of these actions is: 

<img width="315" alt="Screen Shot 2023-05-22 at 11 59 33 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/e2088706-9f7b-499c-9c3a-381c738722e6">

<img width="509" alt="Screen Shot 2023-05-22 at 11 59 55 AM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/482b89a9-a9be-4712-ac85-d6e9c6f18585">

The changes are now officially made and pushed to github! 

Now we had successfully changed our code and fixed it, and commit and push it to git. 
