# Calculate-Simple-Interest
import java.util.Scanner;

class SimpleInterestCalculator {
    private double principal;
    private double rate;
    private double time;

    public SimpleInterestCalculator(double principal, double rate, double time) {
        this.principal = principal;
        this.rate = rate;
        this.time = time;
    }

    public double calculateSimpleInterest() {
        double simpleInterest = (principal * rate * time) / 100;
        return simpleInterest;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the principal amount: ");
        double principal = scanner.nextDouble();

        System.out.print("Enter the annual interest rate (%): ");
        double rate = scanner.nextDouble();

        System.out.print("Enter the time period in years: ");
        double time = scanner.nextDouble();

        SimpleInterestCalculator calculator = new SimpleInterestCalculator(principal, rate, time);

        double simpleInterest = calculator.calculateSimpleInterest();

        System.out.println("Simple Interest = " + simpleInterest);

        scanner.close();
    }
}
