# Exp-8a
## Title :Daemon Threads
```java
class DaemonThread extends Thread {
    public void run() {
        while (true) {
            System.out.println("Daemon thread running...");
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
            }
        }
    }
}

class UserThread extends Thread {
    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println("User thread iteration: " + i);
            try {
                Thread.sleep(1000);
            } catch (InterruptedException e) {
            }
        }
    }
}

public class TestDaemon {
    public static void main(String[] args) {
        UserThread userThread = new UserThread();
        DaemonThread daemonThread = new DaemonThread();
        daemonThread.setDaemon(true);
        userThread.start();
        daemonThread.start();
        System.out.println("Main thread ends...");
    }
}
```
# OUTPUT
![output of TestDaemon](DaemonThread.png)

