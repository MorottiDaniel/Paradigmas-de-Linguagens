# Exercícios

### JavaScript:

a)
<img width="219" height="163" alt="image" src="https://github.com/user-attachments/assets/7e2562d1-4d34-4e3a-bb57-a0856b81ef65" />

b) Detecção do problema: nunca detectado. 0.1 * 3 resulta em 0.30000000000000004 devido à limitação da representação em binário por isso que a comparação da false, número 9007199254740993 é igual a 2⁵³ + 1. Como o tipo Number em JS usa ponto flutuante de 64 bits, ele perde precisão inteira para valores acima de 2⁵³ (9007199254740992)

---

### Python

a)
<img width="163" height="136" alt="image" src="https://github.com/user-attachments/assets/e46dda00-83e6-4155-abfe-d21ba71d94d1" />


b) Detecção do problema: não há problemas. len(p) conta o número de caracteres/code points da string, retornando 4. p.encode() converte a string para uma sequência de bytes codificada em UTF-8. Como os caracteres ASCII (m, a) usam 1 byte cada e o caractere ç e o ã utilizam 2 bytes cada em UTF-8, a representação em bytes do texto consome um total de 6 bytes.

---

### Go

a)
<img width="433" height="152" alt="image" src="https://github.com/user-attachments/assets/b2bfb997-3596-4d80-ad3b-182e9440ce33" />


b) Detecção do problema: nunca detectado. O tipo byte em Go (inteiro sem sinal de 8 bits), cujo valor máximo é 255. Ao incrementar (b++), ocorre o estouro de inteiro, fazendo com que o valor retorne ao limite inferior (0).

---

### Java

a)
<img width="789" height="238" alt="image" src="https://github.com/user-attachments/assets/b6a9e120-be51-4ad7-bc64-48cde3d95e64" />


b) Detecção do problema: Na execução. Array em java sempre começa com 0, como v[3] é um array de 3 posições (0, 1, 2) quando chamado print de v[3] da erro pois não existe numero dessa posição

---

### Rust

A)
<img width="792" height="769" alt="image" src="https://github.com/user-attachments/assets/bff93d5d-5619-4373-92c1-5f89ace6738f" />


b) Detecção do problema: Na compilação. Rust utiliza o sistema de posse e empréstimo. Na atribuição let t = s;, a posse da string é movida de s para t. A variável s passa a ser considerada inválida. Quando a macro println! tenta acessar s na linha seguinte, o compilador detecta o erro e recusa a compilação.

---

### C

a)
<img width="163" height="117" alt="image" src="https://github.com/user-attachments/assets/a9ac6b1c-a34e-4527-a540-20b5f9aeab40" />


b) Detecção do problema: Nunca detectado. C utiliza uniões livres. Os membros i e f compartilham exatamente o mesmo espaço de memória. Quando atribuímos 1.0f ao campo f, os bits dessa representação em ponto flutuante IEEE 754 (0x3F800000) são gravados na memória. Ao ler o campo i usando o especificador %d, o C simplesmente interpreta esses mesmos bits binários como se fossem um inteiro, resultando no valor decimal 1065353216 sem realizar nenhuma verificação de tipo.
