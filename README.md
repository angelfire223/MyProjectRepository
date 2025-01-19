import java.util.Scanner;

public class FuelCostCalculator {
    public static void main(String[] args) {
        // Display message stating program purpose to the user. 
        System.out.println("This program calculates the fuel cost per 100 miles and how far your car can go with a full tank of gas.");
        
        // Create a Scanner object for user input.
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter the number of gallons of gas in the tank.
        System.out.print("Please enter the number of gallons of gas needed to fill up your gas tank(floating-point/rational number): ");
        double gallonsInTank = scanner.nextDouble();

        // Prompt the user to enter the vehicle’s fuel efficiency in miles per gallon.
        System.out.print("Enter the fuel efficiency of your vehicle in miles per gallon (floating-point/rational number): ");
        double fuelEfficiency = scanner.nextDouble();

        // Prompt the user to enter the price of gas per gallon.
        System.out.print("Enter the price of gas per gallon (floating-point/rational number): ");
        double pricePerGallon = scanner.nextDouble();

        // Calculate the cost per 100 miles travelled.
        double costPer100Miles = (100 / fuelEfficiency) * pricePerGallon;

        // Calculate how far the car can go with a full tank of gas.
        int milesWithFullTank = (int) (gallonsInTank * fuelEfficiency);

        // Display the results for the user. 
        System.out.printf("The cost per every 100 miles travelled is: $%.2f\n", costPer100Miles);
        System.out.println("The car can go " + milesWithFullTank + " miles with a full tank of gas.");

        // Close the scanner
        scanner.close();
    }
}
