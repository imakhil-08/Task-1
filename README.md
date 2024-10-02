
# task 1


import java.util.ArrayList;
import java.util.Scanner;

public class StudentGrades {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Double> grades = new ArrayList<>();

        System.out.println("Enter the number of students:");
        int numStudents = scanner.nextInt();
        scanner.nextLine(); // Consume newline left-over

        for (int i = 0; i < numStudents; i++) {
            System.out.println("Enter grade for student " + (i + 1) + ":");
            double grade = scanner.nextDouble();
            grades.add(grade);
        }

        double sum = 0;
        double highest = grades.get(0);
        double lowest = grades.get(0);

        for (double grade : grades) {
            sum += grade; h 
            if (grade > highest) {
                highest = grade;
            }
            if (grade < lowest) {
                lowest = grade;
            }
        }

        double average = sum / numStudents;

        System.out.println("Average grade: " + average);
        System.out.println("Highest grade: " + highest);
        System.out.println("Lowest grade: " + lowest);
    }
}
