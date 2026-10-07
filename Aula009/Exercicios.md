# Exercícios

---

## Java

### (a) Código e Saída
<img width="770" height="520" alt="image" src="https://github.com/user-attachments/assets/82084e9f-0a13-40ff-b41a-abee6ba43fec" />


### (b) Decisão e Explicação
Decisão: Execução. Em Java os métodos comuns são dinâmicos por padrão, então ele olha o tipo do objeto real no monte (Cachorro) e não a referência.

---

## C++

### (a) Código e Saída
<img width="633" height="566" alt="image" src="https://github.com/user-attachments/assets/258c5545-28f3-4fbd-b409-ee82b0a4cbab" />


### (b) Decisão e Explicação
Decisão: Compilação. O método f() não tem a palavra-chave virtual em A. Por isso, o C++ chama direto o método baseado no tipo do ponteiro (A*).

---

## Java

### (a) Código e Saída
<img width="888" height="522" alt="image" src="https://github.com/user-attachments/assets/7b94e6d9-2bdd-4e8f-b4ff-3bcba76a654b" />


### (b) Decisão e Explicação
x.nome: Compilação (atributos/campos não têm polimorfismo em Java; ele pega o nome da classe declarada A. x.getNome(): Execução (método sobrescrito roda no objeto real B.

---

## Python

### (a) Código e Saída
<img width="650" height="331" alt="image" src="https://github.com/user-attachments/assets/458b8b30-dc4a-4969-b8e1-645a5ae2e3dc" />


### (b) Decisão e Explicação
Decisão: Execução. O atributo de classe total é compartilhado por todas as instâncias. A cada __init__ executado, ele incrementa esse total geral.

---

## Java

### (a) Código e Saída
<img width="769" height="550" alt="image" src="https://github.com/user-attachments/assets/3518391f-07cd-4ba6-90e6-eb931edc3c15" />


### (b) Decisão e Explicação
Decisão: Compilação (métodos static em Java não têm vinculação dinâmica). Como a variável x foi declarada como tipo A, ele chama o método estático de A.

---

## GO

### (a) Código e Saída
<img width="774" height="558" alt="image" src="https://github.com/user-attachments/assets/1810692a-de5e-4884-a4cb-851924c6b023" />


### (b) Decisão e Explicação
Decisão: Compilação. O método Falar() do struct embutido Animal chama internamente o seu próprio a.Som(), e não o Som() do Cao.
