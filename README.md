# Segue uma solução simples em Java para cada questão:

1. Filtro de Palavras Reservadas

import java.util.*;
public class Questao1 {
    public static void main(String[] args) {
        Set<String> reservadas = new HashSet<>(Arrays.asList(
                "if", "else", "while", "for", "return",
                "int", "System", "out", "print",
                "public", "class"
        ));
        Set<String> palavrasCodigo = new HashSet<>(Arrays.asList(
                "public", "class", "StarRectangle", "void",
                "printRectangle", "int", "n", "for",
                "i", "System", "out", "print"
        ));
        Set<String> presentes = new HashSet<>(palavrasCodigo);
        presentes.retainAll(reservadas);
        Set<String> identificadores = new HashSet<>(palavrasCodigo);
        identificadores.removeAll(reservadas);
        System.out.println("Reservadas: " + presentes);
        System.out.println("Identificadores: " + identificadores);
    }
}
