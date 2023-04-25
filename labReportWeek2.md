## LAB REPORT 2 <br> Danielle Dang 
<br>
Part 1: Creating a server called String Server that keeps track of requests! 

What should this server do? It should store and keep track of a string that gets added onto by more strings through the means of requests. 

In order to achieve this, my code looks like this: 

<img width="807" alt="Screen Shot 2023-04-24 at 4 26 48 PM" src="https://user-images.githubusercontent.com/130107069/234136803-e9938e77-19b7-4f2f-b086-1719c362018c.png">

Notes on what the code does: 
* I first created String variable that starts as a empty string (this is where I will add the String requests and store them
* the command line/url argument is then split from the "=" if the keyword "/add-message" is given
* together is then updated to whatever together previously was plus the new string given in the URL
* together is then returned 
* if theres no key "\add-message" a error message is then returned 
* The code in StringServer class functions to start the server itself 

The server:

<img width="500" alt="Screen Shot 2023-04-24 at 4 24 55 PM" src="https://user-images.githubusercontent.com/130107069/234136592-387679c0-f312-443a-a273-3fe4e1a6282a.png">

Note the url is: "http://localhost:4000/add-message?s=Hello", if we trace the code with the input above in the URL, the handleRequest method is called. It notices that the key "/add-message" is found and enters the if statement. At this point, because this is the first time ".\add-message" is found, together is still an empty string. However, it is now updated with the given "Hello" that was found after the "=" in the URL. the variable together now equals "Hello"

<img width="546" alt="Screen Shot 2023-04-24 at 4 25 14 PM" src="https://user-images.githubusercontent.com/130107069/234136628-30f7c11b-e2f9-434a-acb1-e5cf8aa5a8be.png">

Note the url this time is: http://localhost:4000/add-message?s=Pineapples. Similarily, the method handleRequest is found and the URL is given as it's paramenter. The keyword is found and it prints out the word after the "=" (or the first index after you split the URL string). Note from the previous section, together is currently "Hello", but with the new String found after the "=" in the URL, its updated to "Hello + "\n" + Pineapples" (the "\n" prints out a new line). The updated String stored in together is then shown on the server page.

<img width="471" alt="Screen Shot 2023-04-24 at 4 25 45 PM" src="https://user-images.githubusercontent.com/130107069/234136683-422f4c9a-f699-4168-add5-baa4b93ae3ea.png">
Note the url this time is: http://localhost:4000/add-message?s=Cherry. Similarily, the method handleRequest is found and the URL here is the argument passed into it. The key "/add-message" is found so the URL is passed into the if statement. it seems that the first argument has an s so it enters another if statement. Together is then updated to "Hello + "\n" + "Pineapples" + "\n" + "Cherry", and it's returned and shown on the server. 

<img width="411" alt="Screen Shot 2023-04-24 at 4 26 29 PM" src="https://user-images.githubusercontent.com/130107069/234136761-c95292f0-6386-434a-809f-617aeecc531b.png">
Note the url this time is: http://localhost:4000/. The URL is passed into the handleRequest method, but this time it doesn't see the key "/add-message" and doesn't enter the if statement. Due to the fact that it doesn't enter the if statement, the String variable is not updated and stays as "Hello + "\n" + "Pineapples" + "\n" + "Cherry". Instead of going into the if statement, it would just return "404 Not Found!" as seen in the screenshot. 



Part 2: bugs! 

In lab, one of the methods we had to debug was:
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
The method itself is supposed to return a new array with all the elements in the integer array (arr) inside the parameters, but in reversed order. 

With this being said, its expected that this test should pass using Junit: 
```
  @Test
  public void testReverses1(){
    int[] input2 = {1,2,3};
    assertArrayEquals(new int[] {3,2,1}, ArrayExamples.reversed(input2));
  }
 ```
 What does this code mean: 
 * What the assertArrayEquals method is checks if the expected value matches the actual value. In this case the integer array 
```
    int[] input2 = {1,2,3};
  }
```
is passed into the reversed method. If the method works as intended, the output should be a new integer array with the elements {3,2,1} in their respective order. However, this test had failed which is indicated by Junit with this message:
<img width="425" alt="Screen Shot 2023-04-22 at 12 23 16 PM" src="https://user-images.githubusercontent.com/130107069/233802789-97da4872-f88b-45f8-aa67-3b1552ee38b7.png">
<img width="641" alt="Screen Shot 2023-04-22 at 12 23 43 PM" src="https://user-images.githubusercontent.com/130107069/233802803-cf8790f5-7206-4991-bfc2-2c6f59fad904.png">

**Note: the output given by Junit can be viewed as a symptom of the bug. The symptom itself is the output from code with bugs. 

**What does this mean?** there's a bug in the code for reversed!

However, this is a test that doesn't fail when passed through Junit:
```
  @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
Why did this pass? My best guess as to why this test passed, while the other one failed is because this is testing reversed with an empty array. This test is definately not as strong as the one before, given the empty list thats passed through. Furthermore, it's hard to make a definitive conclusion that a method is properly implemented if the input is empty, and the expected output is also an empty list. It could easily be the case that the code didn't change/do anything to the list, but the programmer has no way of knowing this if the expected value returned is the same as the input. 

**Changes made to fix the code**
For comparison and ease in seeing the bug this is the code before the changes (with the bugs):
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
and this is the code with no bugs and the proper implementaion that passes the tests: 
```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1;
    }
    return newArray;
  }
```
The bug in the initial implementation of reversed was very small and can easily be overlooked. All that needed to change was the last few lines in the code. To further explain, the top half is done right (a new integer array is made of the same length of the input array, and you want a for loop that starts from 0, and increment by 1 until the length of arr is reached). However, this piece of code: 
```
arr[i] = newArray[arr.length - i - 1];
```
is actually replacing each integer element from the input array with the elements in the new empty array created. This would result in an empty array, hence the failed tests we saw earlier. Therefore that segment of code should look like this instead: 
```
newArray[i] = arr[arr.length - i - 1;
```
Each iteration of the for loop would now assign the proper integer values into the new array from the input array, which is what we want to do. 

Additionally, another change created is seen at the return statement. 

The original code with bugs had this: 
```
return arr;
```
return arr means that it's returning the input array rather than the new array with the same integer values reversed. A small fix such as this: 
```
return newArray;
```
would then properly return the reversed array. 

With the change the Junit test now successfully passed. 

**Part 3: What I learned in lab 2 and 3!**

My understanding of web servers and how to run them was extremely limited before lab 2 and lab 3. I had never opened/built a web server myself and write code to manipulate what shows up in the web page. I specifically learned how to start a web server (this involves understanding what a port and local host was), how to access URLS from the command line using the curl and see the web page's contents from the terminal, and so much more. I also learned a little more about debugging and the sepcific terms and aspects of it. Beforehand, my understanding of debugging was very broad and my general view on it was that debugging was just fixing code that doesn't work. However with week 3's lectures and lab 3, I now understand that a symptom is the output from the bug, a failure inducing output is the input that caused the error and leads to the symptom, and a bug is the program that causes the failure itself. 
