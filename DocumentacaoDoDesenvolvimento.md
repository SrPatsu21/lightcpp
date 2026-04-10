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
    1. Suporte as 4 operacoes basicas; operacoes de incremento ("++" "--"); shift; operacoes ralacionais; modulo.
    2. A operacao mais complicada de se constuir foi a de incremento quando nao ha atribuição ex("a++;" ou "--a;"). Motivo disso é que a linguaguem proibe a chamada de variaveis e expressoes sem objetivo. Isso significa que a expressao precisa ser entendida como alterando uma variavel ou tendo o valor consumido, e ja que nao é uma atribuicao muito explicita, essa parte foi mais dificil.
  
7. Atribuição:
    1. O analisador n distingue tipos entao qualquer valor do citados anteriormente pode ser atribuido a qualquer variavel. Valores tambem englobam expressoes.
    2. Tambem temos suporte a operadores de atribuicao ("+=", "/="), que vao alem de apenas atribuir um valor.
  
8. Include:
    1. comando include foi adicionado para possibilitar a inclusao de arquivos.
  
9. funcoes:
    1. funcoes como variaveis precisam comecar com letra minuscola.
    2. O uso do "(" e ")" é obrigatorio para identificar uma funcao.
    3. Funcoes podem ser chamadas em qualquer momento.
    4. A funcao pode ser apenas declarada, isso permite que ela seja definida posteriormente.

10. if
    1. Ate entao o unico conditional statement da linguaguem.
    2. Permite recursividade.
    3. Nao é possivel crialo sem um bloco de comando "{ }"
    4. Se o trabalho continuar a adicao de um comando "switch" como o comando na linguagem C.

11. For, while, do while
    1. sao os 3 unicos loops da linguaguem
    2. Considerase cada um unico e exencial
    3. Apesar do "do while" ser raramente usado, consideramos que, nao podemos escolher simplicidade encima de performance.
   
12. Classe e Struct
    1. Devem iniciar com letra maiuscola para diferenciar das variaveis e funcoes
    2. Foi decidido que apesar de nao ser comum usar construtores(ou destrutores) em struct é permitido, sendo a unica coisa que diferencia as duas estruturas de dados é o polimorfismo que a classe pode possuir.
    3. O construtor é praticamente uma funcao que inicia com letra maiuscola e o destrutor é um construtor que nao permite parametros.
   
13. Acesso a memoria
    1. atualmente nao temos arrays e nem ponteiros
    2. Ja temos 2 operadoes "*" e "&" ambos exerceriam a mesma funcao que em programas C.
