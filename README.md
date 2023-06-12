# Lista-Final
//ENTRADA, PROCESSAMENTO E SAÍDA
//1)

    #include <stdio.h>
    #define PI 3.14

    int main() 
    {
    
    float raio, diametro, comprimento, area;

    // Solicitar o raio da circunferência
    printf("Digite o raio da circunferência: ");
    scanf("%f", &raio);

    // Calcular o diâmetro
    diametro = 2 * raio;

    // Calcular o comprimento
    comprimento = 2 * PI * raio;

    // Calcular a área
    area = PI * raio * raio;

    // Exibir os resultados
    printf("Diâmetro: %.2f\n", diametro);
    printf("Comprimento: %.2f\n", comprimento);
    printf("Área: %.2f\n", area);

    return 0;}

//2)

    #include <stdio.h>

    int main() {
    int numero;

    printf("Digite um número inteiro: ");
    scanf("%d", &numero);

    printf("Antecessor: %d\n", numero - 1);
    printf("Sucessor: %d\n", numero + 1);

    return 0;}

//3)

    #include <stdio.h>

    int main() 
    {
    
    float metros, decimetros, centimetros, milimetros;

    printf("Digite um valor em metros: ");
    scanf("%f", &metros);

    decimetros = metros * 10;
    centimetros = metros * 100;
    milimetros = metros * 1000;

    printf("Valor em decímetros: %.2f\n", decimetros);
    printf("Valor em centímetros: %.2f\n", centimetros);
    printf("Valor em milímetros: %.2f\n", milimetros);

    return 0;}

//4)

    #include <stdio.h>

    int main() 
    {
    
    int numero;

    printf("Números ímpares de 1 a 100:\n");

    for (numero = 1; numero <= 100; numero++) {
        if (numero % 2 != 0) {
            printf("%d ", numero);
        }
    }

    printf("\n");

    return 0;}

//5)

    #include <stdio.h>

    int main() 
    {
    
    int numero;

    printf("Números pares de 1 a 100:\n");

    for (numero = 2; numero <= 100; numero += 2) {
        printf("%d ", numero);
    }

    printf("\n");

    return 0;}

//6)

    #include <stdio.h>
    #include <math.h>

    int main() 
    {
    
    float numero1, numero2;
    float soma, produto, quadrado1, raizQuadrada, seno;

    printf("Digite o primeiro número: ");
    scanf("%f", &numero1);

    printf("Digite o segundo número: ");
    scanf("%f", &numero2);

    // a) A soma dos números
    soma = numero1 + numero2;
    printf("Soma dos números: %.2f\n", soma);

    // b) O produto do primeiro número pelo quadrado do segundo
    produto = numero1 * pow(numero2, 2);
    printf("Produto do primeiro número pelo quadrado do segundo: %.2f\n", produto);

    // c) O quadrado do primeiro número
    quadrado1 = pow(numero1, 2);
    printf("Quadrado do primeiro número: %.2f\n", quadrado1);

    // d) A raiz quadrada da soma dos quadrados
    raizQuadrada = sqrt(pow(numero1, 2) + pow(numero2, 2));
    printf("Raiz quadrada da soma dos quadrados: %.2f\n", raizQuadrada);

    // e) O seno da diferença do primeiro número pelo segundo
    seno = sin(numero1 - numero2);
    printf("Seno da diferença do primeiro número pelo segundo: %.2f\n", seno);
    return 0;}

//7)

    #include <stdio.h>

    int main() 
    {
    
    char nome[50];
    printf("Digite o nome: ");
    scanf("%s", nome);

    printf("As 4 primeiras letras do nome: %.4s\n", nome);
    return 0;}

//8)

    #include <stdio.h>

    int main() 
    {
    
    float preco, novoPreco;
    float desconto = 0.09; // 9% de desconto

    printf("Digite o preço do produto: ");
    scanf("%f", &preco);

    novoPreco = preco - (preco * desconto);

    printf("Novo preço com desconto de 9%%: %.2f\n", novoPreco);
    return 0;}

