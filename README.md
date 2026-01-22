# Experiment1a
## Title : Display Primitive Data Types
```java
public class Defaultvalues{
byte b;
short s;
int i;
long l;
float f;
double d;
char c;
boolean bool;
public static void main(String []args){
Defaultvalues obj=new Defaultvalues();
System.out.println("Default values of primitive data types:");
System.out.println("Default byte value:"+obj.b);
System.out.println("Default short value:"+obj.s);
System.out.println("Default int value:"+obj.i);
System.out.println("Default long value:"+obj.l);
System.out.println("Default float value:"+obj.f);
System.out.println("Default double value:"+obj.d);
System.out.println("Default char value:"+obj.c);
System.out.println("Default boolean value:"+obj.bool);
}
}
```
# output
![output of primitive](primitive.png)
## Title :Quadratic Equation
```java
import java.util.Scanner;
public class QuadraticEqn{
public static void main(String []args){
Scanner sc=new Scanner(System.in);
System.out.println("Enter coefficient a:");
double a=sc.nextDouble();
System.out.println("Enter coefficient b:");
double b=sc.nextDouble();
System.out.println("Enter coefficient c:");
double c=sc.nextDouble();
double D=b*b-4*a*c;
System.out.println("Discriminate:"+D);
if(D>0){
System.out.println("Roots are real and distint.");
double root1=(-b+Math.sqrt(D))/(2*a);
double root2=(-b-Math.sqrt(D))/(2*a);
System.out.println("Root 1:"+root1);
System.out.println("Root 2:"+root2);
}
else if(D==0){
System.out.println("Roots are real and equal.");
double root=-b/(2*a);
System.out.println("Root:"+root);
}
else{
System.out.println("Roots are complex and imaginary.");
double realpart=-b/(2*a);
double imaginarypart=Math.sqrt(-D)/(2*a);
System.out.println("Root 1:"+realpart+"+i"+imaginarypart);
System.out.println("Root 2:"+realpart+"-i"+imaginarypart);
}
}
}
```
# output
![output of primitive](Quad.png)






# Experiment-2-java
## 2a
### Title : MY Class
```java
class Myclass{
void displayMessage(){
System.out.println("welcome to java class mechanism program");
}
int add(int a,int b){
return a+b;
}
public static void main(String []args){
Myclass obj=new Myclass();
obj.displayMessage();
int result=obj.add(10,20);
System.out.println("Sum of two numbers:"+result);
}
}

```
# OUTPUT
![output of Myclass](Myclass.png)

# 2b
## Title :OverloadExample
```java

class OverloadExample{
int add(int a,int b){
return a+b;
}
double add(double a,double b){
return a+b;
}
int add(int a,int b,int c){
return a+b+c;
}
public static void main(String []args){
OverloadExample obj=new OverloadExample();
int sumTwoInts=obj.add(10,20);
double sumTwoDoubles=obj.add(5.5,4.5);
int sumThreeInts=obj.add(1,2,3);
System.out.println("Result of adding two integers:"+sumTwoInts);
System.out.println("Result of adding two double values:"+sumTwoDoubles);
System.out.println("Result of adding three integers:"+sumThreeInts);
}
}

```
# OUTPUT
![output of OverloadExample](Overload.png)
# 2c
## Title :To implement Constructor
```java
class Student{
String name;
int age;
int marks;
Student(String n,int a,int m){
name=n;
age=a;
marks=m;
}
void display(){
System.out.println("Name:"+name);
System.out.println("Age:"+age);
System.out.println("Marks:"+marks);
}
}
class Main{
public static void main(String []args){
Student s1=new Student("Alice",20,85);
s1.display();
}
}

```


# OUTPUT
![output os student](Student.png)






