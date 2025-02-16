// date (13/02/25)

// Parent class Employee
class Employee {
    int id;
    String name;

    // Constructor to initialize Employee
    public Employee(int id, String name) {
        this.id = id;
        this.name = name;
    }

    // Method to display employee details
    public void display() {
        System.out.println("Employee ID: " + id);
        System.out.println("Employee Name: " + name);
    }
}

// Child class HR that inherits Employee
class HR extends Employee {
    double salary;

    // Constructor to initialize HR 
    public HR(int id, String name, double salary) {
        super(id, name); // Calling the constructor of the parent class Employee
        this.salary = salary;
    }

    // Method to display HR details, including salary
    public void display() {
        super.display();
        System.out.println("Employee Salary: " + salary);
    }
}

// Child class SoftwareEngineer that inherits Employee
class SoftwareEngineer extends Employee {
    double salary;

    // Constructor to initialize SoftwareEngineer
    public SoftwareEngineer(int id, String name, double salary) {
        super(id, name); // Call the constructor of the parent class Employee
        this.salary = salary;
    }

    // Method to display SoftwareEngineer details, including salary
    public void display() {
        System.out.println("Employee Salary: " + salary);
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating HR employee
        HR hrEmployee = new HR(283, "Md. Ijaj Hakim Arfique", 50000.0);
        // Creating Software Engineer employee
        SoftwareEngineer seEmployee = new SoftwareEngineer(284, "Mahamub", 70000.0);

        // Displaying HR employee details
        hrEmployee.display();

        // Displaying Software Engineer employee details
        seEmployee.display();
    }
}