//9)

    #include <stdio.h>

    int main() 
    {
    
    float tempo, velocidade, distancia;

    printf("Digite o tempo gasto na viagem (em horas): ");
    scanf("%f", &tempo);

    printf("Digite a velocidade média (em km/h): ");
    scanf("%f", &velocidade);
    distancia = tempo * velocidade;
    printf("Distância percorrida: %.2f km\n", distancia);
    return 0;}




//10)
    #include <stdio.h>

    int main() 
    {
    
    int numero;

    printf("Digite um número decimal: ");
    scanf("%d", &numero);

    printf("Número em hexadecimal: %x\n", numero);
    printf("Número em octal: %o\n", numero);

    return 0;}

//11)

    #include <stdio.h>

    int main()
    {
    
    float valorHoraAula, salarioBruto, salarioLiquido;
    int numAulas;
    float descontoINSS;

    // Solicitar os valores do usuário
    printf("Digite o valor da hora-aula: ");
    scanf("%f", &valorHoraAula);

    printf("Digite o número de aulas dadas: ");
    scanf("%d", &numAulas);

    printf("Digite a porcentagem de desconto do INSS: ");
    scanf("%f", &descontoINSS);

    // Calcular o salário bruto
    salarioBruto = valorHoraAula * numAulas;

    // Calcular o valor do desconto do INSS
    float desconto = salarioBruto * (descontoINSS / 100.0);

    // Calcular o salário líquido
    salarioLiquido = salarioBruto - desconto;

    // Exibir o resultado
    printf("Salário Líquido: R$%.2f\n", salarioLiquido);

    return 0;}

//12)

    #include <stdio.h>

    int main() 
    {
    
    int num1, num2;
    char operacao;

    printf("Digite o primeiro número: ");
    scanf("%d", &num1);

    printf("Digite a operação (+, -, *, /): ");
    scanf(" %c", &operacao);

    printf("Digite o segundo número: ");
    scanf("%d", &num2);

    switch (operacao) {
        case '+':
            printf("Resultado: %d\n", num1 + num2);
            break;
        case '-':
            printf("Resultado: %d\n", num1 - num2);
            break;
        case '*':
            printf("Resultado: %d\n", num1 * num2);
            break;
        case '/':
            if (num2 != 0) {
                printf("Resultado: %.2f\n", (float)num1 / num2);
            } else {
                printf("Erro: divisão por zero.\n");
            }
            break;
        default:
            printf("Operação inválida.\n");
            break;
    }
    return 0;}

//IF E ELSE

//13)

    #include <stdio.h>

    int main() 
    {
    
    int idade;

    printf("Digite a idade da pessoa: ");
    scanf("%d", &idade);

    if (idade >= 18 && idade <= 67) {
        printf("A pessoa pode doar sangue.\n");
    } else {
        printf("A pessoa não pode doar sangue.\n");
    }
    return 0;}

//14)

    #include <stdio.h>

    int main() {
    
    int numero;

    printf("Digite um número inteiro: ");
    scanf("%d", &numero);

    if (numero % 2 == 0) {
        printf("O número é par.\n");
    } else {
        printf("O número é ímpar.\n");
    }
    return 0;}

//15)

    #include <stdio.h>

    int main() {
    
    int idade;

    printf("Digite a idade: ");
    scanf("%d", &idade);

    if (idade >= 10 && idade <= 14) {
        printf("Categoria: Infantil\n");
    } else if (idade >= 15 && idade <= 17) {
        printf("Categoria: Juvenil\n");
    } else if (idade >= 18 && idade <= 25) {
        printf("Categoria: Adulto\n");
    } else {
        printf("Idade inválida\n");
    }

    return 0;}

//16)

    #include <stdio.h>
    #include <math.h>

    int main() {
    
    float numero;

    printf("Digite um número: ");
    scanf("%f", &numero);

    if (numero >= 0) {
        printf("Raiz quadrada: %.2f\n", sqrt(numero));
    } else {
        printf("Elevado ao quadrado: %.2f\n", pow(numero, 2));
    }

    return 0;}
