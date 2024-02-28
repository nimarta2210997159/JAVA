//Write a Java program that prints all the prime numbers between 1 and 100.
//Implement this using both for and while loops.
public class PrimeNumbers {
    public static void main(String[] args) {
        System.out.println("Prime numbers between 1 and 100 using for loop:");
        printPrimesUsingForLoop();
        
        System.out.println("\nPrime numbers between 1 and 100 using while loop:");
        printPrimesUsingWhileLoop();
    }
    
    public static void printPrimesUsingForLoop() {
        for (int i = 2; i <= 100; i++) {
            if (isPrime(i)) {
                System.out.print(i + " ");
            }
        }
    }
    
    public static void printPrimesUsingWhileLoop() {
        int num = 2;
        while (num <= 100) {
            if (isPrime(num)) {
                System.out.print(num + " ");
            }
            num++;
        }
    }
    
    public static boolean isPrime(int number) {
        if (number <= 1) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(number); i++) {
            if (number % i == 0) {
                return false;
            }
        }
        return true;
    }
}
