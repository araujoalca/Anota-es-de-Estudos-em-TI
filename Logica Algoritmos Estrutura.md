# LÓGICA E PROGRAMAÇÃO  

**Programar** é resolver problemas, mais do que codificar. Antes de começar a codificar, o programador deve estabelecer qual será a lógica da resolução do problema que o programa irá lidar.

- **Metacognição:** pensar como vocêpensa.  
- **Algoritmo:** “é uma sequência depassos que resolve um problema”.   
- **Pseudocódigo:** “é uma forma genéricade escrever um algoritmo utilizando uma linguagem simples (nativa...).”  
- **Fluxograma:** “é uma ferramenta utilizada para representar graficamente o algoritmo, isto é, a sequência lógica e coerente do fluxo de dados”  
- **Linguagem de programação:** “...linguragem escrita e formal que especifica um conjunto de instruções e regras usadas para gerar programas...”

  [DIO][1]


# ESTRUTURAS DE DADOS  


***Principais Estruturas de Dados:***  

|      Estrutura                | **Considerações**                         |
| :---------------------------: | ----------------------------------------- |
| Array (Vetor / Matriz)        | Mesmo tipo, tamanho fixo e sequencial, uso de índices |
|          Registro             | Como um array que aceita tipos diferentes |
|            Lista              | Tamanho dinâmico, espaço espalhado na memória. Um **nó** faz referência ao elemento e ao próximo nó (usando ponteiros). Para se chegar a um elemento, precisa-se percorrer todos os elementos até chegar a ele. Normalmente implementada como "Lista Encadeada" ou "Array". **Lista Ligada**: um nó guarda a referência de nó seguinte a ele - é **unidirecional**. Já as **Listas Duplamente Ligadas** são **bidirecionais, pois cada nó, além de guardar a referência do nó seguinte, guarda a referência ao nó que o antecede. |
| Pilha (Stack)                 | Coleção de elementos com acesso a apenas um item (o último): **LIFO**. Exemplos de uso de pilhas em um sistema: Funções recursivas em compiladores; Mecanismo de desfazer/refazer dos editores de texto; Navegação entre páginas Web; etc. |
| Fila                          | Coleção de elementos com acesso a apenas um item (o primeiro): **FIFO** |
| Árvore<br>Tabela Hash,<br>Map, HashMap<br>Dicionário | Tabela Hash "é uma generalização da ideia de array, porém utiliza uma função denominada **Hashing** para espalhar os elementos, fazendo com que os mesmos fiquem de forma não ordenada dentro do “array” que define a tabela"[DIO][1]<br>Não é bom que esteja ordenada (melhor é estar balanceada). A árvore binária usa dois ponteiros (esq e dir) e uma chave.<br>Usa-se funções hash para determinar a posição de cada elemento. Faz uso de índices. Armazena pares (chave, valor) chamados itens, e podem ser de qualquer tipo |
| Grafo                         | Permite codificar relacionamentos (**arestas**) entre pares de objetos (**vértices** ou **nós**). Ex: relacionamentos numa rede social (amigos que se conhecem); ou um labirinto, ou um mapa do metrô (cada estação um nó e as linhas as arestas |
| Set (Conjunto)                | Grupo de dados homogêneos únicos, NÃO DUPLICADOS. Normalmente implementado como "Tabela Hash" ou "Árvore" |


**Referências:**
[DIO][1]
[Loiane Groner][2]
[DEVMEDIA][3]
[DSC - UFCG][4]
[UNIVESP][5]

[1]: https://web.dio.me/home "DIO"

[2]: https://www.youtube.com/watch?v=RW0oD2L_tSg&amp;list=PLGxZ4Rq3BOBrgumpzz-l8kFMw2DLERdxi&amp;index=46 "Loiane Groner"

[3]: https://www.devmedia.com.br/conhecendo-a-interface-map-do-java/37463 "DEVMEDIA"

[4]: http://www.dsc.ufcg.edu.br/~jacques/cursos/p2/html/ed/colecoes.htm "DSC - UFCG"

[5]: https://www.youtube.com/watch?v=y0B-vQI6Tiw&amp;list=PLxI8Can9yAHf8k8LrUePyj0y3lLpigGcl "UNIVESP"