//17)

    #include <stdio.h>

    int main() {
    
    int numero;

    printf("Digite um número: ");
    scanf("%d", &numero);

    if (numero % 10 == 0) {
        printf("Divisível por 10\n");
    } else if (numero % 5 == 0) {
        printf("Divisível por 5\n");
    } else if (numero % 2 == 0) {
        printf("Divisível por 2\n");
    } else {
        printf("Não é divisível por 10, 5 ou 2\n");
    }
    return 0;}

//18)

    #include <stdio.h>

    int main() {
    
    float valorCompra, valorVenda;
    float lucro;

    printf("Digite o valor da compra: ");
    scanf("%f", &valorCompra);

    if (valorCompra < 20.00) {
        lucro = 0.45;  // 45% de lucro
    } else {
        lucro = 0.30;  // 30% de lucro
    }
    valorVenda = valorCompra + (valorCompra * lucro);
    printf("Valor da venda: %.2f\n", valorVenda);
    return 0;}

//19)


    #include <stdio.h>

    int main() {
    
    int idade;

    printf("Digite a idade: ");
    scanf("%d", &idade);

    if (idade < 16) {
        printf("Não-eleitor\n");
    } else if (idade >= 18 && idade <= 65) {
        printf("Eleitor obrigatório\n");
    } else if ((idade >= 16 && idade < 18) || idade > 65) {
        printf("Eleitor facultativo\n");
    } else {
        printf("Idade inválida\n");
    }

    return 0;}
//20)

    #include <stdio.h>
    int main() {
    
    
    int num1, num2, num3;

    printf("Digite o primeiro número: ");
    scanf("%d", &num1);

    printf("Digite o segundo número: ");
    scanf("%d", &num2);

    printf("Digite o terceiro número: ");
    scanf("%d", &num3);
    if (num1 <= num2 && num1 <= num3) {
        if (num2 <= num3) {
            printf("Ordem crescente: %d, %d, %d\n", num1, num2, num3);
        } else {
            printf("Ordem crescente: %d, %d, %d\n", num1, num3, num2);
        }
    } else if (num2 <= num1 && num2 <= num3) {
        if (num1 <= num3) {
            printf("Ordem crescente: %d, %d, %d\n", num2, num1, num3);
        } else {
            printf("Ordem crescente: %d, %d, %d\n", num2, num3, num1);
        }
    } else {
        if (num1 <= num2) {
            printf("Ordem crescente: %d, %d, %d\n", num3, num1, num2);
        } else {
            printf("Ordem crescente: %d, %d, %d\n", num3, num2, num1);
        }
    }
    return 0;}
//21)

    #include <stdio.h>

    int main() {
    
    int lado1, lado2, lado3;

    printf("Digite o valor do primeiro lado: ");
    scanf("%d", &lado1);

    printf("Digite o valor do segundo lado: ");
    scanf("%d", &lado2);

    printf("Digite o valor do terceiro lado: ");
    scanf("%d", &lado3);

    if (lado1 == lado2 && lado2 == lado3) {
        printf("Triângulo equilátero\n");
    } else if (lado1 != lado2 && lado1 != lado3 && lado2 != lado3) {
        printf("Triângulo escaleno\n");
    } else {
        printf("Triângulo isósceles\n");
    }

    return 0;}

//22)

    #include <stdio.h>

    int main() {
    
    int dia, mes, ano;

    printf("Digite o dia do aniversário: ");
    scanf("%d", &dia);

    printf("Digite o mês do aniversário: ");
    scanf("%d", &mes);

    printf("Digite o ano do aniversário: ");
    scanf("%d", &ano);

    if (ano == 2023) {
        if (mes >= 1 && mes <= 12) {
            if (dia >= 1 && dia <= 31) {
                printf("Data de aniversário válida.\n");
            } else {
                printf("Dia inválido.\n");
            }
        } else {
            printf("Mês inválido.\n");
        }
    } else {
        printf("Ano inválido.\n");
    }

    return 0;}

