# Est-gio---TargetSystem
Questões de 1  a 5 (README file).
package estagioTargetResposta1;

import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Fibonacci {
	
	public static void main(String[] args) {
		
        @SuppressWarnings("resource")
        
		Scanner scanner = new Scanner(System.in);
        System.out.print("Informe um número: ");
        //Usuario entra com numero
        int n = scanner.nextInt();

        List<Integer> sequence = fibonacci(n);
        //Sequencia guardada no List
        if (sequence.contains(n)) {
            System.out.println("O número " + n + " pertence à sequência de Fibonacci.");
        } else {
            System.out.println("O número " + n + " não pertence à sequência de Fibonacci.");
        }
    }//Se o numero esta na sequencia a mensagem surge,indicando que não é um numero na tabela fibonnaci
             
    public static List<Integer> fibonacci(int n) {
        List<Integer> sequence = new ArrayList <>();
        sequence.add(0);
        sequence.add(1);
        while (sequence.get(sequence.size() - 1) < n) {
            sequence.add(sequence.get(sequence.size() - 1) + sequence.get(sequence.size() - 2));
        }
        return sequence;
    }

}
Questão 02
package resposta2;

import java.util.Scanner;

public class ContadorLetras {
	
	public static void main(String[] args) {
		
        @SuppressWarnings("resource")
        
		Scanner scanner = new Scanner(System.in);
        System.out.print("Informe uma string: ");
        String input = scanner.nextLine();

        int count = countLetter(input, 'a');
        //Metodo para contar a letra 'a'
        if (count > 0) {
            System.out.println("A letra 'a' ocorre " + count + " vezes na string.");
        } else {
            System.out.println("A letra 'a' não ocorre na string.");
        }
    }

    public static int countLetter(String str, char letter) {
        int count = 0;
        for (char c : str.toLowerCase().toCharArray())
        //metodo para deixar letra minuscula
        	{
            if (c == letter || c == Character.toUpperCase(letter)) {
                count++;
                //metodo para deixar letra maiuscula
            }
        }
        return count;
    }
}

Questão 03
package resposta3;

public class TrechoCodigo {

	//Observe o trecho de código abaixo: int INDICE = 12, SOMA = 0, K = 1; enquanto K < INDICE faça { K = K + 1; SOMA = SOMA + K; } imprimir(SOMA);

	//Ao final do processamento, qual será o valor da variável SOMA?
	
	//A estrutura "enquanto" (ou "while", em uma tradução para Java) faz o seguinte enquanto K < INDICE (ou seja, enquanto K < 12):

//Vamos analisar o código passo a passo:

//INDICE é definido como 12.
//SOMA é definido como 0.
//K é definido como 1.
//A condição do loop é K < INDICE, que é verdadeira desde que K é 1 e INDICE é 12.
//Dentro do loop, K é incrementado em 1, então K se torna 2.
//SOMA é atualizado adicionando K a ele, então SOMA se torna 2.
//A condição do loop ainda é verdadeira, então o loop continua.
//K é incrementado novamente, tornando-se 3.
//SOMA é atualizado novamente, tornando-se 2 + 3 = 5.
//Este processo continua até K alcançar 12.
//Quando K é 12, a condição do loop não é mais verdadeira, e o loop sai.
//Vamos calcular o valor final de SOMA:

//SOMA = 1 + 2 + 3 + ... + 12

//Isso é uma série aritmética com 12 termos, onde o primeiro termo é 1 e o último termo é 12. A fórmula para a soma de uma série aritmética é:

//SOMA = (n * (a1 + an)) / 2

//onde n é o número de termos, a1 é o primeiro termo e an é o último termo.

//Substituindo os valores, obtemos:

//SOMA = (12 * (1 + 12)) / 2 SOMA = (12 * 13) / 2 SOMA = 78

//Portanto, o valor final de SOMA é 78.
}
Questão 04
package resposta4;

