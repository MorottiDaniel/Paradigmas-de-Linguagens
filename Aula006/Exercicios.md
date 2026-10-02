# Exercícios - Análise 

### JavaScript:

a)
![Console JavaScript](./assets/javascript_output.png)

b) Detecção do problema: nunca detectado. 0.1 * 3 resulta em 0.30000000000000004 devido à limitação da representação em binário por isso que a comparação da false, número 9007199254740993 é igual a 2⁵³ + 1. Como o tipo Number em JS usa ponto flutuante de 64 bits, ele perde precisão inteira para valores acima de 2⁵³ (9007199254740992)

---

### Python

a)
![Console Python](./assets/python_output.png)

b) Detecção do problema: não há problemas. len(p) conta o número de caracteres/code points da string, retornando 4. p.encode() converte a string para uma sequência de bytes codificada em UTF-8. Como os caracteres ASCII (m, a) usam 1 byte cada e o caractere ç e o ã utilizam 2 bytes cada em UTF-8, a representação em bytes do texto consome um total de 6 bytes.

---

### Go

a)
![Console Go](./assets/go_output.png)

b) Detecção do problema: nunca detectado. O tipo byte em Go (inteiro sem sinal de 8 bits), cujo valor máximo é 255. Ao incrementar (b++), ocorre o estouro de inteiro, fazendo com que o valor retorne ao limite inferior (0).

---

### Java

a)
![Console Java](./assets/java_output.png)

b) Detecção do problema: Na execução. Array em java sempre começa com 0, como v[3] é um array de 3 posições (0, 1, 2) quando chamado print de v[3] da erro pois não existe numero dessa posição

---

### Rust

A)
![Console Rust](./assets/rust_output.png)

b) Detecção do problema: Na compilação. Rust utiliza o sistema de posse e empréstimo. Na atribuição let t = s;, a posse da string é movida de s para t. A variável s passa a ser considerada inválida. Quando a macro println! tenta acessar s na linha seguinte, o compilador detecta o erro e recusa a compilação.

---

### C

a)
![Console C](./assets/c_output.png)

b) Detecção do problema: Nunca detectado. C utiliza uniões livres. Os membros i e f compartilham exatamente o mesmo espaço de memória. Quando atribuímos 1.0f ao campo f, os bits dessa representação em ponto flutuante IEEE 754 (0x3F800000) são gravados na memória. Ao ler o campo i usando o especificador %d, o C simplesmente interpreta esses mesmos bits binários como se fossem um inteiro, resultando no valor decimal 1065353216 sem realizar nenhuma verificação de tipo.
