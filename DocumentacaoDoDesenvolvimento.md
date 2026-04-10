# Documentacao Do Desenvolvimento

Este arquivo apresenta algumas partes do processo de desenvolvimento da linguagem e seu analisador lexico.

1. Definicao dos tipos:
    1. Foi observado que na linguagem C/C++ existe varios tipo para variaveis e alguns sao redudantes entao a redundancia foi removida.
    2. Os tipos inteiro(int) e ponto flutuante(float) agora possuem um indicativo do numero de bits que tais usam, por exemplo um byte(8 bits) agora é chamdo de "int8" e double(32 bits) agora é chamado de "float32"
    3. Existe tambem um versao para inteiros sem sinal uint, em diversos momentos a existencia de um valor negativo nao é significante.
    4. O tipo boleano e o tipo char tambem foram criados, porem tais nao tem variacoes, sendo char ate redundantes com o "int8".

2. variaveis:
    1. O nome de variaveis como de funcoes so pode iniciar com uma letra minuscola de [a-z]. Isso foi decidido baseado em convencao.
    2. Pode ser qualquer nome desde que nao seja uma palavra reservada
3. Tipos de valores
    1. existe algum valores para numeros inteiros, reais, boleanos e char.
    2. Para char alem da maioria dos caracteries, ele ainda aceita da suporte para:
        1. '\n'
        2. '\t'
        3. '\r'
        4. '\\'
        5. '\''
        6. '\\'
    3. Para valores boleanos temos "true" e "false" como palavras reservadas.
4. Blocos de comentarios:
    1. Escolhemos os blocos de comentarios padroes da maioria das linguaguens no mercado, tendo em vista que ja estao bem estabelecidos.
5. Comandos:
    1. Para termos os primeiros comandos funcionando, precisamos definir oque seria um comando para a linguaguem.
    2. Inicialmente era apenas declaracao de variaveis porem abrangemos o cenario para:
       1. declare
       2. assignment
       3. expression
       4. conditional statement
       5. loop/iteration statement
       6. block
   3. Foi definido tudo isso como comandos basicos que deveria ser possiveis de se chamar em qualquer lugar, exceto no meio de definicao de classes e structs que permitem apenas declare.
  
6. Expressoes:
7.  
