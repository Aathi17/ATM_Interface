package details;
class BankAccount {
    private double balance;

    public BankAccount(double initialBalance) {
        this.balance = initialBalance;
    }

    public double getBalance() {
        return balance;
    }

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposit successful. New balance: $" + balance);
        } else {
            System.out.println("Invalid deposit amount.");
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawal successful. New balance: $" + balance);
        } else {
            System.out.println("Invalid withdrawal amount or insufficient balance.");
        }
    }
}

package details;
import java.util.Scanner;
public class ATM {
    private static BankAccount userAccount = new BankAccount(1000.0);
    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
    	System.out.println("Welcome to the ATM !");
        while (true) {
            displayOptions();
            int option = getUserChoice();
            switch (option) {
                case 1: withdraw(); break;
                case 2: deposit(); break;
                case 3: checkBalance(); break;
                case 4: System.out.println("Thank you for using the ATM. Goodbye!"); System.exit(0);
                default: System.out.println("Invalid option. Please try again.");
            }
        }
    }

    private static void displayOptions() {
        System.out.println("\nOptions:");
        System.out.println("1. Withdraw");
        System.out.println("2. Deposit");
        System.out.println("3. Check Balance");
        System.out.println("4. Exit");
    }

    private static int getUserChoice() {
        System.out.print("Enter your choice (1-4): ");
        while (!scanner.hasNextInt()) {
            System.out.print("Invalid input. Enter a number (1-4): ");
            scanner.next(); // Consume invalid input
        }
        return scanner.nextInt();
    }

    private static void withdraw() {
        System.out.print("Enter the withdrawal amount: $");
        double amount = scanner.nextDouble();
        userAccount.withdraw(amount);
    }

    private static void deposit() {
        System.out.print("Enter the deposit amount: $");
        double amount = scanner.nextDouble();
        userAccount.deposit(amount);
    }

    private static void checkBalance() {
        System.out.println("Current balance: $" + userAccount.getBalance());
    }
}

