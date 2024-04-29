import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;

public class AgeCalculatorBot {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter your birth date (YYYY-MM-DD):");
        String birthDateInput = scanner.nextLine();

        // Parse the input date string to a LocalDate
        LocalDate birthDate = LocalDate.parse(birthDateInput);

        // Get the current date
        LocalDate currentDate = LocalDate.now();

        // Calculate the age
        Period age = Period.between(birthDate, currentDate);

        // Display the age
        System.out.println("You are " + age.getYears() + " years, " + age.getMonths() + " months, and " + age.getDays() + " days old.");
        
        scanner.close();
    }
}
