import java.util.Scanner;

public class MiniProjeto2 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bem-vindo ao Jogo de Corrida de Carros!");
        System.out.print("Digite o nome do seu personagem: ");
        String nomePersonagem = scanner.nextLine();

        System.out.println("Escolha sua equipe de corrida:");
        System.out.println("1. Mercedes");
        System.out.println("2. Ferrari");
        System.out.println("3. McLaren");

        // Obtém a escolha da equipe do jogador
        int escolhaEquipe = scanner.nextInt();

        // Nome da equipe escolhida
        String equipeEscolhida = "";

        // Define a equipe com base na escolha do jogador
        switch (escolhaEquipe) {
            case 1:
                equipeEscolhida = "Mercedes";
                break;
            case 2:
                equipeEscolhida = "Ferrari";
                break;
            case 3:
                equipeEscolhida = "McLaren";
                break;
            default:
                System.out.println("Escolha inválida. Você não selecionou uma equipe.");
                return;
        }

        System.out.println(nomePersonagem + ", você está na equipe " + equipeEscolhida + " e está participando de uma corrida de carros.");
        System.out.println("Você está na reta final e tem três opções para vencer a corrida.");

        // Mostra as opções de escolha
        System.out.println("Escolha o que fazer:");
        System.out.println("1. Acelerar para ultrapassar o carro à frente.");
        System.out.println("2. Manter a velocidade atual e aguardar por uma oportunidade.");
        System.out.println("3. Frear para evitar um possível acidente.");

        // Obtém a escolha do jogador
        int escolha = scanner.nextInt();

        // Realiza ações com base na escolha do jogador
        switch (escolha) {
            case 1:
                System.out.println("Você acelera para ultrapassar o carro à frente. Agora, você tem duas escolhas:");
                System.out.println("1. Continuar acelerando para a vitória.");
                System.out.println("2. Reduzir a velocidade para evitar riscos.");
                int escolhaAcelerar = scanner.nextInt();
                if (escolhaAcelerar == 1) {
                    System.out.println("Você acelera com coragem e cruza a linha de chegada em primeiro lugar para a equipe " + equipeEscolhida + "!");
                } else {
                    System.out.println("Você decide reduzir a velocidade para evitar riscos, mas outro carro o ultrapassa e vence a corrida.");
                }
                break;
            case 2:
                System.out.println("Você mantém a velocidade atual, esperando por uma oportunidade. Outro carro tenta ultrapassá-lo. Agora, você tem duas escolhas:");
                System.out.println("1. Acelerar para impedir que o carro o ultrapasse.");
                System.out.println("2. Permitir que o carro o ultrapasse e continuar na mesma velocidade.");
                int escolhaManterVelocidade = scanner.nextInt();
                if (escolhaManterVelocidade == 1) {
                    System.out.println("Você acelera para manter sua posição e consegue a vitória para a equipe " + equipeEscolhida + "!");
                } else {
                    System.out.println("Você permite que o carro o ultrapasse e fica em segundo lugar.");
                }
                break;
            case 3:
                System.out.println("Você freia para evitar um possível acidente. Agora, você tem duas escolhas:");
                System.out.println("1. Recomeçar a corrida com cautela.");
                System.out.println("2. Continuar na mesma velocidade após a situação segura.");
                int escolhaFrear = scanner.nextInt();
                if (escolhaFrear == 1) {
                    System.out.println("Você recomeça a corrida com cautela e termina em terceiro lugar.");
                } else {
                    System.out.println("Você continua na mesma velocidade e termina a corrida em segundo lugar.");
                }
                break;
            default:
                System.out.println("Escolha inválida. Você não toma nenhuma ação na corrida.");
                break;
        }

        // Encerra o scanner
        scanner.close();
    }
}
