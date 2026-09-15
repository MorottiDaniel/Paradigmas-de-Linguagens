# Atividade de Paradigmas de Linguagens de Programação: Derivação Sintática

---

## 1. Fonte da Gramática e Construto Sintático Escolhido

* **Linguagem:** Python 3
* **Construto Sintático:** Comando condicional `if...else` com expressão de comparação
* **Fonte da Gramática:** *The Python Language Reference* — Seção 8.5 (*The if statement*) e Seção 10 (*Full Grammar specification* / EBNF).
* **Referência:** Official Python Documentation (https://docs.python.org/3/reference/grammar.html).

---

## 2. Subconjunto da Gramática (BNF / EBNF Simplificada)

Para fins didáticos, utilizaremos um subconjunto da gramática que descreve a estrutura essencial do comando `if...else` em Python.

```bnf
<if_stmt>        ::= "if" <test> ":" <suite> "else" ":" <suite>
<test>           ::= <expr> <comp_op> <expr>
<comp_op>        ::= ">" | "<" | "==" | ">=" | "<=" | "!="
<expr>           ::= <identifier> | <literal>
<suite>          ::= <stmt>
<stmt>           ::= <assign_stmt> | <print_stmt>
<assign_stmt>    ::= <identifier> "=" <expr>
<print_stmt>     ::= "print" "(" <expr> ")"
<identifier>     ::= "idade" | "status"
<literal>        ::= "18" | '"Maior"' | '"Menor"'
```

> **Legenda:**
>
> * Os símbolos entre `< >` são **não-terminais**.
> * As cadeias entre aspas ou em texto simples como `if`, `else`, `:`, `=`, `>`, `(`, `)` são **terminais**.

---

## 3. Código Fonte Reconhecido

O trecho de código em Python a ser derivado a partir das regras estabelecidas é:

```python
if idade >= 18:
    status = "Maior"
else:
    status = "Menor"
```

---

## 4. Derivação Passo a Passo (Derivação Mais à Esquerda)

A derivação a seguir inicia-se no símbolo não-terminal `<if_stmt>` e realiza substituições sucessivas do não-terminal localizado mais à esquerda até obter a sequência exata de terminais do código escolhido.

1. `<if_stmt>`
2. $\Rightarrow$ `if` `<test>` `:` `<suite>` `else` `:` `<suite>`
3. $\Rightarrow$ `if` `<expr>` `<comp_op>` `<expr>` `:` `<suite>` `else` `:` `<suite>`
4. $\Rightarrow$ `if` `<identifier>` `<comp_op>` `<expr>` `:` `<suite>` `else` `:` `<suite>`
5. $\Rightarrow$ `if` `idade` `<comp_op>` `<expr>` `:` `<suite>` `else` `:` `<suite>`
6. $\Rightarrow$ `if` `idade` `>=` `<expr>` `:` `<suite>` `else` `:` `<suite>`
7. $\Rightarrow$ `if` `idade` `>=` `<literal>` `:` `<suite>` `else` `:` `<suite>`
8. $\Rightarrow$ `if` `idade` `>=` `18` `:` `<suite>` `else` `:` `<suite>`
9. $\Rightarrow$ `if` `idade` `>=` `18` `:` `<stmt>` `else` `:` `<suite>`
10. $\Rightarrow$ `if` `idade` `>=` `18` `:` `<assign_stmt>` `else` `:` `<suite>`
11. $\Rightarrow$ `if` `idade` `>=` `18` `:` `<identifier>` `=` `<expr>` `else` `:` `<suite>`
12. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `<expr>` `else` `:` `<suite>`
13. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `<literal>` `else` `:` `<suite>`
14. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `<suite>`
15. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `<stmt>`
16. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `<assign_stmt>`
17. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `<identifier>` `=` `<expr>`
18. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `status` `=` `<expr>`
19. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `status` `=` `<literal>`
20. $\Rightarrow$ `if` `idade` `>=` `18` `:` `status` `=` `"Maior"` `else` `:` `status` `=` `"Menor"`

---

## 5. Explicação Textual Coerente

1. **Estrutura Sintática:** O comando condicional `if...else` permite a execução de blocos de código distintos dependendo do valor lógico de uma expressão de teste (`<test>`).
2. **Avaliação da Condição:** A subcadeia `idade >= 18` é reconhecida pelo não-terminal `<test>`, composto por uma expressão de identificador (`idade`), um operador relacional (`>=`) e um literal inteiro (`18`).
3. **Blocos de Execução (`<suite>`):**
   * Se a condição for verdadeira, o primeiro `<suite>` substitui-se pelo comando de atribuição `status = "Maior"`.
   * Caso contrário, a cláusula `else:` desvia a execução para o segundo `<suite>`, que atribui `status = "Menor"`.
4. **Conclusão:** A derivação formal demonstra que o código fonte escrito é sintaticamente válido segundo as regras da gramática do Python, garantindo que o parser da linguagem conseguirá construir a Árvore de Análise Sintática (*Parse Tree*) correspondente.
