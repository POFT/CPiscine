# CPiscine
Fundamentals C / Exercício 00: ft_putchar    
Escreva uma função que mostre o caractere passado como parâmetro.
Deve ser prototipada da seguinte maneira:
    
    void ft_putchar(char c);

Para mostrar o caractere, deve usar a função write da seguinte maneira:

    write(1, &c, 1);


#Solucao
1. Abrir um arquivo C no Vim:
  
        vim ft_putchar.c

2. Modos do Vim:
  Modo Normal: onde você navega e dá comandos (modo padrão ao abrir).
  Modo Inserção: para digitar código. Pressione i para entrar.
  Modo Comando: para salvar, sair, etc. Pressione [Esc]: para entrar.

3. Escrever código C:
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


4. Salvar e sair:
  Pressione Esc para voltar ao modo normal.
  
          Para salvar: :w + Enter
          Para sair: :q + Enter
          Para salvar e sair juntos: :wq + Enter
          Para sair sem salvar: :q! + Enter

5. Compilar o código C pelo terminal:

          cc -Wall -Wextra -Werror ft_putchar.c

6. Depois de olhar os ficheiros (ls) podemos ver um "a.out", vamos correr o comando local (print's the test):
  
        ./a.out



