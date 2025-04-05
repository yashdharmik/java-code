# java-code
abstract class Employee {
    String name;
    int id;

    Employee(String name, int id) {
        this.name = name;
        this.id = id;
    }

    abstract void displayDetails();
}

class Manager extends Employee {
    double salary;

    Manager(String name, int id, double salary) {
        super(name, id);
        this.salary = salary;
    }

    void displayDetails() {
        System.out.println("Manager Name: " + name + ", ID: " + id + ", Salary: " + salary);
    }
}

class Developer extends Employee {
    String programmingLanguage;

    Developer(String name, int id, String programmingLanguage) {
        super(name, id);
        this.programmingLanguage = programmingLanguage;
    }

    void displayDetails() {
        System.out.println("Developer Name: " + name + ", ID: " + id + ", Language: " + programmingLanguage);
    }
}

public class Main {
    public static void main(String[] args) {
        Employee manager = new Manager("Alice", 1, 75000);
        Employee developer = new Developer("Bob", 2, "Java");

        manager.displayDetails();
        developer.displayDetails();
    }
}
