# Servelet-Login-page
Sure, here's a comprehensive README for your GitHub repository:

---

# Employee Payroll System

## Overview
This project is a Java-based application designed to manage employee payrolls for both full-time and part-time employees. It includes functionalities to add, remove, and display employee details, as well as calculate salaries.

## Features
- **Abstract Class `Employee`**: Base class with common attributes `id` and `name`, and an abstract method `calculateSalary`.
- **`FullTimeEmployee` Class**: Extends `Employee` and includes `monthlySalary`. Implements the `calculateSalary` method.
- **`PartTimeEmployee` Class**: Extends `Employee` and includes `hoursWorked` and `rate`. Implements the `calculateSalary` method.
- **`PayRollSystem` Class**: Manages a list of `Employee` objects. Provides methods to add, remove, and display employees.

## Usage
### Adding Employees
```java
PayRollSystem PS = new PayRollSystem();
FullTimeEmployee FE = new FullTimeEmployee("Sarfaraz Essa", 9, 100000);
PartTimeEmployee PE = new PartTimeEmployee("Amir Essa", 8, 6, 500);
PS.addEmployee(FE);
PS.addEmployee(PE);
```

### Displaying Employees
```java
PS.displayEmployee();
```

### Removing Employees
```java
PS.removeEmployee(9); // Removes employee with ID 9
```

## Example
Here's a sample usage of the program:
```java
public class Main {
    public static void main(String[] args) {
        PayRollSystem PS = new PayRollSystem();
        FullTimeEmployee FE = new FullTimeEmployee("Sarfaraz Essa", 9, 100000);
        PartTimeEmployee PE = new PartTimeEmployee("Amir Essa", 8, 6, 500);
        PS.addEmployee(FE);
        PS.addEmployee(PE);
        System.out.println("Initially, detail of employees:");
        PS.displayEmployee();
        System.out.println("After removal, detail is:");
        PS.removeEmployee(9);
        PS.displayEmployee();
    }
}
```

## How to Run
1. Compile the Java files:
   ```bash
   javac Employee.java FullTimeEmployee.java PartTimeEmployee.java PayRollSystem.java Main.java
   ```

2. Run the `Main` class:
   ```bash
   java Main
   ```

## Contributions
Contributions are welcome! Feel free to fork this repository, submit issues, or create pull requests.
