# java.util.Scanner
java.util.Scanner
import java.util.Scanner;

public class RecursiveGCD {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Введите первое число: ");
        int number1 = scanner.nextInt();

        System.out.print("Введите второе число: ");
        int number2 = scanner.nextInt();

        int gcd = calculateGCD(number1, number2);
        System.out.println("Наибольший общий делитель: " + gcd);
    }

    public static int calculateGCD(int number1, int number2) {
        if (number2 == 0) {
            return number1;
        }
        return calculateGCD(number2, number1 % number2);
    }
}