public class Logica {
	 //Descubra a lógica e complete o próximo elemento:
		 //a) 1, 3, 5, 7, ___
		 //b) 2, 4, 8, 16, 32, 64, ____
		 //c) 0, 1, 4, 9, 16, 25, 36, ____
		 //d) 4, 16, 36, 64, ____
		 //e) 1, 1, 2, 3, 5, 8, ____
		 //f) 2,10, 12, 16, 17, 18, 19, ____

//Vamos analisar cada sequência e descobrir a lógica para completar o próximo elemento:

//a) 1, 3, 5, 7, ___ A sequência é formada por números ímpares consecutivos. O próximo elemento seria o próximo número ímpar, que é 9.

//b) 2, 4, 8, 16, 32, 64, ____ A sequência é formada por potências de 2. O próximo elemento seria a próxima potência de 2, que é 128.

//c) 0, 1, 4, 9, 16, 25, 36, ____ A sequência é formada por quadrados perfeitos. O próximo elemento seria o próximo quadrado perfeito, que é 49.

//d) 4, 16, 36, 64, ____ A sequência é formada por quadrados perfeitos de números pares. O próximo elemento seria o próximo quadrado perfeito de um número par, que é 100.

//e) 1, 1, 2, 3, 5, 8, ____ A sequência é a famosa sequência de Fibonacci, onde cada elemento é a soma dos dois elementos anteriores. O próximo elemento seria a soma dos dois elementos anteriores, que é 13.

//f) 2, 10, 12, 16, 17, 18, 19, ____ A sequência não parece ter uma lógica clara, mas se analisarmos os elementos, podemos notar que a sequência está aumentando em 1 ou 2 unidades a cada vez. Se continuarmos essa tendência, o próximo elemento seria 20.

//Portanto, as respostas são:

//a) 9 b) 128 c) 49 d) 100 e) 13 f) 20
}
Questão 05
package resposta5;

public class SalaLampada {
 //Fiz um algoritimo de como resolver etapa a etapa
//	Passo 1:

	//	Ligue o interruptor 1 por 5 minutos. Desligue o interruptor 1. Ligue o interruptor 2. Vá até a sala das lâmpadas e observe as lâmpadas.

	//	Passo 2:

	//	Volte para a sala dos interruptores e desligue o interruptor 2. Ligue o interruptor 3. Vá até a sala das lâmpadas novamente e observe as lâmpadas.

	//	Análise:

	//	No Passo 1, você ligou o interruptor 1 por 5 minutos, o que significa que a lâmpada correspondente estará quente (ou ao menos mais quente que as outras). Em seguida, você desligou o interruptor 1 e ligou o interruptor 2. Isso significa que a lâmpada correspondente ao interruptor 2 estará acesa.

	//	Ao ir até a sala das lâmpadas, você verá três situações possíveis:

	//	Uma lâmpada está acesa e quente (interruptor 1).
	//	Uma lâmpada está acesa e fria (interruptor 2).
	//	Uma lâmpada está apagada e quente (interruptor 3).
	//	No Passo 2, você desligou o interruptor 2 e ligou o interruptor 3. Isso significa que a lâmpada correspondente ao interruptor 3 estará acesa.

	//	Ao ir até a sala das lâmpadas novamente, você verá que:

	//	A lâmpada que estava acesa e quente agora está apagada (interruptor 1).
	//	A lâmpada que estava acesa e fria agora está apagada (interruptor 2).
	//	A lâmpada que estava apagada e quente agora está acesa (interruptor 3).
	//	Com essas informações, você pode determinar qual interruptor controla qual lâmpada.

	//	Resposta:

	//	Interruptor 1: lâmpada quente no Passo 1.
	//	Interruptor 2: lâmpada acesa e fria no Passo 1.
		//Interruptor 3: lâmpada apagada e quente no Passo 1, e acesa no Passo 2.
}
