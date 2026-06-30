# Relatório Técnico - Estruturas de Dados

## Escolha das Estruturas de Dados

* **Trabalho A (Playlist de Músicas):** Utilizamos uma **Lista Duplamente Encadeada** porque permite a navegação bidirecional (ir para a próxima música ou voltar para a anterior) de forma eficiente através dos ponteiros `prox` e `ant`.
* Funcionalidades extras utilizadas.
  
* **Trabalho B (Chamadas de Emergência):** Utilizamos uma **Pilha Dinâmica (LIFO)** pois, em sistemas de atendimento a emergências, a última chamada recebida frequentemente representa a situação mais recente e crítica que necessita de atenção imediata.
* Funcionalidades extras utilizadas.
    
* **Trabalho C (Fila de Impressão):** Combinamos uma **Fila Dinâmica Simples** (para o fluxo normal) com uma **Fila Circular Encadeada** (para o fluxo prioritário). A fila circular garante um ciclo contínuo de prioridade absoluta, processando todos os elementos prioritários antes de liberar a fila comum.
* Funcionalidades extras utilizadas.
  
## Conclusão
O projeto foi fundamental para solidificar conceitos práticos de alocação dinâmica de memória (`malloc`/`free`), manipulação de ponteiros, persistência de arquivos em formato CSV e organização estruturada de repositórios.
