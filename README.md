# Tailor

import java.util.Scanner;

public class Tailor {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int count = Integer.parseInt(scanner.nextLine());
        double lenght = Double.parseDouble(scanner.nextLine());
        double width = Double.parseDouble(scanner.nextLine());

        double facetcover = (lenght + 2 * 0.30) * (width + 2 * 0.30);
        double facecaret = (lenght / 2) * (lenght / 2);
        double coverprice = facetcover * 7;
        double caretprice = facecaret * 9;
        double sumdollarcover = count * coverprice;
        double sumdollarcaret = count * caretprice;
        double alldollarprice = sumdollarcaret + sumdollarcover;
        double sumlevacover = sumdollarcover * 1.85;
        double sumlevacaret = sumdollarcaret * 1.85;

        double alllevaprice = sumlevacaret + sumlevacover;

        System.out.printf("%.2f USD %n", alldollarprice);
        System.out.printf("%.2f BGN %n" , alllevaprice);

    }
}
