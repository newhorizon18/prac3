# Experiment No. 3

## Title: Programs on Various Types of Inheritance and Exception Handling

## 1. Program Code

### A. Single Inheritance

**File Name: Main.java**

```java
class Vehicle {

    Vehicle() {
        System.out.println("This is a Vehicle");
    }
}

class Car extends Vehicle {

    Car() {
        System.out.println("This Vehicle is Car");
    }
}

public class Main {

    public static void main(String[] args) {

        Car obj = new Car();
        obj.getClass();
    }
}
```

### Output

```text
This is a Vehicle
This Vehicle is Car
```

---

### B. Multilevel Inheritance

**File Name: Main.java**

```java
class Vehicle {

    Vehicle() {
        System.out.println("This is a Vehicle");
    }
}

class FourWheeler extends Vehicle {

    FourWheeler() {
        System.out.println("4 Wheeler Vehicles");
    }
}

class Car extends FourWheeler {

    Car() {
        System.out.println("This 4 Wheeler Vehicle is a Car");
    }
}

public class Main {

    public static void main(String[] args) {

        Car obj = new Car();
    }
}
```

### Output

```text
This is a Vehicle
4 Wheeler Vehicles
This 4 Wheeler Vehicle is a Car
```

---

### C. Hierarchical Inheritance

**File Name: Test.java**

```java
class Vehicle {

    Vehicle() {
        System.out.println("This is a Vehicle");
    }
}

class Car extends Vehicle {

    Car() {
        System.out.println("This Vehicle is Car");
    }
}

class Bus extends Vehicle {

    Bus() {
        System.out.println("This Vehicle is Bus");
    }
}

public class Test {

    public static void main(String[] args) {

        Car obj1 = new Car();
        Bus obj2 = new Bus();
        obj1.getClass();
        obj2.getClass();
    }
}
```

### Output

```text
This is a Vehicle
This Vehicle is Car
This is a Vehicle
This Vehicle is Bus
```

---

### D. Exception Handling

**File Name: Test.java**

```java
import java.util.Scanner;

class InvalidAgeException extends Exception {

    public InvalidAgeException(String msg) {
        super(msg);
    }
}

public class Test {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        try {
            System.out.print("Enter your age: ");
            int age = sc.nextInt();

            if (age < 0) {
                throw new InvalidAgeException("Age cannot be negative!");
            } else if (age < 18) {
                throw new InvalidAgeException("You must be 18 or above to vote.");
            }

            System.out.println("You are eligible to vote.");
        } catch (InvalidAgeException ie) {
            System.out.println("Error: " + ie.getMessage());
        } catch (Exception e) {
            System.out.println("Invalid input! Please enter a valid number.");
        } finally {
            System.out.println("Thank you for using the system.");
            sc.close();
        }
    }
}
```

### Output

**Example 1: Valid Age**

```text
Enter your age: 20
You are eligible to vote.
Thank you for using the system.
```

**Example 2: Invalid Age**

```text
Enter your age: 16
Error: You must be 18 or above to vote.
Thank you for using the system.
```

---

## 2. Aim

To write Java programs demonstrating single inheritance, multilevel inheritance, hierarchical inheritance, and exception handling.

## 3. Theory

- **Inheritance:** Allows one class to acquire the properties and methods of another class.
- **Single Inheritance:** One child class inherits from one parent class.
- **Multilevel Inheritance:** A class inherits from another derived class.
- **Hierarchical Inheritance:** Multiple child classes inherit from the same parent class.
- **extends Keyword:** Used to inherit one class from another.
- **getClass():** Returns the runtime class of an object.
- **Exception Handling:** Handles errors during program execution.
- **try:** Contains statements that may generate exceptions.
- **catch:** Handles exceptions and displays error messages.
- **finally:** Executes whether an exception occurs or not.
- **throw:** Used to throw an exception explicitly.

## 4. Conclusion

Thus, Java programs demonstrating single inheritance, multilevel inheritance, and hierarchical inheritance were successfully implemented.

Exception handling was also demonstrated using try, catch, finally, and throw statements to handle invalid user input.
