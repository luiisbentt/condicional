# condicional
codigo da atividade 
public class SalarioReajuste.java{

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("coloque o seu salario atual: ");
        double salarioAtual = scanner.nextDouble();
        scanner.close();

        double aumento = 0;
        double novoSalario = 0;

        if (salarioAtual <= 280) {
            aumento = salarioAtual * 0.20;
        } else if (salarioAtual <= 700) {
            aumento = salarioAtual * 0.15;
        } else if (salarioAtual <= 1500) {
            aumento = salarioAtual * 0.10;
        } else {
            aumento = salarioAtual * 0.05;
        }

        novoSalario = salarioAtual + aumento;
        double aumentoReal = aumento - (aumento * 0.038); // descontando a inflação de 3.8%

        System.out.println("1. salario antes de fazer o reajuste: R$" + String.format("%.2f", salarioAtual));
        System.out.println("2. o aumento em porcentagem que foi aplicado: " + String.format("%.1f", aumento * 100 / salarioAtual) + "%");
        System.out.println("3. aumento: R$" + String.format("%.2f", aumento));
        System.out.println("4. salario apos o aumento: R$" + String.format("%.2f", novoSalario));
        System.out.println("5. valor do auemnto descontando a inflacao: R$" + String.format("%.2f", aumentoReal));
    }
}
