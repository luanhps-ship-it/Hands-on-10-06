import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int numero;

        int maior = 0;

        int menor = 0;

        boolean primeiro = true;

        while (true) {

            numero = sc.nextInt();

            if (numero == 0) {

                break;

            }

            if (primeiro) {

                maior = numero;

                menor = numero;

                primeiro = false;

            } else {

                if (numero > maior) {

                    maior = numero;

                }

                if (numero < menor) {

                    menor = numero;

                }

            }

        }

        if (!primeiro) {

            System.out.println("Maior = " + maior);

            System.out.println("Menor = " + menor);

        }

  

    }

}

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int positivos = 0;
        int negativos = 0;
        int zeros = 0;

        for (int i = 1; i <= 10; i++) {
            int numero = sc.nextInt();

            if (numero > 0) {
                positivos++;
            } else if (numero < 0) {
                negativos++;
            } else {
                zeros++;
            }
        }

        System.out.println("Positivos = " + positivos);
        System.out.println("Negativos = " + negativos);
        System.out.println("Zeros = " + zeros);

   
    }
}

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int soma = 0;

        for (int i = 1; i <= n; i++) {
            soma += i;
        }

        System.out.println("Soma = " + soma);

   
    }
}

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int soma = 0;

        for (int i = n; i >= 1; i--) {
            System.out.print(i + " ");
            soma += i;
        }

        System.out.println();
        System.out.println("Soma = " + soma);

    }
}

