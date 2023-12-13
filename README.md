# Sistema de Gerenciamento de Banco de Dados - ITP
Este é um sistema simples de gerenciamento de tabelas em C. O projeto é estruturado em módulos separados para as operações de criação, edição, exclusão e visualização de tabelas. Abaixo, fornecemos uma visão geral da estrutura do projeto, suas dependências e principais funções.

## Estrutura do Projeto

O projeto é composto por vários módulos organizados em arquivos separados:

- `criacao.h`: Módulo para funções relacionadas à criação de tabelas.
- `edicao.h`: Módulo para funções relacionadas à edição de tabelas.
- `exclusao.h`: Módulo para funções relacionadas à exclusão de linhas e tabelas.
- `visualizacao.h`: Módulo para funções relacionadas à visualização de tabelas.

Cada módulo possui suas implementações correspondentes em arquivos `.c`.

O arquivo principal `main.c` contém a função principal (`main()`) que interage com o usuário e coordena a execução das operações do sistema.

## Dependências

O projeto depende dos seguintes cabeçalhos padrão da linguagem C e de seus próprios módulos:

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "criacao.h"
#include "edicao.h"
#include "exclusao.h"
#include "visualizacao.h"
```

## Outras Funções
- criarTabela: Permite ao usuário criar uma nova tabela especificando seu nome, colunas e valores iniciais.
- mostarTodas: Lista todas as tabelas existentes.
- criarLinha: Permite ao usuário adicionar uma nova linha (registro) a uma tabela existente.
- mostrarTabela: Exibe os conteúdos de uma tabela específica.
- pesquisaValor: Pesquisa um valor específico em uma tabela.
- editarValorTabela: Permite ao usuário editar o valor de uma coluna em uma tabela.
- deletarLinha: Permite ao usuário apagar uma linha específica de uma tabela.
- deletarTabela: Permite ao usuário apagar uma tabela existente.

## Contribuição
o Projeto foi feito por Dinorah Farias e Flawbert Lorran, e foi feita a seguinte divisão por modulos:

### Dinorah
* criacao.c
* estruturas.c
* visualizacao.c

### Flawbert
* edicao.c
* exclusao.c


***


## Compilação e execução
