# Exp-9a
## Title : Connects a database using JDBC
```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.Statement;

public class Connect {

    public static void main(String[] args) {

        // Database credentials
        String url = "jdbc:mysql://localhost:3306/sharath";
        String username = "root";
        String password = "Sharath@16";   // Change as per your MySQL password

        try {
            // Step 1: Load JDBC Driver (Optional in latest versions)
            Class.forName("com.mysql.cj.jdbc.Driver");

            // Step 2: Establish Connection
            Connection con = DriverManager.getConnection(url, username, password);

                if (con == null)
                System.out.println("Connection is not established");
                else
                System.out.println("Connection is sucessfully established.");
            con.close();

        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
# OUTPUT
![output of Connect](Connect.java)

# Exp-9b
## Title : Create using JDBC
```java

