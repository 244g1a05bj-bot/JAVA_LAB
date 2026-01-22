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



