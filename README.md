1 -

 #include <stdio.h>
#include <string.h>

int main() {
    char string[100]; // Array de caracteres para armazenar a string

    printf("Digite uma string: ");
    fgets(string, 100, stdin); // Lê até 99 caracteres da entrada padrão (stdin) e armazena em 'string'

    string[strcspn(string, "\n")] = 0;

    printf("Você digitou: %s\n", string);

    int comprimento = strlen(string);
    printf("O comprimento da string é: %d caracteres\n", comprimento);

    return 0;
}

2- 

#include <stdio.h>
#include <string.h>

int main() {
    char string1[100], string2[100];

    printf("Digite a primeira string: ");
    fgets(string1, 100, stdin);
    string1[strcspn(string1, "\n")] = 0;

    printf("Digite a segunda string: ");
    fgets(string2, 100, stdin);
    string2[strcspn(string2, "\n")] = 0;

    int resultado = strcmp(string1, string2);

    if (resultado == 0) {
        printf("As strings são iguais.\n");
    } else {
        printf("As strings são diferentes.\n");
    }

    return 0;
}

3-

#include <stdio.h>

int main() {
    char string[100];

    printf("Digite uma string: ");
    fgets(string, 100, stdin);

    string[strcspn(string, "\n")] = 0;

    for (int i = 0; string[i] != '\0'; i++) {
        printf("%c\n", string[i]);
    }

    return 0;
}


4-

#include <stdio.h>

int main() {
    char string[100];
    int contador = 0;

    printf("Digite uma string: ");
    fgets(string, 100, stdin);

    string[strcspn(string, "\n")] = 0;

    for (int i = 0; string[i] != '\0'; i++) {
        if (string[i] == 'a') {
            contador++;
        }
    }

    printf("O caractere 'a' aparece %d vezes na string.\n", contador);

    return 0;
}


5-

#include <stdio.h>
#include <string.h>

int main() {
    char string1[100], string2[100];

    printf("Digite uma string: ");
    fgets(string1, 100, stdin);
    string1[strcspn(string1, "\n")] = 0;

    strcpy(string2, string1);

    printf("String original: %s\n", string1);
    printf("String copiada: %s\n", string2);

    return 0;
}

6-

#include <stdio.h>
#include <string.h>

int main() {
    char string1[100], string2[100], string_concatenada[200];

    printf("Digite a primeira string: ");
    fgets(string1, 100, stdin);
    string1[strcspn(string1, "\n")] = 0;

    printf("Digite a segunda string: ");
    fgets(string2, 100, stdin);
    string2[strcspn(string2, "\n")] = 0;

    strcpy(string_concatenada, string1);
    strcat(string_concatenada, string2);

    printf("String concatenada: %s\n", string_concatenada);

    return 0;
}


7-

#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char string[100];

    printf("Digite uma string: ");
    fgets(string, 100, stdin);
    string[strcspn(string, "\n")] = 0;

    for (int i = 0; string[i] != '\0'; i++) {
        string[i] = toupper(string[i]);
    }

    printf("String em maiúsculas: %s\n", string);

    return 0;
}


8-

#include <stdio.h>
#include <ctype.h>

int main() {
    char string[100];
    int contador_vogais = 0;

    printf("Digite uma string: ");
    fgets(string, 100, stdin);
    string[strcspn(string, "\n")] = 0;

    for (int i = 0; string[i] != '\0'; i++) {
        char c = tolower(string[i]);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            contador_vogais++;
        }
    }

    printf("A string possui %d vogais.\n", contador_vogais);

    return 0;
}



9-

#include <stdio.h>

int main() {
    char string[100];
    int contador_espacos = 0;

    printf("Digite uma string: ");
    fgets(string, 100, stdin);
    string[strcspn(string, "\n")] = 0;

    for (int i = 0; string[i] != '\0'; i++) {
        if (string[i] == ' ') {
            contador_espacos++;
        }
    }

    printf("A string possui %d espaços em branco.\n", contador_espacos);

    return 0;
}


10-

#include <stdio.h>
#include <ctype.h>

int main() {
    char string[100];
    int letras = 0, digitos = 0, especiais = 0;

    printf("Digite uma string: ");
    fgets(string, 100, stdin);
    string[strcspn(string, "\n")] = 0;

    for (int i = 0; string[i] != '\0'; i++) {
        if (isalpha(string[i])) {
            letras++;
        } else if (isdigit(string[i])) {
            digitos++;
        } else {
            especiais++;
        }
    }

    printf("A string possui:\n");
    printf("%d letras\n", letras);
    printf("%d dígitos\n", digitos);
    printf("%d caracteres especiais\n", especiais);

    return 0;
}





