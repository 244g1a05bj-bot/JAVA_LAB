# Exp-7a
## Title : Creation of User Defined Exception
```java
import java.util.Scanner;
class InvalidCountryException extends Exception {

    InvalidCountryException() {
        super();
    }


    InvalidCountryException(String message) {
        super(message);
    }
}
class UserRegistration {
    void registerUser(String username, String userCountry) 
            throws InvalidCountryException {

        if (!userCountry.equalsIgnoreCase("India")) {
            throw new InvalidCountryException(
                "User outside India cannot be registered."
            );
        } else {
            System.out.println("User registered successfully.");
        }
    }
}
public class  UserRegion {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        try {
            System.out.print("Enter the user name: ");
            String uname = sc.nextLine();
            System.out.print("Enter the country name: ");
            String ucountry = sc.nextLine();
            UserRegistration ur = new UserRegistration();
            ur.registerUser(uname, ucountry);
        } 
        catch (InvalidCountryException e) {
            System.out.println(e.getMessage());
        } 
        catch (Exception e) {
            System.out.println("Unknown error: " + e);
        } 
        finally {
            sc.close();
            System.out.println("Finally block executed successfully.");
            System.out.println("Program terminated properly.");
        }
    }
}
```
# OUTPUT
![output of UserRegion](UserRegion.png)

# Exp-7b
## Title : Create Threads by Extending Thread class
```java
 //Thread 1
class GoodMorningThread extends Thread {
    public void run() {
        try {
            while(true) {
                System.out.println("Good Morning");
                Thread.sleep(1000);
            }
        }
        catch(InterruptedException e) {
            System.out.println(e);
        }
    }
}

// Thread 2
class HelloThread extends Thread {
    public void run() {
        try{
            while(true) {
                System.out.println("Hello");
                Thread.sleep(2000);
            }
        }
        catch(InterruptedException e) {
            System.out.println(e);
        }
    }
}

// Thread 3
class WelcomeThread extends Thread {
    public void run() {
        try {
            while(true) {
                System.out.println("Welcome");
                Thread.sleep(3000);
            }
        }
        catch(InterruptedException e) {
            System.out.println(e);
        }
    }
}

// Main class
public class TestThreads {
    public static void main(String[] args) {
        GoodMorningThread t1 = new GoodMorningThread();
        HelloThread t2 = new HelloThread();
        WelcomeThread t3 = new WelcomeThread();
        t1.start();
        t2.start();
        t3.start();
    }
}
```
# OUTPUT
![output of TestThreads](TestThreads.png)

# Exp-7c
## Title : Illustrating is Alive and Join scenario
```java

class LongRunningTask extends Thread {
    public void run() {
        try {
            System.out.println("Long running task started...");
            for(int i = 1; i <= 5; i++)
            {
                System.out.println("Working... " + i);
                Thread.sleep(1000);
            }
            System.out.println("Long running task completed!");
        }
        catch(InterruptedException e){
            System.out.println(e);
        }
    }
}
public class ThreadDemo {
    public static void main(String[] args) {
        LongRunningTask task1 = new LongRunningTask();
        System.out.println("Before starting task1: " + task1.isAlive());
        task1.start();
        System.out.println("After starting task1: " + task1.isAlive());
        try  {
            System.out.println("Main thread waiting for task1 to complete using join()...");
            task1.join();
        }
        catch(InterruptedException e)  {
            System.out.println(e);
        }
        System.out.println("After join(): " + task1.isAlive());
        System.out.println("Main thread continues after task1 completed");
    }
}
```
# OUTPUT
![output of ThreadDemo](ThreadDemo.png)
