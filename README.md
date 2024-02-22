# anagrama 



package verificaanagrama;

import java.util.Arrays;
import java.util.Scanner;

public class VerificaAnagrama {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite a primeira palavra:");
        String palavra1 = scanner.nextLine().toLowerCase().replaceAll("\\s", "");

        System.out.println("Digite a segunda palavra:");
        String palavra2 = scanner.nextLine().toLowerCase().replaceAll("\\s", "");

        // Verifica se as palavras têm o mesmo comprimento
        if (palavra1.length() != palavra2.length()) {
            System.out.println("As palavras não são anagramas.");
            return;
        }

        // Converte as palavras para arrays de caracteres
        char[] arrayPalavra1 = palavra1.toCharArray();
        char[] arrayPalavra2 = palavra2.toCharArray();

        // Ordena os arrays de caracteres
        Arrays.sort(arrayPalavra1);
        Arrays.sort(arrayPalavra2);

        // Verifica se os arrays ordenados são iguais
        if (Arrays.equals(arrayPalavra1, arrayPalavra2)) {
            System.out.println("As palavras são anagramas.");
        } else {
            System.out.println("As palavras não são anagramas.");
        }
        
        // Fecha o Scanner
        scanner.close();
    }
}
