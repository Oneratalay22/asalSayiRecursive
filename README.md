import java.util.Scanner;

public class Main {

    static boolean isPrime(int numberBir, int numberİki) {
        // Base cases
        if (numberBir <= 2)
            return (numberBir == 2);
        if (numberBir % numberİki == 0)
            return false;
        if (numberİki * numberİki > numberBir)
            return true;

        // Recursive case
        return isPrime(numberBir, numberİki + 1);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Bir sayı giriniz: ");
        int number = scanner.nextInt();

        if (isPrime(number, 2))
            System.out.println(number + " bir asal sayıdır.");
        else
            System.out.println(number + " bir asal sayı değildir.");
    }
}
