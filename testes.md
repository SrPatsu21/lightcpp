# Documentação dos testes

Os testes serão feitos usando as seguintes diretrizes:

- teste01-teste10: testes completamente corretos
- teste11-teste20: testes completamente errados
- teste21-teste25: testes parcialmente errados

Importante mencionar que no segundo conjunto de testes não havera nada correto, portanto seria apenas lixo de fonte.txt, mas no terceiro conjunto haverá uma escrita correta em sua maioria porém em um único momento haverá um erro introduzido propositalmente. Por exemplo um código que reconheca apenas a letra 'b' em cada conjunto de testes seria assim:

- primeiro conjunto: bbbb
- segundo conjunto: a
- terceiro conjunto: bbbabb

Os testes estão localizados na pasta 'tests'

## Tabela de testes

A seguinte tabela demonstra cada teste e sua peculiaridade

| **Teste** | **Tipo**      | **Objetivo**                                      |
|-----------|---------------|---------------------------------------------------|
| teste01   | Sucesso       | Declaraçao e atribuição de variavel               |
| teste02   | Sucesso       | Expressoes e atribuiçao em variavel               |
| teste03   | Sucesso       | Estrutura condicional IF                          |
| teste04   | Sucesso       | Estrutura de repetiçao WHILE, FOR, DO-WHILE       |
| teste05   | Sucesso       | Funçoes                                           |
| teste06   | Sucesso       | Blocos                                            |
| teste07   | Sucesso       | Funçoes com retorno                               |
| teste08   | Sucesso       | Struct's                                          |
| teste09   | Sucesso       | Class                                             |
| teste10   | Sucesso       | Include de outros arquivos                        |
| teste11   | Erro completo | Falta o ;                                         |
| teste12   | Erro completo | Operador quebrado                                 |
| teste13   | Erro completo | IF quebrado                                       |
| teste14   | Erro completo | bloco não fechado                                 |
| teste15   | Erro completo | else inválido                                     |
| teste16   | Erro completo | for inválido                                      |
| teste17   | Erro completo | função quebrada                                   |
| teste18   | Erro completo | return inválido                                   |
| teste19   | Erro completo | include errado                                    |
| teste20   | Erro completo | expressão inválida                                |
| teste21   | Erro parcial  | Removido um "-" na linha 2, fonte teste02         |
| teste22   | Erro parcial  | Removido um "resultado" na linha 9, fonte teste05 |
| teste23   | Erro parcial  | Removido um "," na linha 7, fonte teste08         |
| teste24   | Erro parcial  | Removido um ":" na linha 26, fonte teste09        |
| teste25   | Erro parcial  | Removido um "=" na linha 9, fonte teste04         |
