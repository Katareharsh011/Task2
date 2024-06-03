package Task1;
import java.util.Scanner;
public class task2code

     {
        public static void main(String[] args) {
            Scanner scanner = new Scanner(System.in);

            // Input: Take marks obtained (out of 100) in each subject.
            System.out.println("Enter the number of subjects:");
            int numSubjects = scanner.nextInt();

            int totalMarks = 0;

            // Input marks for each subject and calculate total marks
            for (int i = 1; i <= numSubjects; i++) {
                System.out.println("Enter marks obtained in subject " + i + ":");
                int marks = scanner.nextInt();
                totalMarks += marks;
            }

            // Calculate Total Marks
            System.out.println("Total Marks: " + totalMarks);

            // Calculate Average Percentage
            double averagePercentage = (double) totalMarks / numSubjects;
            System.out.println("Average Percentage: " + averagePercentage + "%");

            // Grade Calculation: Assign grades based on the average percentage achieved.
            char grade;
            if (averagePercentage >= 90) {
                grade = 'A';
            } else if (averagePercentage >= 80) {
                grade = 'B';
            } else if (averagePercentage >= 70) {
                grade = 'C';
            } else if (averagePercentage >= 60) {
                grade = 'D';
            } else {
                grade = 'F';
            }

            // Display Results
            System.out.println("Grade: " + grade);

            scanner.close();
        }
    }
