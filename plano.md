# Plano da apresentacao: Ciclo Hamiltoniano

## Ideia central

O Ciclo Hamiltoniano e um problema de grafos simples de entender:

> Da para sair de um vertice, passar por todos os vertices exatamente uma vez e voltar para o inicio?

O ponto central da apresentacao e mostrar o contraste entre tres ideias:

- explicar o problema e facil;
- conferir uma resposta tambem e facil;
- descobrir se existe uma resposta, em geral, pode ser muito dificil.

## Objetivos para a turma

Ao final da apresentacao, a turma deve entender:

- o que e um caminho hamiltoniano;
- o que e um ciclo hamiltoniano;
- qual e a diferenca entre ciclo hamiltoniano e ciclo euleriano;
- como escrever o problema como um problema de decisao;
- por que uma solucao candidata e facil de verificar;
- por que o problema esta em NP;
- por que ele e um exemplo classico de problema NP-completo;
- que existem algoritmos exatos, mas eles crescem muito rapido;
- que, na pratica, muitas abordagens usam busca, poda, programacao dinamica ou heuristicas.

## Organizacao sugerida dos slides

### Slide 1 - Titulo e pergunta central

Abrir com o titulo **Ciclo Hamiltoniano** e uma pergunta simples:

> Existe um passeio fechado que visita todos os vertices uma unica vez?

Esse comeco coloca a turma direto no problema antes de entrar nas definicoes. Se ja houver um grafo pequeno na tela, a pergunta fica concreta desde o primeiro momento.

### Slide 2 - Definicoes basicas

Alinhar o vocabulario minimo:

- grafo;
- vertice;
- aresta;
- caminho;
- ciclo;
- caminho hamiltoniano;
- ciclo hamiltoniano.

Nao vale gastar muito tempo aqui. O objetivo e apenas garantir que todos consigam acompanhar os exemplos seguintes.

### Slide 3 - Exemplo com ciclo hamiltoniano

Mostrar um grafo pequeno em que o ciclo existe e escrever a ordem dos vertices. O ponto e deixar claro que nao basta o desenho parecer circular: o ciclo precisa visitar todos os vertices uma unica vez e voltar ao inicio.

Esse slide e importante porque a definicao fica mais facil quando a turma ve uma sequencia concreta.

### Slide 4 - Exemplo sem ciclo hamiltoniano

Trazer um grafo pequeno que nao tem ciclo, de preferencia com um vertice de grau 1 ou alguma estrutura que force repeticao.

A ideia e mostrar que a ausencia do ciclo nao e uma questao de desenhar melhor o caminho. Em alguns casos, a propria estrutura do grafo impede a solucao.

### Slide 5 - Hamiltoniano vs. Euleriano

Usar a comparacao com Euler para evitar uma confusao comum:

- o ciclo hamiltoniano se preocupa com vertices;
- o ciclo euleriano se preocupa com arestas.

A tabela pode ser simples e visual. O objetivo e deixar claro que os dois problemas parecem parecidos no nome, mas pedem coisas diferentes.

### Slide 6 - Problema de decisao

Apresentar a pergunta formal:

> Dado um grafo `G`, `G` possui um ciclo hamiltoniano?

Depois, mostrar tres formas de olhar para o tema:

- decidir se existe;
- encontrar um ciclo quando existe;
- otimizar algum custo, como no Problema do Caixeiro Viajante.

Esse slide faz a ponte entre o desenho do grafo e a linguagem de complexidade.

### Slide 7 - Verificar e facil

Mostrar uma sequencia candidata, por exemplo:

```text
A, C, D, B, E, A
```

Explicar como conferir:

- todos os vertices aparecem uma vez;
- cada par consecutivo e uma aresta;
- o ultimo vertice volta ao primeiro.

O ponto e separar duas tarefas diferentes: verificar uma resposta pronta e rapido; descobrir a resposta pode nao ser.

### Slide 8 - Encontrar e dificil

Usar este slide para falar da explosao combinatoria. Com muitos vertices, o numero de ordens possiveis cresce muito rapido, entao testar tudo deixa de ser viavel.

Vale citar que existem algoritmos melhores que forca bruta, como programacao dinamica no estilo Held-Karp, mas que eles ainda tem custo exponencial.

### Slide 9 - NP e NP-completo sem pesar

Explicar sem entrar em prova longa:

- o problema esta em NP porque da para conferir um certificado em tempo polinomial;
- o problema e NP-completo porque representa uma dificuldade central dentro de NP.

A ideia nao e demonstrar a reducao, mas deixar a turma entender o peso da afirmacao: se houvesse um algoritmo polinomial geral para Ciclo Hamiltoniano, isso mexeria com a questao `P` versus `NP`.

### Slide 10 - Quando da para garantir ou tentar resolver

Mostrar que "dificil em geral" nao significa "impossivel sempre".

Existem casos especiais e condicoes suficientes, como o Teorema de Dirac, que garantem ciclo hamiltoniano em grafos bem conectados.

Na pratica, tambem aparecem abordagens como:

- busca com poda;
- programacao dinamica;
- modelagem como SAT;
- programacao linear inteira;
- heuristicas.

Esse slide ajuda a nao deixar a apresentacao pessimista demais.

### Slide 11 - Aplicacoes e conexoes

Falar de conexoes sem vender o problema como uma solucao direta para tudo. Boas pontes:

- roteamento;
- Problema do Caixeiro Viajante;
- passeio do cavalo;
- reconstrucao em bioinformatica;
- modelos de visita sem repeticao em redes.

O valor deste slide e mostrar que o problema aparece tanto como ferramenta de modelagem quanto como exemplo classico de limite algoritmico.

### Slide 12 - Fechamento

Fechar voltando a frase-guia:

> Simples de explicar, facil de verificar e dificil de resolver em geral.

Uma boa pergunta final e:

> Por que verificar uma resposta nao e a mesma coisa que encontrar uma resposta?

Ela resume a ligacao entre o problema de grafos e a discussao de complexidade.

## Topicos para o handout

O handout pode ser um pouco mais completo que os slides, mas ainda curto.

Sugestao de estrutura:

- definicao informal;
- definicao mais formal;
- exemplo positivo;
- exemplo negativo;
- diferenca para ciclo euleriano;
- problema de decisao;
- certificado e verificacao;
- NP e NP-completude;
- ideia de algoritmos: forca bruta, backtracking, programacao dinamica e heuristicas;
- aplicacoes e conexoes.
