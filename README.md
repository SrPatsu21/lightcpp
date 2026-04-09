# Documentação da Linguagem – Guia do Usuário

## 1. Introdução

LightCPP foi desenvolvida com base em conceitos da linguagem C/C++, sendo uma linguagem:

* Imperativa
* Tipada estaticamente
* Estruturada
* Com suporte básico a orientação a objetos

Ela permite a criação de programas com:

* Variáveis e constantes
* Expressões matemáticas e lógicas
* Estruturas de controle
* Funções
* Classes e structs
* Inclusão de arquivos

---

## 2. Tipos de Dados

### Inteiros

```
int, int8, int16, int32, int64
uint, uint8, uint16, uint32, uint64
```

### Ponto flutuante

```
float, float32, float64, float128
```

### Outros

```
char    // caractere
bool    // booleano (true ou false)
```

---

## 3. Identificadores

* Variáveis: começam com letra minúscula

  ```
  idade, total1, valorFinal
  ```

* Classes/Structs: começam com letra maiúscula

  ```
  Pessoa, Carro, ContaBancaria
  ```

---

## 📦 4. Declaração de Variáveis

### Sintaxe:

```
tipo nome;
tipo nome = valor;
```

### Exemplos:

```
int x;
int y = 10;
float media = 5.5;
bool ativo = true;
Cachorro class_ame;
```

### Múltiplas variáveis:

```
int a = 1, b = 2, c;
```

### Constantes:

```
const int valor = 100;
```

---

## 5. Expressões e Operadores

### Operadores aritméticos:

```
+  -  *  /  %
```

### Incremento:

```
x++;
x--;
++x;
```

### Operadores lógicos:

```
&&  ||  !
```

### Operadores relacionais:

```
<  >  <=  >=  ==  !=
```

### Exemplo:

```
x = (a + b) * 2;
if (x > 10 && ativo) { ... }
```

---

## 6. Atribuições

```
x = 10;
x += 5;
x -= 2;
```

---

## 7. Estruturas de Controle

### If

```
if (condicao) {
    // código
}
```

### Else If

```
if (x > 10) {
    ...
} else if (x > 5) {
    ...
} else {
    ...
}
```

### While

```
while (condicao) {
    // código
}
```

### Do While

```
do {
    // código
} while (condicao);
```

### For

```
for (int i = 0; i < 10; i++) {
    // código
}
```

---

## Blocos

Blocos são definidos por `{}`:

```
{
    int x = 10;
}
```

---

## Funções

### Declaração:

```
tipo nome(parâmetros) {
    // código
}
```

### Exemplo:

```
int soma(int a, int b) {
    a = a + b;
    return b;
}
```

### Função sem corpo:

```
int soma(int a, int b);
```

---

## Chamada de Funções

```
soma(10, 20);
```

---

## Classes

### Declaração:

```
class Nome {
    // membros
};
```

### Exemplo:

```
class Pessoa {
    public:
    int idade;

    int getIdade() {
        idade = idade;
    }
};
```

---

## Structs

```
struct Ponto {
    int x;
    int y;
};
```

---

## 13. Construtores

```
Pessoa(int idade) {
    idade = idade;
}
```

### Com herança:

```
Pessoa(int idade) : Humano(idade) {
}
```

---

## 14. Destrutores

```
~Pessoa() {
}
```

---

## 15. Modificadores de Acesso

```
public:
private:
protected:
```

---

## 16. Inclusão de Arquivos

```
#include <arquivo>
#include "arquivo"
```

---

## 17. Comentários

### Linha:

```
// comentário
```

### Bloco:

```
/* comentário */
```

---

## 18. Regras Gerais

* Todo comando simples termina com `;`
* Blocos usam `{ }`
* Identificadores devem seguir regras de letras
* Tipos devem ser declarados corretamente

---

## 19. Erros Comuns

### Falta de ponto e vírgula

```
int x = 10   // ERRO
```

### Tipo inválido

```
number x;   // ERRO
```

### Expressão inválida

```
x = + * 5;  // ERRO
```

---

## 20. Limitações da Linguagem

Atualmente, a linguagem **não suporta**:

* Arrays
* Operador ternário (`? :`)
* Comando `return`
* Alocação dinâmica de memória

---

## 21. Exemplo Completo

```
#include <stdio>

int soma(int a, int b) {
    a = a + b;
}

class Pessoa {
    public:
    int idade;
};

int main() {
    int x = 10;
    int y = 20;

    if (x < y) {
        x++;
    }

    for (int i = 0; i < 5; i++) {
        x += i;
    }
}
```

---

## 22. Conclusão

A linguagem permite a construção de programas estruturados e organizados, sendo adequada para testes de análise sintática com suporte a:

* Estruturas de controle
* Tipos variados
* Funções e classes
