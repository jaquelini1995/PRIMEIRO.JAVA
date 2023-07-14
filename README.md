import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class SortNumbers {
    public static void main(String[] args) {
        // Valores de entrada pré-definidos
        int N = 10;
        int[] input = {4, 32, 34, 543, 3456, 654, 567, 87, 6789, 98};

        List<Integer> pares = new ArrayList<>();
        List<Integer> impares = new ArrayList<>();

        for (int i = 0; i < N; i++) {
            int numero = input[i];
            if (numero % 2 == 0) {
                pares.add(numero);
            } else {
                impares.add(numero);
            }
        }

        Collections.sort(pares);
        Collections.sort(impares, Collections.reverseOrder());

        for (int numero : pares) {
            System.out.println(numero);
        }

        for (int numero : impares) {
            System.out.println(numero);
        }
    }
}
