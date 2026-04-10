# Documentação do Desenvolvimento

Este arquivo apresenta algumas partes do processo de desenvolvimento da linguagem e seu analisador léxico.

1. Definição dos tipos:
    1. Foi observado que na linguagem C/C++ existem vários tipos para variáveis e alguns são redundantes, então a redundância foi removida.
    2. Os tipos inteiro (int) e ponto flutuante (float) agora possuem um indicativo do número de bits que utilizam. Por exemplo, um byte (8 bits) agora é chamado de "int8" e double (32 bits) agora é chamado de "float32".
    3. Existe também uma versão para inteiros sem sinal (uint); em diversos momentos a existência de um valor negativo não é significativa.
    4. O tipo booleano e o tipo char também foram criados, porém estes não têm variações, sendo char até redundante com o "int8".

2. Variáveis:
    1. O nome de variáveis, assim como o de funções, só pode iniciar com uma letra minúscula de [a-z]. Isso foi decidido baseado em convenção.
    2. Pode ser qualquer nome, desde que não seja uma palavra reservada.

3. Tipos de valores:
    1. Existem alguns valores para números inteiros, reais, booleanos e char.
    2. Para char, além da maioria dos caracteres, ele ainda aceita suporte para:
        1. '\n'
        2. '\t'
        3. '\r'
        4. '\\'
        5. '\''
        6. '\\'
    3. Para valores booleanos, temos "true" e "false" como palavras reservadas.

4. Blocos de comentários:
    1. Escolhemos os blocos de comentários padrões da maioria das linguagens no mercado, tendo em vista que já estão bem estabelecidos.

5. Comandos:
    1. Para termos os primeiros comandos funcionando, precisamos definir o que seria um comando para a linguagem.
    2. Inicialmente era apenas declaração de variáveis, porém abrangemos o cenário para:
       1. declare
       2. assignment
       3. expression
       4. conditional statement
       5. loop/iteration statement
       6. block
   3. Foi definido tudo isso como comandos básicos que devem ser possíveis de se chamar em qualquer lugar, exceto no meio de definição de classes e structs, que permitem apenas declare.
  
6. Expressões:
    1. Suporte às 4 operações básicas; operações de incremento ("++" "--"); shift; operações relacionais; módulo.
    2. A operação mais complicada de se construir foi a de incremento quando não há atribuição (ex.: "a++;" ou "--a;"). O motivo disso é que a linguagem proíbe a chamada de variáveis e expressões sem objetivo. Isso significa que a expressão precisa ser entendida como alterando uma variável ou tendo o valor consumido e, já que não é uma atribuição muito explícita, essa parte foi mais difícil.
  
7. Atribuição:
    1. O analisador não distingue tipos, então qualquer valor dos citados anteriormente pode ser atribuído a qualquer variável. Valores também englobam expressões.
    2. Também temos suporte a operadores de atribuição ("+=", "/="), que vão além de apenas atribuir um valor.
  
8. Include:
    1. O comando include foi adicionado para possibilitar a inclusão de arquivos.
  
9. Funções:
    1. Funções, assim como variáveis, precisam começar com letra minúscula.
    2. O uso de "(" e ")" é obrigatório para identificar uma função.
    3. Funções podem ser chamadas a qualquer momento.
    4. A função pode ser apenas declarada; isso permite que ela seja definida posteriormente.

10. If:
    1. Até então, o único conditional statement da linguagem.
    2. Permite recursividade.
    3. Não é possível criá-lo sem um bloco de comando "{ }".
    4. Se o trabalho continuar, há a possibilidade de adição de um comando "switch", como o da linguagem C.

11. For, while, do while:
    1. São os 3 únicos loops da linguagem.
    2. Considera-se cada um único e essencial.
    3. Apesar do "do while" ser raramente usado, consideramos que não podemos escolher simplicidade em detrimento da performance.
   
12. Classe e Struct:
    1. Devem iniciar com letra maiúscula para diferenciar das variáveis e funções.
    2. Foi decidido que, apesar de não ser comum usar construtores (ou destrutores) em struct, isso é permitido. A única coisa que diferencia as duas estruturas de dados é o polimorfismo que a classe pode possuir.
    3. O construtor é praticamente uma função que inicia com letra maiúscula, e o destrutor é um construtor que não permite parâmetros.
   
13. Acesso à memória:
    1. Atualmente não temos arrays nem ponteiros.
    2. Já temos 2 operadores "*" e "&", ambos exerceriam a mesma função que em programas C.
