## LAB REPORT 4 <br> Danielle Dang 
<br>

Lab Report task: Do steps 4-9 listed in the lab write up and provide screenshots and the keys used to produce complete the step 

**Step One: Log into ieng6**


<img width="549" alt="Screen Shot 2023-05-22 at 3 58 22 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/6b40cd3d-d92e-411e-81e8-c87696b7f6bd">

* I had previously logged into my ieng6 account, therefore instead of typing out "ssh cs15lsp23jw@ieng6" I was able to type this instead:

```
<up> <up> <up> <enter>
```
Output:

<img width="416" alt="Screen Shot 2023-05-22 at 3 58 48 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/94f82024-120f-4acb-a198-01af9d71c9ea">

* The up command allowed me to go through my history and retrieve the input from the last time I logged into my ieng6 account. This saved a lot of time, and rather 
than spending all the extra time trying to type out ssh and my account, I was able do so with only a few up arrow commands. 

**Step Two: Clone your fork of the repository from your Github account**

<img width="689" alt="Screen Shot 2023-05-22 at 4 30 40 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/d3c3cbed-5ee3-4a1c-ad8d-b7ed90bf276d">


* In order to clone the fork of the repository from my github account I typed out: 

```
<git> <space> <clone> <Ctrl-C> 
*the ssh link of the github repo I wanted to clone* 
<Ctrl-V> 
to paste it into my terminal 
<enter> 
```

* The Ctrl-C and Ctrl-V allowed me to paste the link of the repository I wanted to copy faster and easier. Rather than using my mouse I was able to quickly used these commands 
and complete my tasks in a fast manner. 

Output: 

<img width="693" alt="Screen Shot 2023-05-22 at 3 59 22 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/60985f41-b9f6-4c6c-b303-54b2059733b4">

**Step Three: Run the tests, demonstrating that they fail**
* In order to run the tests I must first enter the appropriate directory 

```
<ls> 
<enter> 
<cd lab7> 
<enter>
```

<img width="581" alt="Screen Shot 2023-05-22 at 4 31 57 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/b94606de-f1b9-4e27-990b-5a359513ead7">

* I knew I had previously ran the tests, therefore it was somewhere in my history. With this understanding, I clicked these keys: 

```
<up> <up> <up> <up> <up> <up> <enter>
```

* Then in order to run JUnit and run the tests, I used the up arrow keys to go through my history and retrieve it with these keys: 
```
<up> <up> <up> <up> <up> <up> <up> <up> <up> <enter>
```

* Another up arrow key allowed me to retrieve the next part of terminal work required to run JUnit 

```
<up> <up> <up> <up> <up> <up> <up> <up> <up> <up> <enter>
```
Output:

<img width="691" alt="Screen Shot 2023-05-22 at 4 33 14 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/f3cbe80b-cc28-405d-90ba-50f331af9ae8">

*The terminal indicates that there is a failing test in the java file. 

**Step Four: Edit the code file to fix the failing test**

<img width="422" alt="Screen Shot 2023-05-22 at 4 34 34 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/0d161bbb-9f09-4827-938c-d98944505c9b">

* To enter the code and start editing:

```
<vim> 
<space> 
<ListExamples.java> 
<enter>
```

* Once inside the folder to fix the code I pressed:

```
<k> <k> <k> <k> <k> <k> 
at this point I was at the line that needed to be fix  
<j> <j> <j> <j> <j> <j> <j> <j> <j> <j> <j> 
at this point I'm positioned between the "x" and "1" in "index1 += 1;" 
<x> 
to delete the 2 
<i> 
to get into insert mode 
<2> 
<esc> 
<:wq> 
to quit and save
```

Code after changes:

<img width="616" alt="Screen Shot 2023-05-22 at 4 36 32 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/0e37bd2e-22b0-41d1-a2fa-ec877d30182e">

**Step Five: Run the tests, demonstrating that they fail**

* Now that we made the changes to fix the code in ListExamples, we can run JUnit again to indicate it properly works. 

To do this, the keys used were: 

```
<Ctrl C> 
I copied the Junit javac from week 3 on the cse15 spring website into the terminal first
<Ctrl V> 
paste into terminal
<enter> 
<Ctrl C>
Copied Junit java from week 3 onto cse15 sprin website into the terminal
<ListExamplesTests> 
the file I want to run JUnit On
<enter> 
```
Output of this: 

<img width="1014" alt="Screen Shot 2023-05-22 at 4 38 15 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/b4eb011e-83c8-4ba3-988c-a1c60be9b549">

* This indicates that the code was fixed and all the tests that failed previously is now passing 

**Step Six: Commit and push the resulting change to your Github account.**

* Now that I had fixed my code, I want to commit and push the code that now properly works into my github account. 

I did this using the following keys: 

```
<git add . > 
<enter> 
<git commit -m changed> 
<enter> 
<git push> 
<enter> 
```

The output of these actions is: 

<img width="554" alt="Screen Shot 2023-05-22 at 4 39 12 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/6a9f6324-c45c-46c4-9a5c-46d7448ac07a">

The changes are now officially made and pushed to github! 

<img width="653" alt="Screen Shot 2023-05-22 at 4 40 19 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/a825993e-8f24-4c43-9731-c3fb63c054fb">


Now we had successfully changed our code and fixed it, and commit and push it to git. 
