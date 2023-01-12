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

From now we will assume you have a functioning VS Code with Java correctly configured as in the tutorial.

## Types
To be able to correclty understand our instructions, we need a way to tell the machine that something is a text to be printed or emailed or anything else. Or that it is a price to be compted, or that it is a **boolean** that can be either true or false. For this we have the notion of **types**. We will avoid theory by now, nd only say that types are a way of grouping values together:  
We say that the above values **"Hello World"** and **"Salutations"** are of type _String_.  
Truth values **true** and **false** are _boolean_  
Integers like **0**, **42** and **-1500** are _int_