//SWITCH
//23)

    #include <stdio.h>

    int main() {

    int mes;

    printf("Digite o número do mês (1-12): ");
    scanf("%d", &mes);

    switch (mes) {
        case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
        case 12:
            printf("O mês possui 31 dias.\n");
            break;
        case 4:
        case 6:
        case 9:
        case 11:
            printf("O mês possui 30 dias.\n");
            break;
        case 2:
            printf("O mês possui 28 ou 29 dias.\n");
            break;
        default:
            printf("Mês inválido.\n");
            break;
    }

    return 0;}

//24)

    #include <stdio.h>

    int main() {

    char tipoCarro;
    float distancia, consumo;

    printf("Digite o tipo de carro (A, B ou C): ");
    scanf(" %c", &tipoCarro);

    printf("Digite a distância rodada em km: ");
    scanf("%f", &distancia);

    switch (tipoCarro) {
        case 'A':
        case 'a':
            consumo = distancia / 8;
            break;
        case 'B':
        case 'b':
            consumo = distancia / 9;
            break;
        case 'C':
        case 'c':
            consumo = distancia / 12;
            break;
        default:
            printf("Tipo de carro inválido.\n");
            return 0;
    }

    printf("O consumo estimado é de %.2f km/litro.\n", consumo);

    return 0;}

//DO, WHILE
//25)

    #include <stdio.h>

    int main() {

    int numAlunos, contador = 0;
    float nota, soma = 0.0, media;

    printf("Digite o número de alunos na sala: ");
    scanf("%d", &numAlunos);

    while (contador < numAlunos) {
        printf("Digite a nota do aluno %d: ", contador + 1);
        scanf("%f", &nota);
        soma += nota;
        contador++;
    }

    media = soma / numAlunos;

    printf("A média da turma é: %.2f\n", media);

    return 0;
}


//26)
    
    #include <stdio.h>

    int main() {

    int lado, i, j;

    printf("Digite o tamanho do lado do quadrado (1-20): ");
    scanf("%d", &lado);

    if (lado < 1 || lado > 20) {
        printf("Tamanho inválido.\n");
        return 0;
    }

    i = 1;
    while (i <= lado) {
        j = 1;
        while (j <= lado) {
            printf("* ");
            j++;
        }
        printf("\n");
        i++;
    }

    return 0;
}

//27)

    #include <stdio.h>

    int main() {

    int numero, i = 1;

    printf("Digite um número: ");
    scanf("%d", &numero);

    printf("Tabuada de %d:\n", numero);

    do {
        printf("%d x %d = %d\n", numero, i, numero * i);
        i++;
    } while (i <= 10);

    return 0;}

//28)

    #include <stdio.h>

    int main() {

    int idade, contador = 1;
    float peso, media1_10 = 0, media11_20 = 0, media21_30 = 0, media30 = 0;
    int quantidade1_10 = 0, quantidade11_20 = 0, quantidade21_30 = 0, quantidade30 = 0;

    while (contador <= 15) {
        printf("Digite a idade da pessoa %d: ", contador);
        scanf("%d", &idade);

        printf("Digite o peso da pessoa %d: ", contador);
        scanf("%f", &peso);

        if (idade >= 1 && idade <= 10) {
            media1_10 += peso;
            quantidade1_10++;
        } else if (idade >= 11 && idade <= 20) {
            media11_20 += peso;
            quantidade11_20++;
        } else if (idade >= 21 && idade <= 30) {
            media21_30 += peso;
            quantidade21_30++;
        } else {
            media30 += peso;
            quantidade30++;
        }

        contador++;
    }

    if (quantidade1_10 > 0) {
        media1_10 /= quantidade1_10;
        printf("Média de peso das pessoas de 1 a 10 anos: %.2f\n", media1_10);
        printf("Quantidade de pessoas de 1 a 10 anos: %d\n", quantidade1_10);
    } else {
        printf("Nenhuma pessoa de 1 a 10 anos.\n");
    }

    if (quantidade11_20 > 0) {
        media11_20 /= quantidade11_20;
        printf("Média de peso das pessoas de 11 a 20 anos: %.2f\n", media11_20);
        printf("Quantidade de pessoas de 11 a 20 anos: %d\n", quantidade11_20);
    } else {
        printf("Nenhuma pessoa de 11 a 20 anos.\n");
    }

    if (quantidade21_30 > 0) {
        media21_30 /= quantidade21_30;
        printf("Média de peso das pessoas de 21 a 30 anos: %.2f\n", media21_30);
        printf("Quantidade de pessoas de 21 a 30 anos: %d\n", quantidade21_30);
    } else {
        printf("Nenhuma pessoa de 21 a 30 anos.\n");
    }

    if (quantidade30 > 0) {
        media30 /= quantidade30;
        printf("Média de peso das pessoas com mais de 30 anos: %.2f\n", media30);
        printf("Quantidade de pessoas com mais de 30 anos: %d\n", quantidade30);
    } else {
        printf("Nenhuma pessoa com mais de 30 anos.\n");
    }
    return 0;}

