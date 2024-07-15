import java.util.Scanner;
public class calculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        while (true) {
            System.out.println("Welcome to the Console Calculator!");
            System.out.println("Select an option:");
            System.out.println("1. Basic Arithmetic");
            System.out.println("2. Scientific Calculations");
            System.out.println("3. Unit Conversions");
            System.out.println("4. Exit");
            System.out.print("Enter choice (1/2/3/4): ");

            int choice = scanner.nextInt();
            switch (choice) {
                case 1:
                    basicArithmetic(scanner);
                    break;
                case 2:
                    scientificCalculations(scanner);
                    break;
                case 3:
                    unitConversions(scanner);
                    break;
                case 4:
                    System.out.println("Exiting the calculator. Goodbye!");
                    scanner.close();
                    return;
                default:
                    System.out.println("Invalid choice, please try again.");
            }
        }
    }

    private static void basicArithmetic(Scanner scanner) {
        System.out.println("\nBasic Arithmetic Operations:");
        System.out.println("1. Addition");
        System.out.println("2. Subtraction");
        System.out.println("3. Multiplication");
        System.out.println("4. Division");
        System.out.print("Enter choice (1/2/3/4): ");

        int choice = scanner.nextInt();
        System.out.print("Enter first number: ");
        double num1 = scanner.nextDouble();
        System.out.print("Enter second number: ");
        double num2 = scanner.nextDouble();

        switch (choice) {
            case 1:
                System.out.println("Result: " + num1 + " + " + num2 + " = " + (num1 + num2));
                break;
            case 2:
                System.out.println("Result: " + num1 + " - " + num2 + " = " + (num1 - num2));
                break;
            case 3:
                System.out.println("Result: " + num1 + " * " + num2 + " = " + (num1 * num2));
                break;
            case 4:
                if (num2 != 0) {
                    System.out.println("Result: " + num1 + " / " + num2 + " = " + (num1 / num2));
                } else {
                    System.out.println("Error: Division by zero is not allowed.");
                }
                break;
            default:
                System.out.println("Invalid choice.");
        }
    }

    private static void scientificCalculations(Scanner scanner) {
        System.out.println("\nScientific Calculations:");
        System.out.println("1. Square Root");
        System.out.println("2. Exponentiation");
        System.out.print("Enter choice (1/2): ");

        int choice = scanner.nextInt();
        switch (choice) {
            case 1:
                System.out.print("Enter number: ");
                double num = scanner.nextDouble();
                if (num >= 0) {
                    System.out.println("Result: sqrt(" + num + ") = " + Math.sqrt(num));
                } else {
                    System.out.println("Error: Square root of a negative number is not allowed.");
                }
                break;
            case 2:
                System.out.print("Enter base number: ");
                double base = scanner.nextDouble();
                System.out.print("Enter exponent: ");
                double exp = scanner.nextDouble();
                System.out.println("Result: " + base + " ^ " + exp + " = " + Math.pow(base, exp));
                break;
            default:
                System.out.println("Invalid choice.");
        }
    }

    private static void unitConversions(Scanner scanner) {
        System.out.println("\nUnit Conversions:");
        System.out.println("1. Temperature");
        System.out.println("2. Currency");
        System.out.print("Enter choice (1/2): ");

        int choice = scanner.nextInt();
        switch (choice) {
            case 1:
                temperatureConversion(scanner);
                break;
            case 2:
                currencyConversion(scanner);
                break;
            default:
                System.out.println("Invalid choice.");
        }
    }

    private static void temperatureConversion(Scanner scanner) {
        System.out.println("\nTemperature Conversion:");
        System.out.println("1. Celsius to Fahrenheit");
        System.out.println("2. Fahrenheit to Celsius");
        System.out.print("Enter choice (1/2): ");

        int choice = scanner.nextInt();
        switch (choice) {
            case 1:
                System.out.print("Enter temperature in Celsius: ");
                double celsius = scanner.nextDouble();
                double fahrenheit = (celsius * 9 / 5) + 32;
                System.out.println("Result: " + celsius + " °C = " + fahrenheit + " °F");
                break;
            case 2:
                System.out.print("Enter temperature in Fahrenheit: ");
                fahrenheit = scanner.nextDouble();
                celsius = (fahrenheit - 32) * 5 / 9;
                System.out.println("Result: " + fahrenheit + " °F = " + celsius + " °C");
                break;
            default:
                System.out.println("Invalid choice.");
        }
    }

    private static void currencyConversion(Scanner scanner) {
        // Hardcoded conversion rates for demonstration
        double usdToEurRate = 0.85;
        double eurToUsdRate = 1.18;

        System.out.println("\nCurrency Conversion:");
        System.out.println("1. USD to EUR");
        System.out.println("2. EUR to USD");
        System.out.print("Enter choice (1/2): ");

        int choice = scanner.nextInt();
        switch (choice) {
            case 1:
                System.out.print("Enter amount in USD: ");
                double usd = scanner.nextDouble();
                double eur = usd * usdToEurRate;
                System.out.println("Result: " + usd + " USD = " + eur + " EUR");
                break;
            case 2:
                System.out.print("Enter amount in EUR: ");
                eur = scanner.nextDouble();
                usd = eur * eurToUsdRate;
                System.out.println("Result: " + eur + " EUR = " + usd + " USD");
                break;
            default:
                System.out.println("Invalid choice.");
        }
    }
}
