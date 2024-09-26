# kalkulator-sederhana menggunakan java
import java.util.Scanner;

public class Kalkulator {

    public static int tambah(int a, int b) {
        int hasil = a + b;
        return hasil;
    }

    public static int kurang(int a, int b) {
        int hasil = a - b;
        return hasil;
    }

    public static int kali(int a, int b) {
        int hasil = a * b;
        return hasil;
    }

    public static float bagi(float a, float b) {
        float hasil = a / b;
        return hasil;
    }

    public static int modulo(int a, int b) {
        int hasil = a % b;
        return hasil;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int a, b;
        char operasi;
        
        a = scanner.nextInt();
        operasi = scanner.next().charAt(0);
        b = scanner.nextInt();
        
        switch(operasi) {
            case '+':
                System.out.println(tambah(a, b));
                break;
                
            case '-':
                System.out.println(kurang(a, b));
                break;
                
            case '*':
                System.out.println(kali(a, b));
                break;
                
            case '/':
                System.out.printf("%.2f\n", bagi(a, b));
                break;
                
            case '%':
                System.out.println(modulo(a, b));
                break;
                
            default:
                System.out.println("Operasi tidak valid");
                break;
        }
        
        scanner.close();
    }
}
