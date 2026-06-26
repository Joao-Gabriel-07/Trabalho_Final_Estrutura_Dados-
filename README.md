# Trabalho_Final_Estrutura_Dados-

Participantes: Filipe Araújo, João Gabriel da Silva Batista e Raul Bastos.

Turma: Sistemas de Informação - Matutino.

Trabalho A - Tema A1 Playlist de Musicas.
Trabalho B - Tema B2 Chamadas de Emergência.
Trabalho C - Tema C2 Filas de Impressão.


Trabalho A — Playlist de Músicas (Lista Duplamente Encadeada)

Explicação:

Gerencia uma playlist de músicas usando uma lista duplamente encadeada. Permite inserir, buscar, editar, remover e listar músicas em ordem normal e reversa, além de exibir estatísticas da playlist.

Como compilar: 
bashgcc musicas.c -o musicas

Como executar: 
bash./musicas

Observações:

A lista é duplamente encadeada, com ponteiros prox e ant, permitindo navegação nos dois sentidos.
A busca parcial localiza músicas por parte do título ou nome do artista.
Exibe estatísticas como total de músicas, duração total e duração média.
Permite limpar toda a playlist com confirmação.
Salva e carrega os dados em musicas.csv.
IDs duplicados são bloqueados automaticamente.


Dificuldades encontradas:

Manter os ponteiros ant e ultimo corretamente atualizados durante inserção e remoção.
Leitura de float com scanf deixava o buffer sujo, exigindo while (getchar() != '\n') para limpar.


Trabalho B — Sistema de Chamadas de Emergência (Pilha)

Explicação:

Simula um sistema de atendimento de emergências utilizando uma pilha encadeada (LIFO). Cada chamada registrada vai para o topo da pilha e é atendida na ordem inversa de chegada. O sistema controla protocolo, local, tipo e horário de cada ocorrência.

Como compilar: 
bashgcc chamadas_emergencia.c -o chamadas

Como executar: 
bash./chamadas

Observações:

A pilha segue a lógica LIFO (Last In, First Out): a última chamada registrada é a primeira a ser atendida.
O programa valida protocolos duplicados.
Antes de atender (Pop), exige confirmação do usuário.
Exporta um relatório completo em relatorio.txt.
Salva e carrega os dados em chamadas.csv.
Interface colorida com códigos ANSI.


Dificuldades encontradas:

Ajuste do scanf(" %[^\n]") para leitura correta de strings com espaços.
Garantir que o carregamento do CSV reconstruísse a pilha na ordem correta, inserindo no topo.
Permissão para criar arquivos em notebooks institucionais com restrições de escrita.

Trabalho C — Fila de Impressão (Fila Normal + Fila Circular Encadeada)

Explicação:

Simula uma fila de impressão com dois tipos de trabalho: normal e prioritário. Trabalhos prioritários são sempre processados antes dos normais. A fila normal é uma lista encadeada simples e a fila prioritária é uma fila circular encadeada.

Como compilar:

bashgcc impressao.c -o impressao

Como executar:

bash./impressao

Observações:

A regra de atendimento é: sempre prioritário primeiro; só processa normal quando a fila prioritária estiver vazia.
A fila prioritária é circular encadeada: o último nó aponta de volta para o primeiro.
Exibe estatísticas de atendimento: total processado, prioritários, normais e páginas impressas.
Exporta relatório em relatorio_impressao.txt com situação atual das filas.
Salva e carrega os dados em impressao.csv.
O carregamento limpa as filas antes de reconstruir, evitando duplicatas.


Dificuldades encontradas:

Manter os ponteiros inicio e fim da fila circular corretamente atualizados ao remover e cancelar elementos.
O Online GDB apresentou instabilidade na criação de arquivos CSV e TXT entre sessões diferentes.
Garantir que o carregamento do CSV não duplicasse os dados já existentes na fila.
