# Lista de Exercícios: Evolução das Linguagens de Programação

---

### **Questão 1**
**Enunciado:** A genealogia das linguagens não é uma escada de progresso. Explique essa afirmação e apresente dois fatores históricos que fazem uma linguagem influenciar outra sem necessariamente substituí-la.

**R:** A evolução das linguagens não é uma escada perfeita de progresso porque novas linguagens não tornam as antigas obsoletas de forma absoluta. Cada linguagem é projetada assumindo diferentes compromissos de projeto para resolver problemas específicos. 

Dois fatores históricos de influência sem substituição:
* **Foco em Domínios de Aplicação:** O Fortran continuou sendo a escolha principal para cálculo científico por décadas por ser altamente otimizado para isso, mesmo após o surgimento de linguagens mais modernas. 
* **Legado Conceitual:** O ALGOL 60 definiu a estrutura de blocos e gramática formal que moldou o C e o Pascal, mas teve baixa adesão comercial por falta de apoio corporativo. 

---

### **Questão 4**
**Enunciado:** Explique por que o projeto Fortran precisou convencer programadores de que código traduzido podia competir com código de máquina escrito à mão. Relacione desempenho, custo de programação e adoção.

**R:** Na década de 1950, o tempo de processamento dos computadores era caríssimo, e os programadores acreditavam que apenas o código escrito à mão em Assembly tinha alto desempenho. Para que o Fortran fosse adotado, John Backus precisou provar que o compilador gerava um código traduzido quase tão rápido quanto o manual.
* **Desempenho:** Se o código traduzido fosse lento, o custo de máquina seria inviável.
* **Custo de Programação:** Provado o desempenho, o tempo para criar um programa caiu drasticamente. 
* **Adoção:** O menor tempo/custo de desenvolvimento gerou aceitação massiva na indústria. 

---

### **Questão 5**
**Enunciado:** Lisp surgiu em um contexto diferente de Fortran. Compare os domínios, a representação de dados e o estilo de computação favorecido pelas duas linguagens.

**R:** Fortran é voltado para a computação científica, com dados numéricos escalares e arranjos/matrizes contíguos em memória, com estilo imperativo, focado em alteração de estados da memória por atribuição, sequenciamento e loops iterativos.

Lisp foi criador para pesquisa em inteligência artificial e computação simbólica, com dados baseados em estruturas de listas e átomos, todos os dados quanto o próprio código da linguagem são representados como listas, com estilo funcional, onde a computação é feita avaliando funções e expressões matemáticas, priorizando a recursão em vez de loops procedurais.

---

### **Questão 6**
**Enunciado:** Avalie três contribuições de ALGOL 60 que ultrapassaram sua adoção comercial. Por que uma linguagem pode ser muito influente sem dominar o mercado?

**R:** Três contribuições duradouras do ALGOL 60: 
* **Estrutura de Blocos:** Introdução do escopo de variáveis delimitado por `begin ... end`. 
* **Notação BNF:** Criação do método formal universal para definir a gramática de linguagens. 
* **Recursão Nativa:** Suporte oficial para funções chamando a si mesmas.

Uma linguagem pode moldar os conceitos teóricos do projeto de linguagens sem dominar o mercado devido a fatores como falta de apoio corporativo, complexidade de implementação e ausência de rotinas de entrada/saída padronizadas em sua especificação original.

---

### **Questão 7**
**Enunciado:** COBOL foi desenhada para processamento comercial. Mostre como domínio e público influenciaram sua legibilidade, seus registros e sua relação com FLOW-MATIC.

**R:** O COBOL foi focado no ambiente corporativo e de negócios, com uma sintaxe que lembra o inglês comum para permitir que gerentes e auditores conseguissem ler o código. Criou estruturas de dados hierárquicas (com níveis 01, 05, etc.) ideais para representar fichas de clientes ou folha de pagamento. Baseou-se na linguagem FLOW-MATIC, herdando o uso de palavras reservadas descritivas em vez de notações matemáticas. 

---

### **Questão 11**
**Enunciado:** Construa uma cadeia de influência que passe por ALGOL, Pascal e C. Depois contraste essa linhagem imperativa com a proposta declarativa de Prolog.

**R:** Existe uma cadeia de influencia entre as 3 linguagens mencionadas no enunciado, seguido na ordem (ALGOL, Pascal e C). Começando com ALGOL que tem muita influencia na linguagem Pascal e na estruturação de programação imperativa, além de ter sido muito importante para apresentar conceitos focado em estrutura de controle, blocos, escopo e sintaxe mais organizada na representação de algoritmos.