public class Main {
    public static void main(String[] args) {
        long fatorial = 1;

        for (int i = 1; i <= 10; i++) {
            fatorial *= i;
            System.out.println(i + "! = " + fatorial);
        }
    }
}

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        double e = 1;
        double fatorial = 1;

        for (int i = 1; i <= n; i++) {
            fatorial *= i;
            e += 1.0 / fatorial;
        }

        System.out.printf("E = %.6f%n", e);

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double salario, somaSalarios = 0, maiorSalario = 0;
        int filhos, total = 0, ate100 = 0;
        int somaFilhos = 0;

        while (true) {
            salario = sc.nextDouble();

            if (salario < 0) {
                break;
            }

            filhos = sc.nextInt();

            somaSalarios += salario;
            somaFilhos += filhos;
            total++;

            if (total == 1 || salario > maiorSalario) {
                maiorSalario = salario;
            }

            if (salario <= 100) {
                ate100++;
            }
        }

        if (total > 0) {
            System.out.printf("Media salarial = %.2f%n", somaSalarios / total);
            System.out.printf("Media de filhos = %.2f%n", (double) somaFilhos / total);
            System.out.printf("Maior salario = %.2f%n", maiorSalario);
            System.out.printf("Percentual ate R$ 100,00 = %.2f%%%n", ate100 * 100.0 / total);
        }

       
    }
}
public class Main {
    public static void main(String[] args) {
        double chico = 1.50;
        double ze = 1.10;
        int anos = 0;

        while (ze <= chico) {
            chico += 0.02;
            ze += 0.03;
            anos++;
        }

        System.out.println("Anos = " + anos);
        System.out.printf("Altura de Chico = %.2f m%n", chico);
        System.out.printf("Altura de Ze = %.2f m%n", ze);
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int[] votos = new int[7];
        int voto;

        while (true) {
            voto = sc.nextInt();

            if (voto == 0) {
                break;
            }

            if (voto >= 1 && voto <= 6) {
                votos[voto]++;
            }
        }

        System.out.println("Candidato 1: " + votos[1]);
        System.out.println("Candidato 2: " + votos[2]);
        System.out.println("Candidato 3: " + votos[3]);
        System.out.println("Candidato 4: " + votos[4]);
        System.out.println("Votos nulos: " + votos[5]);
        System.out.println("Votos em branco: " + votos[6]);

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int a1 = sc.nextInt();
        int r = sc.nextInt();
        int soma = 0;

        for (int i = 0; i < n; i++) {
            int termo = a1 + i * r;

            System.out.print(termo + " ");
            soma += termo;
        }

        System.out.println();
        System.out.println("Soma = " + soma);

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        for (int i = 1; i <= 20; i++) {
            int n = sc.nextInt();

            for (int j = 1; j <= n; j++) {
                System.out.println(j + " x " + n + " = " + (j * n));
            }
        }

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int idade;
        int maiorIdade = 0;
        int mulheres = 0;

        while (true) {
            idade = sc.nextInt();

            if (idade == -1) {
                break;
            }

            char sexo = sc.next().toUpperCase().charAt(0);
            String olhos = sc.next().toLowerCase();
            String cabelos = sc.next().toLowerCase();

            if (idade > maiorIdade) {
                maiorIdade = idade;
            }

            if (sexo == 'F' && idade >= 18 && idade <= 35
                    && olhos.equals("verdes") && cabelos.equals("louros")) {
                mulheres++;
            }
        }

        System.out.println("Maior idade = " + maiorIdade);
        System.out.println("Mulheres com as caracteristicas = " + mulheres);

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int codigo, quantidade = 0;
        double preco, somaAntes = 0, somaDepois = 0;

        while (true) {
            codigo = sc.nextInt();

            if (codigo < 0) {
                break;
            }

            preco = sc.nextDouble();
            double novoPreco = preco * 1.20;

            System.out.printf("Codigo: %d%n", codigo);
            System.out.printf("Novo preco: R$ %.2f%n", novoPreco);

            somaAntes += preco;
            somaDepois += novoPreco;
            quantidade++;
        }

        if (quantidade > 0) {
            System.out.printf("Media antes = R$ %.2f%n", somaAntes / quantidade);
            System.out.printf("Media depois = R$ %.2f%n", somaDepois / quantidade);
        }

      
    }
}
public class Main {
    public static void main(String[] args) {
        for (int i = 1000; i <= 1999; i++) {
            if (i % 11 == 5) {
                System.out.println(i);
            }
        }
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        double soma = 0;

        for (int i = 1; i <= n; i++) {
            soma += 1.0 / i;

            if (i > 1) {
                System.out.print(" + ");
            }

            System.out.print("1/" + i);
        }

        System.out.println();
        System.out.printf("S = %.2f%n", soma);

       
    }
}
public class Main {
    public static void main(String[] args) {
        int encontrados = 0;
        int numero = 2;

        while (encontrados < 5) {
            int soma = 0;

            for (int i = 1; i <= numero / 2; i++) {
                if (numero % i == 0) {
                    soma += i;
                }
            }

            if (soma == numero) {
                System.out.println(numero);
                encontrados++;
            }

            numero++;
        }
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int codigo, acidentes;
        int codigoMaior = 0, codigoMenor = 0;
        int maior = 0, menor = 0;
        double somaVeiculos = 0;

        for (int i = 1; i <= 200; i++) {
            codigo = sc.nextInt();
            String estado = sc.next();
            int veiculos = sc.nextInt();
            acidentes = sc.nextInt();

            somaVeiculos += veiculos;

            if (i == 1 || acidentes > maior) {
                maior = acidentes;
                codigoMaior = codigo;
            }

            if (i == 1 || acidentes < menor) {
                menor = acidentes;
                codigoMenor = codigo;
            }
        }

        System.out.println("Maior numero de acidentes = " + maior);
        System.out.println("Codigo da cidade = " + codigoMaior);
        System.out.println("Menor numero de acidentes = " + menor);
        System.out.println("Codigo da cidade = " + codigoMenor);
        System.out.printf("Media de veiculos = %.2f%n", somaVeiculos / 200);

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        for (int i = 1; i <= 75; i++) {
            int matricula = sc.nextInt();
            double nota = sc.nextDouble();
            char conceito;

            if (nota > 9) {
                conceito = 'A';
            } else if (nota >= 7) {
                conceito = 'B';
            } else if (nota >= 5) {
                conceito = 'C';
            } else {
                conceito = 'D';
            }

            System.out.println("Matricula: " + matricula);
            System.out.printf("Nota final: %.2f%n", nota);
            System.out.println("Conceito: " + conceito);
        }

        
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int[] faixas = new int[6];

        for (int i = 1; i <= 15; i++) {
            int idade = sc.nextInt();

            if (idade <= 15) {
                faixas[1]++;
            } else if (idade <= 30) {
                faixas[2]++;
            } else if (idade <= 45) {
                faixas[3]++;
            } else if (idade <= 60) {
                faixas[4]++;
            } else {
                faixas[5]++;
            }
        }

        for (int i = 1; i <= 5; i++) {
            System.out.println("Faixa " + i + " = " + faixas[i]);
        }

        System.out.printf("Percentual da primeira faixa = %.2f%%%n", faixas[1] * 100.0 / 15);
        System.out.printf("Percentual da ultima faixa = %.2f%%%n", faixas[5] * 100.0 / 15);

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        double x = sc.nextDouble();
        double soma = 0;
        double potencia = 1;
        double fatorial = 1;

        for (int i = 1; i <= n; i++) {
            int expoente = i + 1;

            potencia *= x;

            if (i == 1) {
                fatorial = 1;
            } else {
                fatorial *= i;
            }

            double termo = potencia / fatorial;

            if (i % 2 == 1) {
                soma -= termo;
            } else {
                soma += termo;
            }
        }

        System.out.printf("S = %.6f%n", soma);

 
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double salarioMinimo = 1621.00;

        for (int i = 1; i <= 10; i++) {
            int codigo = sc.nextInt();
            double horas = sc.nextDouble();
            char turno;
            char categoria;

            do {
                turno = sc.next().toUpperCase().charAt(0);
            } while (turno != 'M' && turno != 'V' && turno != 'N');

            do {
                categoria = sc.next().toUpperCase().charAt(0);
            } while (categoria != 'O' && categoria != 'G');

            double percentualHora;

            if (categoria == 'G') {
                percentualHora = turno == 'N' ? 0.18 : 0.15;
            } else {
                percentualHora = turno == 'N' ? 0.13 : 0.10;
            }

            double valorHora = salarioMinimo * percentualHora;
            double salarioInicial = horas * valorHora;
            double percentualAuxilio;

            if (salarioInicial <= 1080) {
                percentualAuxilio = 0.20;
            } else if (salarioInicial <= 2160) {
                percentualAuxilio = 0.15;
            } else {
                percentualAuxilio = 0.05;
            }

            double auxilio = salarioInicial * percentualAuxilio;
            double salarioFinal = salarioInicial + auxilio;

            System.out.println("Codigo: " + codigo);
            System.out.printf("Horas trabalhadas: %.2f%n", horas);
            System.out.printf("Valor da hora: R$ %.2f%n", valorHora);
            System.out.printf("Salario inicial: R$ %.2f%n", salarioInicial);
            System.out.printf("Auxilio alimentacao: R$ %.2f%n", auxilio);
            System.out.printf("Salario final: R$ %.2f%n", salarioFinal);
        }

        
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        long a = 0;
        long b = 1;

        for (int i = 1; i <= n; i++) {
            System.out.print(a + " ");

            long proximo = a + b;
            a = b;
            b = proximo;
        }

      
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double salarioMinimo = 1621.00;
        double folha = 0;
        int totalPecas = 0;
        int pecasHomens = 0;
        int quantidadeHomens = 0;
        int pecasMulheres = 0;
        int quantidadeMulheres = 0;
        double maiorSalario = -1;
        int maiorOperario = 0;

        for (int i = 1; i <= 15; i++) {
            int numero = sc.nextInt();
            int pecas = sc.nextInt();
            char sexo = sc.next().toUpperCase().charAt(0);

            double salario;

            if (pecas <= 30) {
                salario = salarioMinimo;
            } else if (pecas <= 50) {
                salario = salarioMinimo + (pecas - 30) * salarioMinimo * 0.03;
            } else {
                salario = salarioMinimo + (pecas - 30) * salarioMinimo * 0.05;
            }

            folha += salario;
            totalPecas += pecas;

            if (sexo == 'M') {
                pecasHomens += pecas;
                quantidadeHomens++;
            } else if (sexo == 'F') {
                pecasMulheres += pecas;
                quantidadeMulheres++;
            }

            if (salario > maiorSalario) {
                maiorSalario = salario;
                maiorOperario = numero;
            }

            System.out.println("Operario: " + numero);
            System.out.printf("Salario: R$ %.2f%n", salario);
        }

        System.out.printf("Total da folha: R$ %.2f%n", folha);
        System.out.println("Total de pecas: " + totalPecas);

        if (quantidadeHomens > 0) {
            System.out.printf("Media de pecas dos homens: %.2f%n", (double) pecasHomens / quantidadeHomens);
        }

        if (quantidadeMulheres > 0) {
            System.out.printf("Media de pecas das mulheres: %.2f%n", (double) pecasMulheres / quantidadeMulheres);
        }

        System.out.println("Operario com maior salario: " + maiorOperario);

        sc.close();
    }
}

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int nascimentos = sc.nextInt();
        int femininasMortas = 0;
        int masculinasMortas = 0;
        int ate24Meses = 0;

        for (int i = 1; i <= nascimentos; i++) {
            char sexo = sc.next().toUpperCase().charAt(0);
            int meses = sc.nextInt();

            if (meses <= 24) {
                ate24Meses++;
            }

            if (meses == 0) {
                if (sexo == 'F') {
                    femininasMortas++;
                } else if (sexo == 'M') {
                    masculinasMortas++;
                }
            }
        }

        if (nascimentos > 0) {
            System.out.printf("Percentual feminino morto: %.2f%%%n", femininasMortas * 100.0 / nascimentos);
            System.out.printf("Percentual masculino morto: %.2f%%%n", masculinasMortas * 100.0 / nascimentos);
            System.out.printf("Percentual com ate 24 meses: %.2f%%%n", ate24Meses * 100.0 / nascimentos);
        }

       
    }
}
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double somaAdicionais = 0;
        double totalImpostos = 0;
        double maiorPreco = Double.NEGATIVE_INFINITY;
        double menorPreco = Double.POSITIVE_INFINITY;
        int barato = 0;
        int normal = 0;
        int caro = 0;

        for (int i = 1; i <= 12; i++) {
            double preco = sc.nextDouble();
            char refrigeracao = sc.next().toUpperCase().charAt(0);
            char categoria = sc.next().toUpperCase().charAt(0);

            double custo;

            if (preco <= 20) {
                if (categoria == 'A') {
                    custo = 2;
                } else if (categoria == 'L') {
                    custo = 3;
                } else {
                    custo = 4;
                }
            } else if (preco <= 50) {
                custo = refrigeracao == 'S' ? 6 : 0;
            } else {
                if (refrigeracao == 'S') {
                    if (categoria == 'A') {
                        custo = 5;
                    } else if (categoria == 'L') {
                        custo = 2;
                    } else {
                        custo = 4;
                    }
                } else {
                    custo = categoria == 'L' ? 1 : 0;
                }
            }

            double imposto = preco * ((categoria == 'A' && refrigeracao == 'S') ? 0.04 : 0.02);
            double precoFinal = preco + custo + imposto;
            double adicionais = custo + imposto;

            somaAdicionais += adicionais;
            totalImpostos += imposto;

            if (precoFinal > maiorPreco) {
                maiorPreco = precoFinal;
            }

            if (precoFinal < menorPreco) {
                menorPreco = precoFinal;
            }

            String classificacao;

            if (precoFinal <= 20) {
                classificacao = "Barato";
                barato++;
            } else if (precoFinal <= 100) {
                classificacao = "Normal";
                normal++;
            } else {
                classificacao = "Caro";
                caro++;
            }

            System.out.println("Produto " + i);
            System.out.printf("Preco unitario: R$ %.2f%n", preco);
            System.out.printf("Custo de estocagem: R$ %.2f%n", custo);
            System.out.printf("Imposto: R$ %.2f%n", imposto);
            System.out.printf("Preco final: R$ %.2f%n", precoFinal);
            System.out.println("Classificacao: " + classificacao);
        }

        System.out.printf("Media dos valores adicionais: R$ %.2f%n", somaAdicionais / 12);
        System.out.printf("Maior preco final: R$ %.2f%n", maiorPreco);
        System.out.printf("Menor preco final: R$ %.2f%n", menorPreco);
        System.out.printf("Total de impostos: R$ %.2f%n", totalImpostos);
        System.out.println("Baratos: " + barato);
        System.out.println("Normais: " + normal);
        System.out.println("Caros: " + caro);

   
    }
}
