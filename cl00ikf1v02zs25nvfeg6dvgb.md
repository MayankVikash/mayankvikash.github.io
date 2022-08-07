## Report Card Program in Java

I learned Java last semester, so I thought I should make a project.
I searched on Google for Java projects and I found:

**Write a program to take marks of 2 subjects from the user and display the Total, Percentage, Highest Marks, Average, and Remarks.
**
It was not that tough, so this is how I made it.

First, I imported this library for taking input from users:
```
import  java.util.Scanner;
```

Then, I created the file named ‘marks’. I know this file name doesn’t make sense but it’s ok.

Java starting Template:
```
public  class  marks {
public  static  void  main(String  args[]) { 
    // Code Here
    }
}
```

Starting with my code, I defined Scanner Class a variable ‘sc’ to make it easy to get input from the user

```
try (Scanner  sc = new  Scanner(System.in)) {
	// Code Here
}
```

I put the above variable in ‘try’ because Visual Studio was giving errors.

Next, I displayed in the console what I want from them:

```
System.out.println("Enter the marks of 2 subjects (out of 100)");
```
Then, I asked the two inputs from the user

```
System.out.println("Enter the marks of subject 1:");  
int  sub1 = sc.nextInt();

System.out.println("Enter the marks of subject 2:");
int  sub2 = sc.nextInt();
```

‘sc’ is the variable name that I declared above and nextInt() is the function for accepting the values in an integer which will be stored in the variable ‘sub1’ and ‘sub2’ respectively.

Okay, here comes the important step, as you know you can’t score more than 100 in a subject, doesn’t matter how brilliant you are. So, I have to make sure that, the user can’t add numbers greater than 100.

This condition makes sure that the entered value is less than or equal to 100.

```
if (sub1 <= 100 && sub2 <= 100) {
    // This code will be executed if the condition is true
} else{
    // This code will be executed if the condition if false
}
```
Wow, great! All the measures are taken, users also can’t give any other input except number, if they try, they will get an error.

Now time for the real code:

```
int  total = sub1 + sub2;
System.out.println("Total = " + total);
```
This will add the two values and print the Total.

This code will find the percentage, just take the total, divide it by 200 (because there are 2 subjects so total marks will be 200) then, multiply it by 100. Simple.

Note: ‘float’ is used because the answer may be in decimal and it is also multiplied by ‘float’ to covert it into float datatype. How to convert Integer into Float.

```
float  percent = (float) total / 200 * 100;
System.out.println("Percentage = " + percent);
```
Then, a simple if-else statement to get the highest number:

```
if (sub1 > sub2) {
System.out.println("Highest marks scored is " + sub1);
} else {
System.out.println("Highest marks scored is " + sub2);
}
```

For finding the average, just take the total and divide it by 2:

```
float  avg = (float) total / 2;
System.out.println("Average is " + avg);
```
Then, again an if-else to display remarks. If the mark is 50 or less than that, then it will display ‘You need to work hard!’. If the marks are above 80 or equal and less than 90 then it will show ‘Good Marks’, if it is above 90 then it will show ‘Excellent’. Pretty Simple.

```
if (percent <= 50) {
System.out.println("Remarks: You need to work hard!");
} else  if (percent >= 80 && percent <= 90) {
System.out.println("Remarks: Good Marks :)");
} else  if (percent >= 90) {
System.out.println("Remarks: Excellent");
} else {
System.out.println("Remarks: Good");
}
```
So, that’s how I made it. It was really fun. By the way, thanks for visiting and reading :)

Source Code:
import  java.util.Scanner;

  

```
public  class  marks {

public  static  void  main(String  args[]) {

  

try (Scanner  sc = new  Scanner(System.in)) {

  

System.out.println("Enter the marks of 2 subjects (out of 100)");

  

System.out.println("Enter the marks of subject 1:");

int  sub1 = sc.nextInt();

  

System.out.println("Enter the marks of subject 2:");

int  sub2 = sc.nextInt();

  

if (sub1 <= 100 && sub2 <= 100) {

  

// Total

  

int  total = sub1 + sub2;

System.out.println("Total = " + total);

  

// Percentage

  

float  percent = (float) total / 200 * 100;

System.out.println("Percentage = " + percent);

  

// Highest Marks

  

if (sub1 > sub2) {

System.out.println("Highest marks scored is " + sub1);

} else {

System.out.println("Highest marks scored is " + sub2);

}

  

// Average

  

float  avg = (float) total / 2;

System.out.println("Average is " + avg);

  

// Remarks

if (percent <= 50) {

System.out.println("Remarks: You need to work hard!");

} else  if (percent >= 80 && percent <= 90) {

System.out.println("Remarks: Good Marks :)");

} else  if (percent >= 90) {

System.out.println("Remarks: Excellent");

} else {

System.out.println("Remarks: Good");

}

  

} else {

System.out.println("Values are Greator!");

}

  

}

  

}

  

}
```


Wow great! I am able to make it but it looks a little bit easy, let’s add some complex things.

Write a program to take marks of 15 subjects from the user and display the Total, Percentage, Highest Marks, Average, and Remarks. It should also work if the number of subjects is less than 15.

I have published this program on my website, don't worry it doesn't have any ads. You can check out the program for 15 subjects here: https://mayankvikash.ml/posts/simple-report-card-in-java.html


Originally Published at [https://mayankvikash.ml/posts/simple-report-card-in-java.html](https://mayankvikash.ml/posts/simple-report-card-in-java.html)

Check out other posts: [https://mayankvikash.ml/posts/](https://mayankvikash.ml//posts/)

Latest updates: [https://mayankvikash.ml//news/](https://mayankvikash.ml//news/)

HTML Sitemap: [https://mayankvikash.ml/sitemap.html](https://mayankvikash.ml/sitemap.html) 

Sitemap: [https://mayankvikash.ml/sitemap.xml](https://mayankvikash.ml/sitemap.xml)

Made by [Mayank Vikash](https://mayankvikash.ml/)

