# Chapter 1: The very basics
A Java program can be seen as a set of instructions that you (the programmer) give to a computer for execution.  
You tell it to do some task and it will try to do as instructed. We use the word "_try_" since what you ask can be something illogic or impossible. 

## Print Hello World
The most common cliché when introducing a programming tutorial is to print Hello World. That is we instruct the computer to print the message "Hello World" in the console:

```java
class SayHello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
Don't be intimidated by these strange things, we will explain all of them later. What matters here is the line:
```java
System.out.println("Hello World!");
```
Do not pass over the **;** at the end of the line. You may have noticed that we surrounded our message with quotes **""**. And yes, if we wanted the computer to rather print **Salutations** instead we could have done:
```java
System.out.println("Salutations");
```

But let's go back to the basics.

## Install VS Code
Visual Studio Code is a free tool to write and execute programs in many languages (it can do many other things).
You can use this page to install it and configure the needed Java environment: https://code.visualstudio.com/docs/java/java-tutorial

From now we will assume you have a functioning VS Code with Java correctly configured as in the tutorial. Or you can just use the online compiler: https://www.jdoodle.com/online-java-compiler/

## Types
To be able to correclty understand our instructions, we need a way to tell the machine that something is a text to be printed or emailed or anything else. Or that it is a price to be computed, or that it is a **boolean** that can be either true or false. For this we have the notion of **types**. We will avoid theory by now, and only say that types are a way of grouping values together:  
We say that the above values **"Hello World"** and **"Salutations"** are of type _String_.  
Truth values **true** and **false** are _boolean_  
Integers like **0**, **42** and **-1500** are _int_

## Variables
Like in elementary maths, we need variables that store values of some types:
```java
String message;
```
Here we declared a variable named message and of type String. We can assign values to our variables:
```java
message = "Hello World";
```

So the pattern for declaring a variable is: __TYPE variableName;__:
```java
String message;
int age;
boolean isTheWeatherGood;
```
And we assign values to variables using __=__:
```java
message = "Hello World";
age = 30;
isTheWeatherGood = true;
```

> Note that since we declared __age__ as __int__ we can not assign to it non integer values. We will get an error (called compiler error, later on that) if we do following:
```java
age = "thirty";
```

And it's good to know that we can combine both declaration and assignment of variables and values:

```java
String message = "Hello World";
int age = 30;
boolean isTheWeatherGood = true;
```

We can use these variables to print their values to the console, like we did for our **Hello Wolrd**. Here is a complete example:

```java
public class MyClass {
    public static void main(String args[]) {
        String message = "Hello World";
        int age = 30;
        boolean isTheWeatherGood = true;
        
        System.out.println(message);
        System.out.println(age);
        System.out.println(isTheWeatherGood);
    }
}
```
> As mentioned above, don't bother with the first two lines that start with **public** we will explain them later. 

If you copy this code and execute it, it will print :
> Hello World  
> 30  
> true


## Operators
We just saw how to assign values to variables using the __=__ operator. Other simple operators include:

- Addition: **+**
- Subtraction: **-**
- Multiplication: **\***
- Division: **/**

And so we can use them like this:
```java
public class MyClass {
    public static void main(String args[]) {
        int x = 10;
        int y = 2;
        
        int sum = x + y;
        int product = x * y;
        int difference = x - y;
        int quotient = x / y;

        System.out.println(sum);
        System.out.println(product);
        System.out.println(difference);
        System.out.println(quotient);
    }
}
```

Executing this little porgram will print:
> 12  
> 20  
> 8  
> 5  

We can use the operator **+** to concatenate Strings:
```java
String greeting = "Hello " + "Nell";
```
or like this:
```java
String hello = "Hello ";
String name = "Nell";
String greeting = hello + name;
```
And so the variable greeting will have the value = __Hello Nell__  
