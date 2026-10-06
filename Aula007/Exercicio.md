# Exercício

---

## JavaScript

### (a) Saída com erro
<img width="170" height="116" alt="image" src="https://github.com/user-attachments/assets/0382058f-6537-4fb4-b5b0-bddef5f74331" />


### (b) Detecção e Explicação do Problema
A instrução `for...in` em JavaScript itera sobre as chaves/índices (que são strings: `"0"`, `"1"`, `"2"`), e não sobre os valores do array. Ao usar `total += p`, ocorre coerção implícita de tipos e concatenação de strings (`0 + "0" -> "00"`, `"00" + "1" -> "001"`, etc.).

### (c) Correção do Código
<img width="605" height="233" alt="image" src="https://github.com/user-attachments/assets/8ca69905-fb57-482f-b286-e710d5a4672e" />


---

## Python

### (a) Saída com erro
<img width="189" height="167" alt="image" src="https://github.com/user-attachments/assets/098c32bf-54a2-48f9-8b58-a1a6a05b399f" />

### (b) Detecção e Explicação do Problema
Avaliação booleana em curto-circuito do operador `or` em Python. O valor numérico `0` é avaliado como `False`. Portanto, na expressão `d = 0 or 10`, o operador ignora o `0` e atribui o valor padrão `10`, ignorando a intenção de aplicar `0%` de desconto.

### (c) Correção do Código
<img width="623" height="367" alt="image" src="https://github.com/user-attachments/assets/fb975fb0-4201-492d-a0c7-2875c2c33d98" />


---

## Java (Switch)

### (a) Saída com erro
<img width="170" height="125" alt="image" src="https://github.com/user-attachments/assets/466574ce-47a1-46f9-a615-45a70cfd588c" />

### (b) Detecção e Explicação do Problema
A ausência da instrução `break`, a execução "cai" para os casos seguintes consecutivamente (`case 2 -> case 3 -> default`), sobrescrevendo a variável `nome` até o valor final `"inválido"`.

### (c) Correção do Código
<img width="759" height="519" alt="image" src="https://github.com/user-attachments/assets/135d29c9-b764-4877-ae52-f9b96b37489f" />

---

## C

### (a) Saída com erro
<img width="248" height="188" alt="image" src="https://github.com/user-attachments/assets/a8771bf4-0974-4782-baf1-bba04de4ff8e" />


### (b) Detecção e Explicação do Problema
Instrução nula (ponto e vírgula `;` logo após o `if`). Em C, o `;` fecha o bloco do `if` imediatamente como uma instrução vazia. O comando `printf("saldo insuficiente\n");` deixa de fazer parte da condição e passa a ser executado incondicionalmente.

### (c) Correção do Código
<img width="641" height="344" alt="image" src="https://github.com/user-attachments/assets/55723445-3d4a-4b3b-a75a-2025c6a709ca" />


---

## Go

### (a) Saída com erro
<img width="173" height="163" alt="image" src="https://github.com/user-attachments/assets/6aacecd4-fff9-4700-be3d-f1120896ea9c" />


### (b) Detecção e Explicação do Problema
Ao utilizar o operador de declaração curta `:=` dentro do bloco `if`, Go declara uma nova variável local `x` que existe apenas no escopo do bloco. A variável `x` do escopo externo não é alterada.

### (c) Correção do Código
<img width="650" height="428" alt="image" src="https://github.com/user-attachments/assets/7f5e1799-4012-4b8c-a530-c092c084c948" />


---

## Java (Expressão de Divisão)

### (a) Saída com erro
<img width="141" height="114" alt="image" src="https://github.com/user-attachments/assets/d9f37917-d2df-46ea-a70b-b9d7a68be660" />

### (b) Detecção e Explicação do Problema
Como `acertos` e `total` são dois operandos do tipo `int`, a operação `7 / 10` realiza truncamento inteiro resultando em `0`. Apenas ao final da expressão o resultado `0 * 100 = 0` é convertido (*widened*) para `double` (`0.0`).

### (c) Correção do Código
<img width="833" height="409" alt="image" src="https://github.com/user-attachments/assets/ad5c4e95-5399-4432-8920-44f75dabc499" />
