# dk
import java.util.Scanner;

public class DecimalToBinaryConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Welcome to the Decimal to Binary Converter!");
        System.out.println("Enter a decimal number to convert it to binary.");
        System.out.println("Type 'STOP' to end the program.");

        while (true) {
            System.out.print("Enter a decimal number: ");
            String userInput = scanner.nextLine();

            if (userInput.equalsIgnoreCase("STOP")) {
                System.out.println("Terminating the program. Goodbye!");
                break;
            }

            try {
                int decimalNumber = Integer.parseInt(userInput);
                String binaryNumber = Integer.toBinaryString(decimalNumber);
                System.out.println(decimalNumber + " in binary is: " + binaryNumber);
            } catch (NumberFormatException e) {
                System.out.println("Invalid input. Please enter a valid decimal number.");
            }
        }

        scanner.close();
    }
}
