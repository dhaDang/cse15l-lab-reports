## LAB REPORT 5 <br> Danielle Dang 
<br>

**Part One
Lab Report task: Debugging Scenario 

1) The original post from a student with a screenshot showing a symptom and a description of a guess at the bug 
Student submission:

**What envioronment are you using (computer operating system, web browser, terminal/editor, and so on)?

Hello! I am using my Macbook Pro 14 on Visual Studio Code. I'm trying to run my `hello.java` file that I've created using a bash script `help.sh` that should compile and run it. Everything is being done on the terminal. 

**Detail the symptom you're seeing. Be speicifc; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avvoid saying "it doesnt work".

Right now, I'm trying to run my bash script `help.sh` and use it compile the code from `intro.java`. 
This is what the bash script looks like:
```
#!/bin/bash
javac ../javafile/hello.java
cd ../javafile
java -cp ../javafile hello.java
```

This is what the hello.java file looks like:
```
package javafile;

public class hello {
    public static void main(String [] args){
        System.out.println("hello!");
    }
}
```
However, I looked at past labs and worksheets and to run the bash script I know the command line argument should be `bash help.sh` but it gives me this error: 

<img width="407" alt="Screenshot 2023-06-04 at 1 24 40 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/c7720cb9-a369-4b84-9ce8-4e378619d10e">

**Detail the failure inducing input and context. That might mean any or all of the command you're running, a test case, command line arguments, working directory, even the last cew commands you ran. Do your best to provide as much context as you can. 

I've gone through both the `help.sh` bash script and everything looks like it should work properly! The first line:
```
javac ../javafile/hello.java
```
should compile `hello.java`.
Then the second line:
```
cd ../javafile
```
should go to the parent directory 
and the third line: 
```
java -cp ../javafile hello.java
```
Should run `hello.java`

I expected this to output from the terminal:
```
hello! 
```
but as shown previously, its stating that the file does not exist. I also know that the actual java file `hello.java` works properly because when I manually compile and run the `hello.java` from my file, it works properly:
<img width="410" alt="Screenshot 2023-06-04 at 1 35 31 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/e3320970-041e-404e-8a2d-e7a12089c642">

**1) A response from a TA asking a teading question or suggesting a command to try. 

hello! This sounds like a weird bug. Have you tried looking at your current working directory to see if you're in the proper one where the bash script is? 

Can you send a picture of your files and if theres multiple folders, you can try typing this on your terminal: 
```
pwd 
```
It might be useful to first find out what directory you're in first! 
Hope this helps. 

**2) Another screenshot or terminal output showing what infromation the student got from trying that and a clear description on what the bug is 

Student's folders and files:
<img width="220" alt="Screenshot 2023-06-04 at 1 46 04 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/2c9966ff-b867-4043-be5f-ffb89df05a6b">

Student taking in the input: 
<img width="363" alt="Screenshot 2023-06-04 at 1 46 18 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/cd0b6695-3c65-4c46-a1d6-f2a86986daf0">

**The BUG! 

The student was simply not in the proper directory as the folder `script`. This means that there was no way the terminal had access to `help.sh` which is why the error message: 
```
bash: help.sh: No such file or directory
```
appears. Its a simple but often overlooked bug! 

**3) At the end, all the information needed about the set up: 
* The file and directory structure needed:
The file and directory structure needed is as follows. I made a folder called `LABREPORT` and within that folder I had two other ones called `javafile` and `script`. Inside `javafile` is where the `hello.class` and `hello.java` files are stored. On the other hand, the `script` folder contains the bash script `help.sh`. 

This is what the structure looks like on Visual Studio Code: 
<img width="223" alt="Screenshot 2023-06-04 at 1 56 37 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/3c7ca343-a570-4352-bcb3-3e951d8f3c44">

* The contents of the file before fixing the bug:

This is what `hello.java`looks like:
```
package javafile;

public class hello {
    public static void main(String [] args){
        System.out.println("hello!");
    }
}
```

While this is what the bash script `help.sh` looks like:

```
#!/bin/bash
javac ../javafile/hello.java
cd ../javafile
java -cp ../javafile hello.java
```
* The command line to trigger the bug when first opening the terminal was:
```
bash help.sh
```
* A description of what to edit to fix the bug

This bug was more of a behavioral and set up bug rather than a coding bug within the files itself. WIth this being said, to fix the bug and get the expected outcome, you simply need to enter the proper java file itself in order to call the bash script you want. For instance, in the beginning the student automatically ran `bash help.sh` without first doing `pwd` and checking if they're in the right directory to making that call. If they checked this in the beginning they could type `ls` to see the folders and then `cd script` to get into the folder where `help.sh` is contained. Only then are they able to run `bash help.sh` and get the expected greeting in their terminal:
```
hello!
```

**Part Two 

Reflection:

Coding and command line arguments was an unfamilar topic to me right from the start, before I even entered my first year of college. With this being said, although I've taken a few introduction coding classes like CSE 8A and CSE 8B prior to CSE 15L, I only knew the basic command line arguments like `ls` and `cd`. It's easy to see how I've learned and grown so much since then. Topics such as vim, bash scripts, and debugging were completely unclear to me. However, now at the end of the course, I feel as if I have a solid understanding of each. I didn't consider how versitle and impactful the command line can be, so it was really fun being able to spend some time out of my week in lab playing around with the different commands and learning by actually doing them! 