//29)

    #include <stdio.h>

    int main() {

    int contador_aluno = 1;
    float nota1, nota2, nota3, nota4;
    float media_aluno, media_turma = 0;
    int pontos_recuperacao, total_alunos = 5;

    while (contador_aluno <= total_alunos) {
        printf("Digite as notas do aluno %d:\n", contador_aluno);

        printf("Nota 1 (peso 3): ");
        scanf("%f", &nota1);

        printf("Nota 2 (peso 2): ");
        scanf("%f", &nota2);

        printf("Nota 3 (peso 1): ");
        scanf("%f", &nota3);

        printf("Nota 4 (peso 1): ");
        scanf("%f", &nota4);

        media_aluno = (nota1 * 3 + nota2 * 2 + nota3 * 1 + nota4 * 1) / 7;
        media_turma += media_aluno;

        printf("Média do aluno %d: %.2f\n", contador_aluno, media_aluno);

        if (media_aluno >= 6.0) {
            printf("Situação: Aprovado\n");
        } else if (media_aluno >= 4.0) {
            pontos_recuperacao = 10 - media_aluno;
            printf("Situação: Recuperação (faltam %d pontos para ser aprovado)\n", pontos_recuperacao);
        } else {
            printf("Situação: Reprovado\n");
        }

        printf("--------------------\n");

        contador_aluno++;
    }

    media_turma /= total_alunos;
    printf("Média da turma: %.2f\n", media_turma);
    return 0;}

//FOR
//30)

    #include <stdio.h>

    int main() {
    int lista[10];
    int opcao, i;

    printf("Digite 10 valores inteiros:\n");
    for (i = 0; i < 10; i++) {
        printf("Valor %d: ", i + 1);
        scanf("%d", &lista[i]);
    }

    printf("Escolha uma opção:\n");
    printf("1 - Listar em ordem crescente\n");
    printf("2 - Listar em ordem decrescente\n");
    printf("3 - Listar na ordem original\n");
    scanf("%d", &opcao);

    switch (opcao) {
        case 1:
            printf("Valores em ordem crescente:\n");
            for (i = 0; i < 10; i++) {
                printf("%d ", lista[i]);
            }
            break;
        case 2:
            printf("Valores em ordem decrescente:\n");
            for (i = 9; i >= 0; i--) {
                printf("%d ", lista[i]);
            }
            break;
        case 3:
            printf("Valores na ordem original:\n");
            for (i = 0; i < 10; i++) {
                printf("%d ", lista[i]);
            }
            break;
        default:
            printf("Opção inválida.\n");
            break;
    }

    return 0;}

//31)

    #include <stdio.h>

    int main() {

    int numero, i;

    printf("Digite um número: ");
    scanf("%d", &numero);

    printf("Tabuada de multiplicação de %d:\n", numero);
    for (i = 0; i <= 10; i++) {
        printf("%d x %d = %d\n", numero, i, numero * i);
    }
    return 0;}
