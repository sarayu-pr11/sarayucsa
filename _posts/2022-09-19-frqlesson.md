---
description: Methods and Control Structures
title: AP FRQ Lesson
toc: true
layout: post
categories: [markdown]
comments: true
---

# FRQ Lesson: Methods and Control Structures
## Methods
A method is something to be declared within a class. It only runs when it is called and you can pass parameters in a method. Methods are used to perform functions, and they are helpful since you can reuse code.

### Calling a method
```
public class Main {
    static void myMethod() {
        //code to be executed
    }
}

```
### Initializing a Method
```
private static void myFunction() {
    // function body
   }
```

### CB Example
![image](https://user-images.githubusercontent.com/55467797/191194118-5d0fae8d-e46f-4d89-ac9f-205ca615047e.png)

## Control Structures
### If/Else/Else If
```
if (count > 5) {
    System.out.println("Count is higher than 5");
    }
    else if (count > 2) {
    System.out.println("Count is higher than 2");
    }
    else {
    System.out.println("Count is lower than 2");
    }
```


### Switch 
```
int count = 3;
switch (count) {
case 0:
    System.out.println("Count is equal to 0");
    break;
case 1:
    System.out.println("Count is equal to 1");
    break;
default:
    System.out.println("Count is either negative, or higher than 1");
    break;
}
```
### Loops
```
for (int i = 1; i <= 50; i++) {
    methodToRepeat();
}

int whileCounter = 1;
while (whileCounter <= 50) {
    methodToRepeat();
    whileCounter++;
}
```
## College Board Requirements
College board questions will include the following
- a for-loop that probably uses the method’s parameter variables,

- an if statement, probably inside the loop,

- calls to other class methods given to you,

- a numerical or string value that is calculated by the loop and returned at the end of the method.

- if the question has 2 parts, 1 part will probably require a loop and the other just an expression

College board specifically says:
![image](https://user-images.githubusercontent.com/55467797/191193960-031c67a8-4af6-43e1-a896-71b91c25dc2e.png)

#### Helpful Links
[Khan Academy](https://www.khanacademy.org/computing/computer-programming/programming/object-oriented/pt/object-methods)
[AP Live Review](https://www.youtube.com/watch?v=8V4vsRVd-wE)