O pascal em seguida aproveitou as ideias mostrado pelo ALGOL e aderiu a forte preocupação com estruturação dos programas e tipagem, se tornando muito útil no ensino de programação estruturada, por fim o C, que apesar de ter surgido de uma linhagem diferente a BCPL e B, compartilhou da influencia deixado pelas 2 outras linguagens, no caso a programação estruturada e imperativa.

O que pudemos entender dessa relação histórica iniciada por ALGOL é que os programas organizados em procedimentos, estruturas de controle e uma abordagem imperativa, ou seja, que o programador conduz a sequencia de operações que modificam o estado de programa são atrelados ao paradigma imperativo. Em contraste o Prolog, que pertence ao paradigma de programação lógica apresenta uma proposta declarativa no qual, em vez de especificar uma sequência de comandos para produzir determinado resultado, o programador descreve fatos e relações, enfatizando o que é verdadeiro dentro de um determinado conjunto de fatos e regras.

---

### **Questão 12**
**Enunciado:** Modele em linguagem natural uma pequena base Prolog com dois fatos, uma regra e uma consulta. Explique por que isso representa programação lógica, não apenas armazenamento de dados.

**R:**  
Usando esse prompt:
```prolog
gosta(joao, programacao).
gosta(maria, programacao).

estuda(X, programacao) :- gosta(X, programacao).

?- estuda(joao, programacao).
```
Criamos os 2 fatos (João e Maria gostam de programação), regra (Uma pessoa que estuda programação se ela gosta de programação) e a consulta (João estuda programação), como Prolog utiliza fatos, regras e consultas para representar uma base de conhecimento.

Por exemplo, podemos ter os fatos “João gosta de programação” e “Maria gosta de programação”, além da regra “quem gosta de programação estuda programação”.

Ao consultar se João estuda programação, Prolog pode concluir que sim.
Isso caracteriza programação lógica porque há inferência a partir de fatos e regras, e não apenas armazenamento de dados.

---

### **Questão 13**

**Enunciado:** Ada resultou de requisitos e projeto em grande escala. Analise como confiabilidade, tipos, pacotes e concorrência se relacionam ao domínio de sistemas críticos.

**R:** Ada foi projetada para sistemas de grande escala, nos quais confiabilidade e segurança são fundamentais. A tipagem forte ajuda a detectar erros, enquanto os pacotes permitem organizar o programa em módulos, facilitando manutenção e controle da complexidade.

Seus recursos de concorrência permitem representar tarefas executadas simultaneamente, importantes em sistemas embarcados e de tempo real. Assim, esses recursos tornam Ada adequada para sistemas críticos e de alta confiabilidade.

---

### **Questão 14**

**Enunciado:** Compare o papel dos objetos em Smalltalk, C++ e Java. Inclua na resposta o compromisso de C++ com C e a estratégia de portabilidade de Java.

**R:** Smalltalk, C++ e Java utilizam o conceito de objetos, mas de maneiras diferentes. Em Smalltalk, os objetos são o elemento central da linguagem, e praticamente tudo é tratado como objeto, seguindo fortemente o paradigma orientado a objetos.

O C++ incorporou a orientação a objetos ao C, mantendo grande parte de sua compatibilidade e características, como o acesso de baixo nível à memória. Dessa forma, o C++ permite utilizar tanto recursos de programação estruturada quanto recursos de orientação a objetos.

Já o Java foi projetado com uma abordagem mais voltada à orientação a objetos e à portabilidade. Seu código é compilado para bytecode, que pode ser executado pela Máquina Virtual Java (JVM), permitindo que o mesmo programa seja executado em diferentes sistemas sem precisar ser recompilado especificamente para cada plataforma.

Assim, podemos entender que Smalltalk prioriza a orientação a objetos, C++ busca combinar orientação a objetos com a tradição e o controle de baixo nível do C, enquanto Java prioriza a orientação a objetos junto com a portabilidade entre diferentes plataformas.

---

### **Questão 15**

**Enunciado:** A primeira aplicação de Java não foi a Web, mas a Web impulsionou sua adoção. Explique como mudanças de contexto podem reposicionar uma linguagem.

**R:** Java foi criada inicialmente para dispositivos eletrônicos e sistemas embarcados, buscando portabilidade e segurança. Porém, com o crescimento da Web, suas características se tornaram úteis para o desenvolvimento de aplicações na Internet. A JVM permitia que os programas fossem executados em diferentes sistemas, facilitando sua portabilidade. Com isso, Java passou a ser muito utilizada no desenvolvimento Web, mesmo não tendo sido criada inicialmente para esse propósito. Isso demonstra como uma mudança de contexto pode aumentar a importância de uma linguagem e direcioná-la para novos domínios.
