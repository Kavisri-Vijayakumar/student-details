import java.util.Scanner;
class Student {
    private String name;
    private int rollNumber;
    private int age;
    public void create() {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter name: ");
        this.name = scanner.nextLine();
        System.out.print("Enter roll number: ");
        this.rollNumber = scanner.nextInt();
        System.out.print("Enter age: ");
        this.age = scanner.nextInt();
    }
    public void display() {
        System.out.println("Name: " + this.name);
        System.out.println("Roll number: " + this.rollNumber);
        System.out.println("Age: " + this.age);
    }
}
public class JavaApplication16 {
    public static void main(String[] args) {
        Student[] students = new Student[2];
        for (int i = 0; i < students.length; i++) {
            students[i] = new Student();
            students[i].create();
        }
        System.out.println("\nStudent Details:");
        for (int i = 0; i < students.length; i++) {
            System.out.println("Student " + (i + 1) + ":");
            students[i].display();
            System.out.println();
        }
    }
} 

Output

run:
Enter name: kavi
Enter roll number: 45
Enter age: 18
Enter name: sri
Enter roll number: 25
Enter age: 18

Student Details:
Student 1:
Name: kavi
Roll number: 45
Age: 18

Student 2:
Name: sri
Roll number: 25
Age: 18
