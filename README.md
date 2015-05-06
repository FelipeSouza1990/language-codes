# language-codes
# Linguagem C

#include <stdio.h>
#include <stdlib.h>
#include <conio.h>

	int main(int argc, char *argv[]){

	float a=0, b=0, resultado=0, totPessoasCont=0;
	int op=0;
	
	do{
	printf ("\tSeja bem vindo!\n");
	printf ("Qual o setor da empresa que deseja?\n");
	printf ("\n\t1 - FINANCEIRO\n\t2 - CONTAS A PAGAR\n\t3 - RECURSOS HUMANOS\n\t4 - DESENVOLVIMENTO ORGANIZACIONAL\n\t5 - TECNOLOGIA DA INFORMACAO\n\t6 - ADMINISTRATIVO\n\n\t");
	scanf ("%i", &op);
	if (op == 1){
		
		printf ("\n\t DEPARTAMENTO - FINANCEIRO \n");
		printf ("Escolha a operacao que deseja fazer no setor financeiro\n\t");		
		
		printf ("\n\t1 - SOMA\n\t2 - SUBTRACAO\n\t3 - MULTIPLICACAO\n\t4 - DIVISAO\n\t");
		scanf ("%i", &op);
	
		printf ("Entre com o primeiro valor: \t");
		scanf ("%f", &a);
	
		printf ("Entre com o segundo valor: \t");
		scanf ("%f", &b);
		
		switch (op){
			case 1:
				resultado = a + b;
				break;
			case 2:
				resultado = a - b;
				break;
			case 3:
				resultado = a * b;
				break;
			case 4:
				resultado = a / b;
				break;
			default:
		printf ("\n Digite uma operacao valida \n");
				break;
		}
		printf ("\n\t O resultado e: %0.2f", resultado);
		printf ("\n Digite 1 para continuar: ");
		scanf ("%i", &op);

        }else if (op == 2){
		
		printf ("\n\t DEPARTAMENTO - CONTAS A PAGAR \n");
		printf ("Escolha a operacao que deseja fazer no setor de contas a pagar\n\t");	
		printf ("\n\t1 - NOTAS FISCAIS RECEBIDAS\n\t2 - NOTAS FISCAIS EMITIDAS\n\n\t");
	scanf ("%i", &op);
			printf ("Entre com o primeiro valor: \t");
		scanf ("%f", &a);
	
		printf ("Entre com o segundo valor: \t");
		scanf ("%f", &b);
		
		switch (op){
			case 1:
				resultado = (a * b)/100;
				break;
			case 2:
				resultado = (a * b)/100;
				break;
			default:
				printf ("\n\tDigite uma opcao valida\n");
				break;
		}
		printf ("\n\t O resultado e: %0.2f", resultado);
		printf ("\n Digite 1 para continuar: ");
		scanf ("%i", &op);
	}else if (op == 3){
		printf ("\n\t DEPARTAMENTO - RECURSOS HUMANOS \n");
		printf ("Escolha a operacao que deseja fazer no setor de recursos humanos\n\t");	
		printf ("\n\t1 - CALCULAR INSALUBRIDADE\n\t2 - CALCULAR DESCONTOS EM FOLHA DE PAGAMENTO\n\n\t");
		scanf ("%i", &op);
		printf ("Entre com o seu salario: \t");
		scanf ("%f", &a);
			switch (op){
			case 1:
				a = (a * 0.2) + a;
				printf ("\n\t O salario liquido e: R$%0.2f", a);
				break;
			case 2:
				if (a <= 1247.70){
					a = a - (a * 0.08); 
				printf ("\n\t O salario liquido e: R$%0.2f", a);
				break;
				}else if (a <= 2079.50){
					a = a - (a * 0.09);
				printf ("\n\t O salario liquido e: R$%0.2f", a);
				break;
				}else if (a <= 4159.00){
					a = a - ((a * 11)/100);
				printf ("\n\t O salario liquido e: R$%0.2f", a);
				break;
				}else if (a >= 4159.00){
					a = a - 457.49;
				printf ("\n\t O salario liquido e: R$%0.2f", a);
				}
			default:
				printf ("\n\tDigite uma opcao valida\n");
				break;
		}
		printf ("\n Digite 1 para continuar: ");
		scanf ("%i", &op);
		
	}else if (op == 4){
		printf ("\n\t DEPARTAMENTO - DESENVOLVIMENTO ORGANIZACIONAL \n");
		printf ("Escolha a operacao que deseja fazer no setor de desenvolvimento organizacional\n\t");	
		printf ("\n\t1 - CALCULAR TURNOVER (ADMISSOES E DESLIGAMENTOS)\n\t2 - CALCULAR TURNOVER (DESLIGAMENTOS)\n\n\t");
		scanf ("%i", &op);
	
		switch (op){
			case 1:
				printf ("Entre com o numero de pessoas contratadas: \t");
				scanf ("%f", &totPessoasCont);
	
				printf ("Entre com o numero de pessoas demitidas: \t");
				scanf ("%f", &a);
				
				printf ("Entre com o numero total de funcionarios: \t");
				scanf ("%f", &b);
				
				resultado = (totPessoasCont + a);///2/b * 100;
				resultado = resultado / 2;
				resultado = (resultado / b) * 100;
				
				printf ("\n\t O turnover de admissoes e desligamentos e: %.2f porcento", resultado);
				break;
			case 2:	
				printf ("Entre com o numero de pessoas demitidas: \t");
				scanf ("%f", &a);
				
				printf ("Entre com o numero total de funcionarios: \t");
				scanf ("%f", &b);
				
				resultado = (a / b)*100;
				
				printf ("\n\t O turnover de desligamentos e: %.2f porcento", resultado);
				break;
				
				default:
				printf ("\n\tDigite uma opcao valida\n");
				break;
	}
			printf ("\n Digite 1 para continuar: ");
			scanf ("%i", &op);
		
		
	}else if (op == 5){
		printf ("\n\t DEPARTAMENTO - TECNOLOGIA DA INFORMACAO \n");
		printf ("Escolha a operacao que deseja fazer no setor de tecnologia da informacao\n\t");	
		printf ("\n\t1 - CALCULAR NUMERO DE CHAMADOS POR FUNCIONARIO DA EMPRESA\n\t2 - INVESTIMENTO NA AREA POR PROFISSIONAL DA EMPRESA\n\n\t");
		scanf ("%i", &op);
		
		switch (op){
			case 1:
				printf ("Entre com o numero de chamados: \t");
				scanf ("%f", &a);
				
				printf ("Entre com o numero de funcionarios da empresa: \t");
				scanf ("%f", &b);
				
				resultado = a / b;
				
				printf ("\nO numero de chamados por funcionario da empresa e de aproximadamente: %.1f", resultado);
				break;
			case 2:
				printf ("Entre com o total de valor investido: \t");
				scanf ("%f", &a);
				
				printf ("Entre com o numero de funcionarios da empresa: \t");
				scanf ("%f", &b);
				
				resultado = a / b;
				
				printf ("\nO investimento na area por profissional da empresa e de aproximadamente: R$%.2f", resultado);
				break;
				
				default:
				printf ("\n\tDigite uma opcao valida\n");
				break;
	}
			printf ("\n Digite 1 para continuar: ");
			scanf ("%i", &op);
		}else if (op == 6){
		printf ("\n\t DEPARTAMENTO - ADMINISTRATIVO \n");
		printf ("\n\t CALCULAR METRO QUADRADO DISPONIVEL PARA CADA FUNCIOANRIO E A QUANTIDADE DE FUNCIONARIOS QUE IRAO EFETUAR A LIMPEZA\n\n\t");
		
		printf ("Entre com o total de metros quadrados: \t");
		scanf ("%f", &a);
				
		printf ("Entre com o numero de funcionarios da empresa: \t");
		scanf ("%f", &b);
		
			resultado = a / b;
		
		printf ("\nO total de metros quadrados para cada funcionario e: %.2f m² \n", resultado);
			
				
		if (b <= 50){
		b = 2;
			printf ("Apenas %f funcionarios farao a limpeza do local", b);
		}else{
			b = b + 2;
			printf ("%f funcionarios farao a limpeza", b);
			break;
		}
  }
			printf ("\n Digite 1 para continuar: ");
			scanf ("%i", &op);
	}
	while (op == 1);
	getch();
	system ("PAUSE");
	return 0;
}




