# CPiscine
Fundamentals C / Exercício 00: ft_putchar    
Escreva uma função que mostre o caractere passado como parâmetro.
Deve ser prototipada da seguinte maneira:
    
    void ft_putchar(char c);

Para mostrar o caractere, deve usar a função write da seguinte maneira:

    write(1, &c, 1);


#Resolution
1. Create a file:
  
        vim ft_putchar.c
    Vim é um editor de texto, usado para programar e editar ficheiros de texto no terminal (linha de comandos).
    Como funciona (modo básico)?
       Modo Normal: para navegar, copiar, colar, apagar texto, etc.
       Modo Inserção: para escrever texto (como num editor normal).
       Modo Comando: para salvar, sair, procurar, substituir, etc.

2. Write code:
  (:Stdheader or F1) The 42 header - a.k.a start a file with style
  Pressione i para entrar no modo inserção.
  Escreva seu código C normalmente:

        #include <unistd.h>
        
        void    ft_putchar(char c)
        {
                write(1, &c, 1);
        }
        
        int     main(void)
        {
                ft_putchar('a');
                return (0);
        }
   
[How to]:
#include <unistd.h> → é uma diretiva de pré-processador em C, que indica ao compilador para incluir o conteúdo do ficheiro unistd.h. Este ficheiro faz parte das bibliotecas POSIX e fornece acesso a várias funções de sistema que lidam com input/output, processos, ficheiros, entre outros.
A função write() é uma função de sistema (system call) fornecida pelo sistema operativo através da interface POSIX. write() → escreve dados num ficheiro ou no terminal (ex: write(1, &c, 1);

[O que acontece com o código (3. Escrever código)]?
A função ft_putchar recebe um carácter c (no caso, 'a').
Chama write(1, &c, 1);:
    1 é o descritor para stdout (terminal).
    &c é o endereço do carácter 'a' na memória.
    1 indica que queremos escrever 1 byte (1 carácter).

Por isso, o carácter 'a' é enviado para o terminal e aparece na tela.

    write(1, "Olá\n", 4);
> Isto envia os 4 caracteres "O", "l", "á" e "\n" para o terminal (stdout).
| Código | Significado                           |
| ------ | ------------------------------------- |
| `c`    | O valor da variável (ex: `'A'`)       |
| `&c`   | O **endereço** da variável na memória |


3. Save and Exit:
  Pressione Esc para voltar ao modo normal.
  
          Para salvar: :w + Enter
          Para sair: :q + Enter
          Para salvar e sair juntos: :wq + Enter
          Para sair sem salvar: :q! + Enter

4. Compile C code via terminal:

          cc -Wall -Wextra -Werror ft_putchar.c
    > A Moulinette compila com as textitflags -Wall -Wextra -Werror, e utiliza cc

5. View created files (ls):
    a.out  ft_putchar.c
Para executar o programa e ver o resultado (como imprimir o caractere 'a' no terminal), usas:
  
        ./a.out
    ./ significa "diretório atual"
    a.out é o nome do programa executável


